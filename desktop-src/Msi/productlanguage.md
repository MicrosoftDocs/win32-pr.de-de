---
description: Die productlanguage-Eigenschaft gibt die Sprache an, die vom Installer für alle Zeichen folgen in der Benutzeroberfläche verwendet werden soll, die nicht in der Datenbank erstellt werden.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Productlanguage-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352037"
---
# <a name="productlanguage-property"></a>Productlanguage-Eigenschaft

Die **productlanguage** -Eigenschaft gibt die Sprache an, die vom Installer für alle Zeichen folgen in der Benutzeroberfläche verwendet werden soll, die nicht in der Datenbank erstellt werden. Diese Eigenschaft muss eine numerische sprach Kennung (langid) sein. Wenn eine Transformation die Sprache der Benutzeroberfläche in der Datenbank ändert, sollte Sie auch den Wert dieser Eigenschaft ändern, um die neue Sprache widerzuspiegeln.

Diese Eigenschaft ist erforderlich.

## <a name="remarks"></a>Bemerkungen

Der Wert der **productlanguage** -Eigenschaft muss eine der in der [**Template Summary**](template-summary.md) -Eigenschaft aufgelisteten Sprachen sein.

Wenn Sie ein Paket als sprachneutral erstellen, legen Sie die **productlanguage** -Eigenschaft auf 0 fest, und verwenden Sie die Schriftart der MS Shell Dlg als Textstil für alle erstellten Dialoge. Da einige Schriftarten nicht alle Zeichensätze unterstützen, können Sie mithilfe dieser Schriftart sicherstellen, dass der Text in allen lokalisierten Versionen des Betriebssystems ordnungsgemäß angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




