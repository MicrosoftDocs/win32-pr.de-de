---
description: Die msiarpsettingsidentifier-Eigenschaft enthält eine durch Semikolons getrennte Liste der Registrierungs Speicherorte, an denen die Anwendung die Einstellungen und Einstellungen des Benutzers speichert.
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: Msiarpsettingsidentifier (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360976"
---
# <a name="msiarpsettingsidentifier-property"></a>Msiarpsettingsidentifier (Eigenschaft)

Die **msiarpsettingsidentifier** -Eigenschaft enthält eine durch Semikolons getrennte Liste der Registrierungs Speicherorte, an denen die Anwendung die Einstellungen und Einstellungen des Benutzers speichert. Während eines Upgrades des Betriebssystems kann das Setup diese Informationen verwenden, um die Benutzeroberflächen zu verbessern, die Anwendungen migrieren.

Der Wert der Eigenschaft **msiarpsettingsidentifier** ist Literaltext, der die Liste der Registrierungs Orte enthält, in denen die Anwendung die Einstellungen speichert. Der Wert kann mehrere mögliche Registrierungs Speicherorte angeben. Trennen Sie mehrere Registrierungs Speicherorte mithilfe von Semikolons. Anwendungseinstellungen werden in der Regel in den **HKCU** -oder **HKLM** -Registrierungs Strukturen in der Form gespeichert: *Unternehmens \\ Anwendungs \\ Version*. Das folgende Beispiel ist ein möglicher Wert für die **msiarpsettingsidentifier** -Eigenschaft.

*MyCompany \\ appsuite \\ 1,0; MyCompany \\ App1 \\ 1,0; MyCompany \\ App2 \\ 1,0*

Diese Eigenschaft ist optional und kann in der [Eigenschaften](property-table.md) Tabelle festgelegt werden. Wenn diese Eigenschaft in der Eigenschaften Tabelle angezeigt wird, darf der Wert nicht auf **null** festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




