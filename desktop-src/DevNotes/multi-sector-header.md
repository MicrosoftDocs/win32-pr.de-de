---
description: Stellt den multisektorheader dar.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: MULTI_SECTOR_HEADER Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747881"
---
# <a name="multi_sector_header-structure"></a>\_Multisektor- \_ Header Struktur

\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt den multisektorheader dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**Signature**
</dt> <dd>

Die Signatur. Dieser Wert ist für den Benutzer benutzerfreundlicher.

</dd> <dt>

**Updatesequencearrayoffset**
</dt> <dd>

Der Offset des Update Sequenz Arrays vom Anfang dieser-Struktur. Das Update Sequenz Array muss vor dem letzten ushort-Wert des ersten Sektors enden.

</dd> <dt>

**Updatesequencearraysize**
</dt> <dd>

Die Größe des Update Sequenz Arrays in Bytes.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.

Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.

Der multisektorheader und das Update Sequenz Array ermöglichen die Erkennung unvollständiger multisektorübertragungen für Geräte, die eine physische Sektorgröße aufweisen, die größer oder gleich der Sequenznummer Stride (512) ist, oder die keine Sektoren außerhalb der Reihenfolge übertragen. Wenn ein Gerät vorhanden ist, dessen Sektorgröße kleiner ist als die Sequenznummer, und in einigen Fällen Sektoren außerhalb der Reihenfolge übermittelt werden, bietet das Update Sequenz Array keine absolute Erkennung unvollständiger Übertragungen. Die Sequenznummer Stride wird auf eine kleine Zahl festgelegt, um den absoluten Schutz für alle bekannten Festplatten bereitzustellen. Der Wert ist nicht kleiner, oder es kann zu einer übermäßigen Laufzeit oder mehr Aufwand kommen.

Das Update Sequenz Array besteht aus einem Array von *n* **UShort** -Werten, wobei *n* die Größe der geschützten Struktur ist, dividiert durch die Sequenznummer Stride. Das erste Wort enthält die Aktualisierungs Sequenznummer, bei der es sich um einen zyklischen gegen Wert handelt, mit dem die Anzahl der in die enthaltenden Struktur auf den Datenträger geschrieben wurde. Im nächsten Schritt werden die *n* gespeicherten **UShort** -Werte, die von der Update Sequenznummer beim letzten Schreiben der enthaltenden Struktur auf den Datenträger überschrieben wurden, überschrieben.

Jedes Mal, wenn die geschützte Struktur in den Datenträger geschrieben wird, wird das letzte Wort in jeder Sequenznummern Sequenz an der jeweiligen Position im Sequenznummern Array gespeichert und mit der nächsten Update Sequenznummer überschrieben. Nach dem Schreiben oder immer dann, wenn die Struktur gelesen wird, wird das gespeicherte Wort aus dem Sequenznummern Array an seine tatsächliche Position in der Struktur wieder hergestellt. Vor dem Wiederherstellen der gespeicherten Wörter bei Lesevorgängen werden alle Sequenznummern am Ende jedes Stride mit der tatsächlichen Sequenznummer am Anfang des Arrays verglichen. Wenn einer dieser Vergleiche nicht gleich ist, wurde eine fehlgeschlagene multisektorübertragung erkannt.

Die Größe des Arrays wird durch die Größe der enthaltenden Struktur bestimmt. Das Update Sequenz Array sollte am Ende des Headers der Struktur eingeschlossen werden, die er aufgrund seiner Variablen Größe schützt. Der Benutzer muss sicherstellen, dass der richtige Speicherplatz für die enthaltende Struktur reserviert ist: (Größe von Structure/512 + 1) \* sizeof (UShort).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Master Dateitabelle](master-file-table.md)
</dt> </dl>

 

 
