---
description: Wenn Sie die Eigenschaft ARPNOMODIFY festlegen, wird die Funktion "Software" in Systemsteuerung deaktiviert, die das Produkt ändert.
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: ARPNOMODIFY-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c9a097f183c13e1c5b6f8f8b6a521c8a03149df130befaa1221b14b732418a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581810"
---
# <a name="arpnomodify-property"></a>ARPNOMODIFY-Eigenschaft

Durch Festlegen der **ARPNOMODIFY-Eigenschaft** wird die Funktion "Software" in Systemsteuerung deaktiviert, die das Produkt ändert. Für Windows 2000 deaktiviert dies die Schaltfläche **Ändern** für das Produkt in **Software in** **Systemsteuerung**. Wenn Sie unter früheren Betriebssystemen auf die Schaltfläche **Software** klicken, wird das Produkt deinstalliert, anstatt in den Wartungsmodus-Assistenten zu wechseln.

Wenn die **ARPNOMODIFY-Eigenschaft** festgelegt ist, schreibt die [RegisterProduct-Aktion](registerproduct-action.md) den Wert "NoModify" unter den Registrierungsschlüssel:

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Deinstallieren** \\ **{*Product Key*}**

Wenn die **ARPNOMODIFY-Eigenschaft** festgelegt ist und die [**ARPNOREMOVE-Eigenschaft**](arpnoremove.md) nicht festgelegt ist, schreibt die RegisterProduct-Aktion auch den UninstallString-Wert unter diesen Schlüssel. Der UniierungString-Wert ist eine Befehlszeile zum Entfernen des Produkts, anstatt das Produkt neu zu konfigurieren.

## <a name="remarks"></a>Hinweise

Am Windows 2000 deaktiviert dies die Schaltfläche **Ändern** für das Produkt im  **Systemsteuerung Programme hinzufügen oder entfernen.**

Diese Eigenschaft kann durch eine Anpassungstransformation festgelegt werden, um zu verhindern, dass Benutzer die Anpassung eines Administrators durch **Hinzufügen oder Entfernen von Programmen** ändern. Diese Eigenschaft wirkt sich nur auf **Software aus.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Beispiel für eine Anpassungstransformation](a-customization-transform-example.md)
</dt> </dl>

 

 




