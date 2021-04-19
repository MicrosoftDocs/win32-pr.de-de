---
description: Wenn Sie die Eigenschaft arpnomodify festlegen, werden die Funktionen zum Hinzufügen oder Entfernen von Programmen in der Systemsteuerung deaktiviert, die das Produkt ändert.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: Arpnomodify (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356480"
---
# <a name="arpnomodify-property"></a>Arpnomodify (Eigenschaft)

Wenn Sie die Eigenschaft **arpnomodify** festlegen, werden die Funktionen zum Hinzufügen oder Entfernen von Programmen in der Systemsteuerung deaktiviert, die das Produkt ändert. Bei Windows 2000 wird die Schaltfläche **ändern** für das **Produkt in der** **Systemsteuerung** unter Software deaktiviert. Unter älteren Betriebssystemen wird durch Klicken auf die Schaltfläche "Software **" das Produkt** deinstalliert, anstatt in den Wartungsmodus-Assistenten zu wechseln.

Wenn die **arpnomodify** -Eigenschaft festgelegt ist, schreibt die [registerproduct-Aktion](registerproduct-action.md) den Wert "nomodify" unter den folgenden Registrierungsschlüssel:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **{*Product Key*}**

Wenn die **arpnomodify** -Eigenschaft festgelegt ist und die [**ARPNOREMOVE**](arpnoremove.md) -Eigenschaft nicht festgelegt ist, wird von der registerproduct-Aktion auch der UninstallString-Wert unter diesem Schlüssel geschrieben. Der unistallstring-Wert ist eine Befehlszeile zum Entfernen des Produkts, anstatt das Produkt neu zu konfigurieren.

## <a name="remarks"></a>Bemerkungen

Unter Windows 2000 wird dadurch die Schaltfläche **ändern** für das Produkt in den **Programmen** Software der **Systemsteuerung** deaktiviert.

Diese Eigenschaft kann durch eine Anpassungs Transformation festgelegt werden, um zu verhindern, dass Benutzer die Anpassung eines **Administrators über "** Software" ändern. Diese Eigenschaft wirkt sich nur auf die Option **Programme hinzufügen oder entfernen**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Beispiel für eine Anpassungs Transformation](a-customization-transform-example.md)
</dt> </dl>

 

 




