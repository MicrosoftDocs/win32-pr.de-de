---
description: Das Installationsprogramm legt den Wert der Eigenschaft primaryvolumespacerequired auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle ausgewählten Funktionen auf dem Volume erforderlich sind, auf das von der Eigenschaft primaryvolumepath verwiesen wird.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Primaryvolumespacerequired (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364494"
---
# <a name="primaryvolumespacerequired-property"></a>Primaryvolumespacerequired (Eigenschaft)

Das Installationsprogramm legt den Wert der Eigenschaft **primaryvolumespacerequired** auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle ausgewählten Funktionen auf dem Volume erforderlich sind, auf das von der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verwiesen wird. Wie bei der [**primaryvolumespaceavailable**](primaryvolumespaceavailable.md) -Eigenschaft wird diese Zahl in Einheiten von 512 Byte angegeben.

## <a name="remarks"></a>Bemerkungen

Hinweis Wenn dieser Wert in einem statischen [Text Steuer](text-control.md)Element angezeigt werden soll, kann das [formatsize](formatsize-control-attribute.md) -Bit verwendet werden, um diese Zahl nach Bedarf automatisch in Kilobyte oder Megabyte zu formatieren und zu bezeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




