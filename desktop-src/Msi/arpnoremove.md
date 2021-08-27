---
description: Durch Festlegen der ARPNOREMOVE-Eigenschaft wird die Funktion "Programme hinzufügen" oder "Software entfernen" in Systemsteuerung, die das Produkt entfernt.
ms.assetid: f86c1af8-c984-4075-9c6b-0a71000b01a1
title: ARPNOREMOVE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d69e066aeb96861be220a40334d44bf55fe0569e855029d2a19399b56a1c205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105430"
---
# <a name="arpnoremove-property"></a>ARPNOREMOVE-Eigenschaft

Durch Festlegen **der ARPNOREMOVE-Eigenschaft** wird die Funktion "Programme hinzufügen" oder "Software entfernen" **in** Systemsteuerung die das Produkt entfernt.  Für Windows 2000 deaktiviert **dies**  die Schaltfläche Entfernen für das Produkt aus der Option Programme hinzufügen oder entfernen in **Systemsteuerung.** Bei früheren Betriebssystemen hat **dies** den Effekt, dass das Produkt aus der Liste der installierten Produkte auf der Seite Programme hinzufügen oder entfernen **in** Systemsteuerung.

Wenn die **ARPNOREMOVE-Eigenschaft** festgelegt ist, schreibt die [RegisterProduct-Aktion](registerproduct-action.md) den Wert "NoRemove" unter den Registrierungsschlüssel:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **{*Product Key*}**

Das Festlegen **der ARPNOREMOVE-Eigenschaft** verhindert, dass der UninstallString-Wert unter diesem Schlüssel geschrieben wird. Der UnidirektionString-Wert ist eine Befehlszeile zum Entfernen des Produkts, anstatt das Produkt neu zu konfigurieren.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann beispielsweise während einer Anpassungstransformation festgelegt werden, um zu verhindern, dass Benutzer eine Administratoranpassung entfernen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 oder höher auf Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




