---
description: Die FILE SYSTEM RECOGNITION STRUCTURE-Struktur, die intern von Windows definiert und von der Dateisystemerkennung \_ (File System \_ Recognition, FRS) verwendet wird, enthält einen Prüfsummenwert, der ordnungsgemäß berechnet werden muss, damit FRS ordnungsgemäß mit einem angegebenen unbekannten Dateisystem \_ funktioniert.
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Berechnen einer Prüfsumme für die Dateisystemerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce146fda589668d39f1f7ff4158384986fb719f2bbbee6ce0584ad9f1e540b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329180"
---
# <a name="computing-a-file-system-recognition-checksum"></a>Berechnen einer Prüfsumme für die Dateisystemerkennung

Die [**FILE SYSTEM RECOGNITION \_ \_ \_ STRUCTURE-Struktur,**](file-system-recognition-structure.md) die intern von Windows definiert und von der Dateisystemerkennung (File System [Recognition,](file-system-recognition.md) FRS) verwendet wird, enthält einen Prüfsummenwert, der ordnungsgemäß berechnet werden muss, damit FRS ordnungsgemäß mit einem angegebenen nicht ermittelten Dateisystem funktioniert. Im folgenden Beispiel wird diese Berechnung durchgeführt.


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

[Dateisystemerkennung](file-system-recognition.md)
</dt> <dt>

[**\_ \_ \_ DATEISYSTEMERKENNUNGSSTRUKTUR**](file-system-recognition-structure.md)
</dt> </dl>

 

 



