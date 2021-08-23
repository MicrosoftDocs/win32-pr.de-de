---
description: Das Installationsprogramm legt den Wert der PrimaryVolumeSpaceAvailable-Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der verfügbaren Bytes in Einheiten von 512 auf dem Volume darstellt, auf das von der PrimaryVolumePath-Eigenschaft verwiesen wird.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: PrimaryVolumeSpaceAvailable-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9336bfa32ebb3bf0c12b7e7fc54ddad2b26cd635c820ca6e8ea2caabe163ceb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580670"
---
# <a name="primaryvolumespaceavailable-property"></a>PrimaryVolumeSpaceAvailable-Eigenschaft

Das Installationsprogramm legt den Wert der **PrimaryVolumeSpaceAvailable-Eigenschaft** auf eine Zeichenfolge fest, die die Gesamtzahl der verfügbaren Bytes in Einheiten von 512 auf dem Volume darstellt, auf das von der [**PrimaryVolumePath-Eigenschaft**](primaryvolumepath.md) verwiesen wird.

## <a name="remarks"></a>Hinweise

Wenn [**PrimaryVolumePath**](primaryvolumepath.md) beispielsweise auf "D:" festgelegt ist und Volume D: 446.134.272 Bytes frei hat, wird **PrimaryVolumeSpaceAvailable** auf 871356 festgelegt.

Wenn dieser Wert in einem statischen [Textsteuerelement](text-control.md)angezeigt werden soll, kann das [FormatSize-Bit](formatsize-control-attribute.md) verwendet werden, um diese Zahl automatisch in Kilobyte- oder Megabyteeinheiten zu formatieren und zu bezeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




