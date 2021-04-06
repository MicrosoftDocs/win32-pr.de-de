---
description: Die Struktur der Datei \_ System \_ Erkennungs \_ Struktur, die intern von Windows definiert und von der Dateisystem Erkennung (File System RECOGNITION, FRS) verwendet wird, enthält einen Prüfsummen Wert, der ordnungsgemäß berechnet werden muss, damit FRS ordnungsgemäß mit einem angegebenen nicht erkannten Dateisystem funktioniert.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Berechnen einer Prüfsumme für die Datei System Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cac3975d4e1845dd1ff4aa218526e942fda152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960934"
---
# <a name="computing-a-file-system-recognition-checksum"></a>Berechnen einer Prüfsumme für die Datei System Erkennung

Die Struktur der [**Datei \_ System \_ Erkennungs \_ Struktur**](file-system-recognition-structure.md) , die intern von Windows definiert und von der [Dateisystem Erkennung (File System RECOGNITION](file-system-recognition.md) , FRS) verwendet wird, enthält einen Prüfsummen Wert, der ordnungsgemäß berechnet werden muss, damit FRS ordnungsgemäß mit einem angegebenen nicht erkannten Dateisystem funktioniert. Im folgenden Beispiel wird diese Berechnung durchgeführt.


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE, *PFILE_SYSTEM_RECOGNITION_STRUCTURE;

USHORT ComputeFileSystemInformationChecksum (
    __in PFILE_SYSTEM_RECOGNITION_STRUCTURE Fsrs
    )

/*++

Routine Description:

    This routine computes the file record checksum.

Arguments:

    Fsrs - Pointer to the record.

Return Value:

    The checksum result.

--*/

{
    USHORT Checksum = 0;
    USHORT i;
    PUCHAR Buffer = (PUCHAR)Fsrs;
    USHORT StartOffset;

    //
    //  Skip the jump instruction
    //

    StartOffset = FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, FsName);
    
    for (i = StartOffset; i < Fsrs->Length; i++) {

        //
        //  Skip the checksum field itself, which is a USHORT.
        //

        if ((i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)) ||
            (i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)+1)) {

            continue;
        }

        Checksum = ((Checksum & 1) ? 0x8000 : 0) + (Checksum >> 1) + Buffer[i];
    }

    return Checksum;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datei System Erkennung](file-system-recognition.md)
</dt> <dt>

[**Datei \_ System- \_ Erkennungs \_ Struktur**](file-system-recognition-structure.md)
</dt> </dl>

 

 



