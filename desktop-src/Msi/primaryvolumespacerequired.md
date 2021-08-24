---
description: Das Installationsprogramm legt den Wert der PrimaryVolumeSpaceRequired-Eigenschaft auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle ausgewählten Features auf dem Volume erforderlich sind, auf das von der PrimaryVolumePath-Eigenschaft verwiesen wird.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: PrimaryVolumeSpaceRequired-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c644c53b5a36c8ba834a52c22ca3ba2b192499cbf351f122d8ed2b6a66a57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042260"
---
# <a name="primaryvolumespacerequired-property"></a>PrimaryVolumeSpaceRequired-Eigenschaft

Das Installationsprogramm legt den Wert der **PrimaryVolumeSpaceRequired-Eigenschaft** auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle ausgewählten Features auf dem Volume erforderlich sind, auf das von der [**PrimaryVolumePath-Eigenschaft**](primaryvolumepath.md) verwiesen wird. Wie bei der [**PrimaryVolumeSpaceAvailable-Eigenschaft**](primaryvolumespaceavailable.md) wird diese Zahl in Einheiten von 512 Bytes ausgedrückt.

## <a name="remarks"></a>Hinweise

Wenn dieser Wert in einem statischen [Textsteuerelement](text-control.md)angezeigt werden soll, kann das [FormatSize-Bit](formatsize-control-attribute.md) verwendet werden, um diese Zahl automatisch in Kilobyte- oder Megabyteeinheiten zu formatieren und zu bezeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installationsprogramm 4.0 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




