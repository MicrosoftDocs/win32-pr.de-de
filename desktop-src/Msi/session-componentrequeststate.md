---
description: Die componentrequeststate-Eigenschaft des Session-Objekts Ruft eine Änderung im Aktionszustand einer Zeile in der Komponenten Tabelle ab oder fordert Sie an.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Session. componentrequeststate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368473"
---
# <a name="sessioncomponentrequeststate-property"></a>Session. componentrequeststate (Eigenschaft)

Die **componentrequeststate** -Eigenschaft des [**Session**](session-object.md) -Objekts Ruft eine Änderung im Aktionszustand einer Zeile in der [Komponenten Tabelle](component-table.md)ab oder fordert Sie an.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Eigenschaftswert

Erforderlicher Zeichen folgen Name des Komponenten Elements, Primärschlüssel der Komponenten Tabelle.

## <a name="remarks"></a>Bemerkungen



| Auswahl Status        | Wert | BESCHREIBUNG                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | Fordert an, dass für dieses Element keine Aktion ausgeführt wird.                |
| msiinstallstatemissing  | 2     | Das Element muss entfernt werden.                                         |
| msiinstallstatuelocal   | 3     | Das Element muss lokal installiert werden.                               |
| msiinstallstaatource  | 4     | Das Element muss installiert und vom Quell Medium aus ausgeführt werden.         |
| msiinstallstatedefault | 5     | Wenn das Element installiert ist, muss es im selben Zustand neu installiert werden. |



 

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




