import mido
from mido import Message, MidiFile, MidiTrack

#把音名、唱名等换成 MIDO相对应的数字
#已完成
# 简化了下并增加升降
def num(noteName):
    if noteName in ["A0", "a0"]:
        return 21
    elif noteName in ["A#0", "a#0", "Bb0", "bb0"]:
        return 22
    elif noteName in ["B0", "b0"]:
        return 23
    elif noteName in ["C1", "c1"]:
        return 24
    elif noteName in ["C#1", "c#1", "Db1", "db1"]:
        return 25
    elif noteName in ["D1", "d1"]:
        return 26
    elif noteName in ["D#1", "d#1", "Eb1", "eb1"]:
        return 27
    elif noteName in ["E1", "e1"]:
        return 28
    elif noteName in ["F1", "f1"]:
        return 29
    elif noteName in ["F#1", "f#1", "Gb1", "gb1"]:
        return 30
    elif noteName in ["G1", "g1"]:
        return 31
    elif noteName in ["G#1", "g#1", "Ab1", "ab1"]:
        return 32
    elif noteName in ["A1", "a1"]:
        return 33
    elif noteName in ["A#1", "a#1", "Bb1", "bb1"]:
        return 34
    elif noteName in ["B1", "b1"]:
        return 35
    elif noteName in ["C2", "c2"]:
        return 36
    elif noteName in ["C#2", "c#2", "Db2", "db2"]:
        return 37
    elif noteName in ["D2", "d2"]:
        return 38
    elif noteName in ["D#2", "d#2", "Eb2", "eb2"]:
        return 39
    elif noteName in ["E2", "e2"]:
        return 40
    elif noteName in ["F2", "f2"]:
        return 41
    elif noteName in ["F#2", "f#2", "Gb2", "gb2"]:
        return 42
    elif noteName in ["G2", "g2"]:
        return 43
    elif noteName in ["G#2", "g#2", "Ab2", "ab2"]:
        return 44
    elif noteName in ["A2", "a2"]:
        return 45
    elif noteName in ["A#2", "a#2", "Bb2", "bb2"]:
        return 46
    elif noteName in ["B2", "b2"]:
        return 47
    elif noteName in ["C3", "c3"]:
        return 48
    elif noteName in ["C#3", "c#3", "Db3", "db3"]:
        return 49
    elif noteName in ["D3", "d3"]:
        return 50
    elif noteName in ["D#3", "d#3", "Eb3", "eb3"]:
        return 51
    elif noteName in ["E3", "e3"]:
        return 52
    elif noteName in ["F3", "f3"]:
        return 53
    elif noteName in ["F#3", "f#3", "Gb3", "gb3"]:
        return 54
    elif noteName in ["G3", "g3"]:
        return 55
    elif noteName in ["G#3", "g#3", "Ab3", "ab3"]:
        return 56
    elif noteName in ["A3", "a3"]:
        return 57
    elif noteName in ["A#3", "a#3", "Bb3", "bb3"]:
        return 58
    elif noteName in ["B3", "b3"]:
        return 59
    elif noteName in ["C4", "c4"]:
        return 60
    elif noteName in ["C#4", "c#4", "Db4", "db4"]:
        return 61
    elif noteName in ["D4", "d4"]:
        return 62
    elif noteName in ["D#4", "d#4", "Eb4", "eb4"]:
        return 63
    elif noteName in ["E4", "e4"]:
        return 64
    elif noteName in ["F4", "f4"]:
        return 65
    elif noteName in ["F#4", "f#4", "Gb4", "gb4"]:
        return 66
    elif noteName in ["G4", "g4"]:
        return 67
    elif noteName in ["G#4", "g#4", "Ab4", "ab4"]:
        return 68
    elif noteName in ["A4", "a4"]:
        return 69
    elif noteName in ["A#4", "a#4", "Bb4", "bb4"]:
        return 70
    elif noteName in ["B4", "b4"]:
        return 71
    elif noteName in ["C5", "c5"]:
        return 72
    elif noteName in ["C#5", "c#5", "Db5", "db5"]:
        return 73
    elif noteName in ["D5", "d5"]:
        return 74
    elif noteName in ["D#5", "d#5", "Eb5", "eb5"]:
        return 75
    elif noteName in ["E5", "e5"]:
        return 76
    elif noteName in ["F5", "f5"]:
        return 77
    elif noteName in ["F#5", "f#5", "Gb5", "gb5"]:
        return 78
    elif noteName in ["G5", "g5"]:
        return 79
    elif noteName in ["G#5", "g#5", "Ab5", "ab5"]:
        return 80
    elif noteName in ["A5", "a5"]:
        return 81
    elif noteName in ["A#5", "a#5", "Bb5", "bb5"]:
        return 82
    elif noteName in ["B5", "b5"]:
        return 83
    elif noteName in ["C6", "c6"]:
        return 84
    elif noteName in ["C#6", "c#6", "Db6", "db6"]:
        return 85
    elif noteName in ["D6", "d6"]:
        return 86
    elif noteName in ["D#6", "d#6", "Eb6", "eb6"]:
        return 87
    elif noteName in ["E6", "e6"]:
        return 88
    elif noteName in ["F6", "f6"]:
        return 89
    elif noteName in ["F#6", "f#6", "Gb6", "gb6"]:
        return 90
    elif noteName in ["G6", "g6"]:
        return 91
    elif noteName in ["G#6", "g#6", "Ab6", "ab6"]:
        return 92
    elif noteName in ["A6", "a6"]:
        return 93
    elif noteName in ["A#6", "a#6", "Bb6", "bb6"]:
        return 94
    elif noteName in ["B6", "b6"]:
        return 95
    elif noteName in ["C7", "c7"]:
        return 96
    elif noteName in ["C#7", "c#7", "Db7", "db7"]:
        return 97
    elif noteName in ["D7", "d7"]:
        return 98
    elif noteName in ["D#7", "d#7", "Eb7", "eb7"]:
        return 99
    elif noteName in ["E7", "e7"]:
        return 100
    elif noteName in ["F7", "f7"]:
        return 101
    elif noteName in ["F#7", "f#7", "Gb7", "gb7"]:
        return 102
    elif noteName in ["G7", "g7"]:
        return 103
    elif noteName in ["G#7", "g#7", "Ab7", "ab7"]:
        return 104
    elif noteName in ["A7", "a7"]:
        return 105
    elif noteName in ["A#7", "a#7", "Bb7", "bb7"]:
        return 106
    elif noteName in ["B7", "b7"]:
        return 107
    elif noteName in ["C8", "c8"]:
        return 108
    else:
        raise ValueError("Invalid note name")
