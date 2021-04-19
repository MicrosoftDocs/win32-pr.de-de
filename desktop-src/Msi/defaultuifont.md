---
description: Die defaultuifont-Eigenschaft legt den für Steuerelemente verwendeten Standard Schriftstil fest. Um die Standardeinstellung anzugeben, legen Sie defaultuifont auf eines der vordefinierten Stile in der Tabelle "TextStyle" in der Eigenschaften Tabelle fest.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Defaultuifont (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372783"
---
# <a name="defaultuifont-property"></a>Defaultuifont (Eigenschaft)

Die **defaultuifont** -Eigenschaft legt den für Steuerelemente verwendeten Standard Schriftstil fest. Um die Standardeinstellung anzugeben, legen Sie **defaultuifont** auf eines der vordefinierten Stile in der [Tabelle "TextStyle](textstyle-table.md) " in der [Eigenschaften Tabelle](property-table.md)fest.

## <a name="remarks"></a>Bemerkungen

Die **defaultuifont** -Eigenschaft jedes Installationspakets mit einer Benutzeroberfläche sollte in der [Eigenschaften Tabelle](property-table.md) auf einen der vordefinierten Stile in der [TextStyle-Tabelle](textstyle-table.md)festgelegt werden. Wenn diese Eigenschaft nicht angegeben wird, verwendet das Installationsprogramm die System Schriftart. Dies kann dazu führen, dass das Installationsprogramm Text Zeichenfolgen nicht ordnungsgemäß anzeigt, wenn sich die Codepage des Pakets von der standardmäßigen UI-Codepage des Benutzers unterscheidet.

Der Text und der Schrift Schnitt eines Steuer Elements können wie unter [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md)beschrieben festgelegt werden. Wenn die Zeichenfolge, die in der Text-Spalte der [Steuerelement Tabelle](control-table.md) oder der Tabelle " [bbcontrol](bbcontrol-table.md) " aufgeführt ist, den Schrift Schnitt nicht angibt, verwendet das Steuerelement den Wert der **defaultuifont** -Eigenschaft als Schriftart Stil.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




