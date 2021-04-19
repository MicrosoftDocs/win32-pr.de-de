---
description: Die uilevel-Eigenschaft des Installer-Objekts ist eine Lese-/Schreibeigenschaft, die den Typ der zu verwendenden Benutzeroberfläche angibt, wenn nachfolgende Pakete im aktuellen Prozessbereich geöffnet und verarbeitet werden.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Installer. uilevel-Eigenschaft
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
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362142"
---
# <a name="installeruilevel-property"></a>Installer. uilevel-Eigenschaft

Die **uilevel** -Eigenschaft des [**Installer**](installer-object.md) -Objekts ist eine Lese-/Schreibeigenschaft, die den Typ der zu verwendenden Benutzeroberfläche angibt, wenn nachfolgende Pakete im aktuellen Prozessbereich geöffnet und verarbeitet werden.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen



| Benutzeroberflächen Ebene   | Wert | BESCHREIBUNG                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msiuilevelnochange     | 0     | Ändert die Benutzeroberflächen Ebene nicht.                                                                                                                                                                          |
| msiuileveldefault      | 1     | Verwendet die standardmäßige Benutzeroberflächen Ebene.                                                                                                                                                                             |
| msiuilevelnone         | 2     | Automatische Installation.                                                                                                                                                                               |
| msiuilevelbasic        | 3     | Einfacher Fortschritt und Fehlerbehandlung.                                                                                                                                                                |
| msiuilevelreduced      | 4     | Die Benutzeroberfläche und die Dialogfelder der Assistenten wurden unterdrückt                                                                                                                                                    |
| msiuilevelfull         | 5     | Erstellte Benutzeroberfläche mit Assistenten, Fortschritt und Fehlern.                                                                                                                                                    |
| msiuilevelhidecancel   | 32    | In Kombination mit dem Wert von "msiuilevelbasic" zeigt das Installationsprogramm Status Dialogfelder an, zeigt jedoch keine Schaltfläche **Abbrechen** im Dialogfeld an, um zu verhindern, dass die Installation von Benutzern abgebrochen wird. |
| msiuilevelprogressonly | 64    | In Kombination mit dem Wert von "msiuilevelbasic" zeigt das Installationsprogramm Status Dialogfelder an, zeigt jedoch keine modalen Dialogfelder oder Fehler Dialogfelder an.                                        |
| msiuilevelenddialog    | 128   | In Kombination mit einem der obigen Werte zeigt das Installationsprogramm am Ende einer erfolgreichen Installation ein modales Dialogfeld an, oder wenn ein Fehler aufgetreten ist. Wenn der Benutzer abbricht, wird kein Dialogfeld angezeigt. |



 

Weitere Informationen finden Sie unter [bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion](determining-ui-level-from-a-custom-action.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




