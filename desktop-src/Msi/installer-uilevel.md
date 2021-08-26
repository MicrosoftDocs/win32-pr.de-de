---
description: Die UILevel-Eigenschaft des Installer-Objekts ist eine Eigenschaft mit Lese-/Schreibzugriff, die den Typ der Benutzeroberfläche angibt, die beim Öffnen und Verarbeiten nachfolgender Pakete im aktuellen Prozessbereich verwendet werden soll.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Installer.UILevel(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3004675ee8e07c3503ec4442832c00975364066fa4a0c770b0b081fc7b64c3c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043570"
---
# <a name="installeruilevel-property"></a>Installer.UILevel(Eigenschaft)

Die **UILevel-Eigenschaft** des [**Installer-Objekts**](installer-object.md) ist eine Eigenschaft mit Lese-/Schreibzugriff, die den Typ der Benutzeroberfläche angibt, die beim Öffnen und Verarbeiten nachfolgender Pakete im aktuellen Prozessbereich verwendet werden soll.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise



| Benutzeroberflächenebene   | Wert | Beschreibung                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiUILevelNoChange     | 0     | Ändert die Benutzeroberflächenebene nicht.                                                                                                                                                                          |
| msiUILevelDefault      | 1     | Verwendet die Standardbenutzeroberflächenebene.                                                                                                                                                                             |
| msiUILevelNone         | 2     | Automatische Installation.                                                                                                                                                                               |
| msiUILevelBasic        | 3     | Einfacher Fortschritt und Fehlerbehandlung.                                                                                                                                                                |
| msiUILevelReduced      | 4     | Die Erstellten Benutzeroberflächen- und Assistentendialogfelder werden unterdrückt.                                                                                                                                                    |
| msiUILevelFull         | 5     | Benutzeroberfläche mit Assistenten, Fortschritt und Fehlern erstellt.                                                                                                                                                    |
| msiUILevelHideCancel   | 32    | In Kombination mit dem Wert msiUILevelBasic zeigt das Installationsprogramm  Statusdialogfelder an, aber keine Schaltfläche Abbrechen im Dialogfeld, um zu verhindern, dass Benutzer die Installation abbrechen. |
| msiUILevelProgressOnly | 64    | In Kombination mit dem Wert msiUILevelBasic zeigt das Installationsprogramm Statusdialogfelder an, aber keine modalen Dialogfelder oder Fehlerdialogfelder.                                        |
| msiUILevelEndDialog    | 128   | In Kombination mit einem der oben genannten Werte zeigt das Installationsprogramm ein modales Dialogfeld am Ende einer erfolgreichen Installation an, oder wenn ein Fehler aufgetreten ist. Wenn der Benutzer den Vorgang abbricht, wird kein Dialogfeld angezeigt. |



 

Siehe auch Determining UI Level from a Custom Action (Bestimmen [der Benutzeroberflächenebene aus einer benutzerdefinierten Aktion).](determining-ui-level-from-a-custom-action.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



 

 




