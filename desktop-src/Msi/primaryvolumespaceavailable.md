---
description: Das Installationsprogramm legt den Wert der Eigenschaft primaryvolumespaceavailable auf eine Zeichenfolge fest, die die Gesamtzahl der verfügbaren Bytes in Einheiten von 512 auf dem Volume darstellt, auf das von der Eigenschaft primaryvolumepath verwiesen wird.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Primaryvolumespaceavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364695"
---
# <a name="primaryvolumespaceavailable-property"></a>Primaryvolumespaceavailable (Eigenschaft)

Das Installationsprogramm legt den Wert der Eigenschaft **primaryvolumespaceavailable** auf eine Zeichenfolge fest, die die Gesamtzahl der verfügbaren Bytes in Einheiten von 512 auf dem Volume darstellt, auf das von der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verwiesen wird.

## <a name="remarks"></a>Bemerkungen

Wenn [**primaryvolumepath**](primaryvolumepath.md) z. b. auf "D:" festgelegt ist und Volume D: 446.134.272 Bytes frei ist, wird **primaryvolumespaceavailable** auf 871356 festgelegt.

Hinweis Wenn dieser Wert in einem statischen [Text Steuer](text-control.md)Element angezeigt werden soll, kann das [formatsize](formatsize-control-attribute.md) -Bit verwendet werden, um diese Zahl nach Bedarf automatisch in Kilobyte oder Megabyte zu formatieren und zu bezeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




