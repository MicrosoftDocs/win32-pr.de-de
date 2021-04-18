---
description: Die doaction-Methode des Session-Objekts führt die Aktions Funktion aus, die dem angegebenen Namen entspricht.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Session. doaction-Methode (photobeschaffung. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365482"
---
# <a name="sessiondoaction-method"></a>Session. doaction-Methode

Die **doaction** -Methode des [**Session**](session-object.md) -Objekts führt die Aktions Funktion aus, die dem angegebenen Namen entspricht. Wenn ein NULL-Aktionsname angegeben wird, verwendet die Engine den Großbuchstaben der [Action-Eigenschaft](action.md) als Aktion, die ausgeführt werden soll. Wenn kein Eigenschafts Wert definiert ist, wird die Standardaktion ausgeführt, die derzeit als install definiert ist. Diese Methode gibt eine ganzzahlige Enumeration zurück.

## <a name="syntax"></a>Syntax


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*action* 
</dt> <dd>

Erforderlicher Zeichen folgen Name der auszuführenden Aktion. Groß-/Kleinschreibung wird beachtet,

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Aktionen, die das System aktualisieren, z. b. die Aktionen " [InstallFiles](installfiles-action.md) " und " [schreiteregistryvalues](writeregistryvalues-action.md) ", können durch Aufrufen der **doaction** -Methode nicht ausgeführt werden. Eine Ausnahme von dieser Regel ist, wenn die **doaction** -Methode von einer benutzerdefinierten Aktion aufgerufen wird, die in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) zwischen den [InstallInitialize](installinitialize-action.md) -und [InstallFinalize-Aktionen](installfinalize-action.md)geplant ist. Aktionen, die das System nicht aktualisieren, z. b. [AppSearch](appsearch-action.md) oder [costinitialize](costinitialize-action.md), können aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| Header<br/>  | <dl> <dt>Photoabruf. h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




