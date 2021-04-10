---
description: Enthält die Informationen auf dem Datenträger, die im Startsektor für Volumes gespeichert sind (logischer Datenträger Sektor null).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: FILE_SYSTEM_RECOGNITION_STRUCTURE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042021"
---
# <a name="file_system_recognition_structure-structure"></a>Struktur der Datei \_ System \_ Erkennungs \_ Struktur

Enthält die Informationen auf dem Datenträger, die im Startsektor des Volumes gespeichert sind (logischer Datenträger Sektor null).

Dabei handelt es sich um eine intern definierte Datenstruktur, die nicht in einem öffentlichen Header verfügbar ist und hier für Dateisystem Entwickler bereitgestellt wird, die die Dateisystem Erkennung nutzen möchten. Weitere Informationen finden Sie unter [Datei System Erkennung](file-system-recognition.md).

## <a name="syntax"></a>Syntax


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a>Member

<dl> <dt>

**"Jmp"**
</dt> <dd>

Die jmp-Anweisung. Dieser Datenmember ist nicht in dem Wert enthalten, der im **Prüfsummen** Datenmember enthalten ist.

</dd> <dt>

**FSName**
</dt> <dd>

Der Name des Dateisystems. Dabei handelt es sich um eine Sequenz von 8 ASCII-Zeichen, die den nicht lokalisierbaren lesbaren Namen des Dateisystems darstellt, mit dem das Volume formatiert ist.

Diese Zeichenfolge befindet sich am gleichen Speicherort wie der OEM-Dateisystem Name auf einem Datenträger mit einer normalen BPB-Struktur (BIOS Parameter Block).

</dd> <dt>

**Mustbezero**
</dt> <dd>

Reservierter Speicherplatz, der alle Nullen enthält.

Dieser Datenmember überlappt, was normalerweise die folgenden Datenmember in einer BPB sind:

-   **Bytespersektor**
-   **Sector-Cluster**
-   **Reservedsector count**

Da diese Datenmember auf 0 (null) festgelegt sind, sollte dies ausreichen, um zu bewirken, dass frühere Betriebssysteme den Schluss haben, dass es sich nicht um ein gültiges BPB handelt und daher das Volume erkannt

</dd> <dt>

**Bezeichner**
</dt> <dd>

Ein Strukturbezeichner. Muss den in Little-Endian-Byte Reihenfolge angeordneten Wert 0x53525346 enthalten.

An dieser Stelle in der Struktur werden die Daten auf 16 Bytes ausgerichtet.

</dd> <dt>

**Länge**
</dt> <dd>

Die Anzahl der Bytes in dieser-Struktur von Anfang bis Ende, einschließlich des **jmp** -Datenelements.

</dd> <dt>

**Prüfsumme**
</dt> <dd>

Eine 2-Byte-Prüfsumme, die über die Bytes beginnend mit dem **FSName** -Datenmember berechnet wird und mit dem letzten Byte dieser Struktur endet, ausgenommen der **jmp** -und **Prüfsumme** -Datenmember.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Berechnen einer Prüfsumme für die Datei System Erkennung](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[Datei System Erkennung](file-system-recognition.md)
</dt> <dt>

[**Informationen zur Datei \_ System \_ Erkennung \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[**FSCTL- \_ Abfrage \_ Datei \_ System \_ Erkennung**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

