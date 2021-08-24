---
description: Das Installationsprogramm legt den Wert der PrimaryVolumeSpaceRemaining-Eigenschaft auf eine Zeichenfolge fest, die die Gesamtanzahl von Bytes darstellt, die auf dem Volume verbleibt, auf das von der PrimaryVolumePath-Eigenschaft verwiesen wird, wenn alle derzeit ausgewählten Features installiert wurden.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: PrimaryVolumeSpaceRemaining (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16107af105de0684bd917177050017a3c14e40aff32c658881342a90e877c973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580490"
---
# <a name="primaryvolumespaceremaining-property"></a>PrimaryVolumeSpaceRemaining (Eigenschaft)

Das Installationsprogramm legt den Wert der **PrimaryVolumeSpaceRemaining-Eigenschaft** auf eine Zeichenfolge fest, die die Gesamtanzahl von Bytes darstellt, die auf dem Volume verbleibt, auf das von der [**PrimaryVolumePath-Eigenschaft**](primaryvolumepath.md) verwiesen wird, wenn alle derzeit ausgewählten Features installiert wurden. Wie bei der [**PrimaryVolumeSpaceAvailable-Eigenschaft**](primaryvolumespaceavailable.md) wird diese Zahl in Einheiten von 512 Bytes ausgedrückt.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass, wenn dieser Wert in einem statischen [Text-Steuerelement](text-control.md)angezeigt werden soll, das [FormatSize-Bit](formatsize-control-attribute.md) verwendet werden kann, um diese Zahl automatisch in Kilobyte- oder Megabyte-Einheiten zu formatieren und entsprechend zu beschriften.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




