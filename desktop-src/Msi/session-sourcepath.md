---
description: Die SourcePath-Eigenschaft des Session-Objekts ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zum angegebenen Ordner auf dem Quell Medium oder dem Server Image bereitstellt.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session. SourcePath (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372736"
---
# <a name="sessionsourcepath-property"></a>Session. SourcePath (Eigenschaft)

Die **SourcePath** -Eigenschaft des [**Session**](session-object.md) -Objekts ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zum angegebenen Ordner auf dem Quell Medium oder dem Server Image bereitstellt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>Eigenschaftswert

Unter Berücksichtigung der Groß-/Kleinschreibung für eine Ordner Eigenschaft, die durch einen Primärschlüssel der [Verzeichnis Tabelle](directory-table.md)angegeben wird. Wenn der Ordner nicht vorhanden ist, wird ein Fehler generiert.

## <a name="remarks"></a>Bemerkungen

Wenn die Eigenschaft fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




