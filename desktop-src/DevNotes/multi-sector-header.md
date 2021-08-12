---
description: Stellt den Multisectorheader dar.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: MULTI_SECTOR_HEADER-Struktur
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
ms.openlocfilehash: 9e34e23d3d2bf2ecfbc1c668e02c177e4d1516c73acabccc88aa7190ec33e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667217"
---
# <a name="multi_sector_header-structure"></a>MULTI \_ SECTOR \_ HEADER-Struktur

\[Diese Struktur ist nur für Version 3 von NTFS-Volumes gültig. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt den Multisectorheader dar.

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

Die Signatur. Dieser Wert ist für den Benutzer praktisch.

</dd> <dt>

**UpdateSequenceArrayOffset**
</dt> <dd>

Der Offset zum Updatesequenzarray vom Anfang dieser Struktur. Das Updatesequenzarray muss vor dem letzten USHORT-Wert im ersten Sektor enden.

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

Die Größe des Updatesequenzarrays in Bytes.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass für diese Struktur keine Headerdatei zugeordnet ist.

Diese Strukturdefinition ist nur für Hauptversion 3 und Nebenversion 0 oder 1 gültig, wie von [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)gemeldet.

Der Multisectorheader und das Updatesequenzarray ermöglichen die Erkennung unvollständiger Multisectorübertragungen für Geräte, die entweder eine physische Sektorgröße aufweisen, die größer oder gleich dem Sequenznummernschritt (512) ist oder die keine Sektoren in die andere Reihenfolge übertragen. Wenn ein Gerät vorhanden ist, das eine Sektorgröße aufweist, die kleiner ist als die Sequenznummernschritte, und es manchmal Sektoren außerhalb der Reihenfolge überträgt, bietet das Updatesequenzarray keine absolute Erkennung unvollständiger Übertragungen. Der Schritt der Sequenznummer ist auf eine kleine Zahl festgelegt, um absoluten Schutz für alle bekannten Festplatten bereitzustellen. Sie ist nicht kleiner festgelegt, oder es kann zu übermäßigem Laufzeit- oder Speicherplatzaufwand kommen.

Das Updatesequenzarray besteht aus einem Array von *n* **USHORT-Werten,** wobei *n* die Größe der geschützten Struktur dividiert durch den Sequenznummernschritt ist. Das erste Wort enthält die Updatesequenznummer. Dies ist ein zyklischer Zähler, der angibt, wie oft die enthaltende Struktur auf den Datenträger geschrieben wurde. Als Nächstes folgen die *n* gespeicherten **USHORT-Werte,** die beim letzten Schreiben der enthaltenden Struktur auf den Datenträger durch die Updatesequenznummer überschrieben wurden.

Jedes Mal, wenn die geschützte Struktur auf den Datenträger geschrieben wird, wird das letzte Wort in jedem Sequenznummernschritt an der entsprechenden Position im Sequenznummernarray gespeichert und mit der nächsten Updatesequenznummer überschrieben. Nach dem Schreiben oder beim Lesen der Struktur wird das gespeicherte Wort aus dem Sequenznummernarray an seiner tatsächlichen Position in der Struktur wiederhergestellt. Vor dem Wiederherstellen der gespeicherten Wörter bei Leseläufen werden alle Sequenznummern am Ende jedes Schritts mit der tatsächlichen Sequenznummer am Anfang des Arrays verglichen. Wenn einer dieser Vergleiche nicht gleich ist, wurde eine fehlgeschlagene Multisectorübertragung erkannt.

Die Größe des Arrays wird durch die Größe der enthaltenden Struktur bestimmt. Das Updatesequenzarray sollte am Ende des Headers der Struktur enthalten sein, die aufgrund seiner Variablengröße geschützt wird. Der Benutzer muss sicherstellen, dass der richtige Speicherplatz für die enthaltende Struktur reserviert ist: (Größe der Struktur / 512 + 1) \* sizeof(USHORT).

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Masterdateitabelle](master-file-table.md)
</dt> </dl>

 

 
