---
description: Das Installationsprogramm legt den Wert der Eigenschaft primaryvolumespaceremaineing auf eine Zeichenfolge fest, die die Gesamtzahl der verbleibenden Bytes auf dem Volume darstellt, auf das von der Eigenschaft primaryvolumepath verwiesen wird, wenn alle derzeit ausgewählten Funktionen installiert wurden.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Primaryvolumespaceremaineing (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352165"
---
# <a name="primaryvolumespaceremaining-property"></a>Primaryvolumespaceremaineing (Eigenschaft)

Das Installationsprogramm legt den Wert der Eigenschaft **primaryvolumespaceremaineing** auf eine Zeichenfolge fest, die die Gesamtzahl der verbleibenden Bytes auf dem Volume darstellt, auf das von der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verwiesen wird, wenn alle derzeit ausgewählten Funktionen installiert wurden. Wie bei der [**primaryvolumespaceavailable**](primaryvolumespaceavailable.md) -Eigenschaft wird diese Zahl in Einheiten von 512 Byte angegeben.

## <a name="remarks"></a>Bemerkungen

Hinweis Wenn dieser Wert in einem statischen [Text Steuer](text-control.md)Element angezeigt werden soll, kann das [formatsize](formatsize-control-attribute.md) -Bit verwendet werden, um diese Zahl nach Bedarf automatisch in Kilobyte oder Megabyte zu formatieren und zu bezeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




