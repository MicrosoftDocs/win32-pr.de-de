---
description: Die DoAction-Methode des Session-Objekts führt die Aktionsfunktion aus, die dem angegebenen Namen entspricht.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Session.DoAction-Methode (Photoacquire.h)
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
ms.openlocfilehash: 5c3f6451ec6ef920e6c6414a9396d2c4eeb2102ffc161e1ed91ce996752cd345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629390"
---
# <a name="sessiondoaction-method"></a>Session.DoAction-Methode

Die **DoAction-Methode** des [**Session-Objekts**](session-object.md) führt die Aktionsfunktion aus, die dem angegebenen Namen entspricht. Wenn ein NULL-Aktionsname angegeben wird, verwendet die Engine den Großbuchstaben der [ACTION-Eigenschaft](action.md) als auszuführende Aktion. Wenn kein Eigenschaftswert definiert ist, wird die Standardaktion ausgeführt, die derzeit als INSTALL definiert ist. Diese Methode gibt eine ganzzahlige Enumeration zurück.

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

Erforderlicher Zeichenfolgenname der auszuführende Aktion. Groß-/Kleinschreibung wird beachtet,

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Aktionen, die das System aktualisieren, z. B. die Aktionen [InstallFiles](installfiles-action.md) und [WriteRegistryValues,](writeregistryvalues-action.md) können nicht durch Aufrufen der **DoAction-Methode** ausgeführt werden. Die Ausnahme von dieser Regel ist, wenn die **DoAction-Methode** von einer benutzerdefinierten Aktion aufgerufen wird, die in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) zwischen den Aktionen [InstallInitialize](installinitialize-action.md) und [InstallFinalize](installfinalize-action.md)geplant ist. Aktionen, die das System nicht aktualisieren, z. B. [AppSearch](appsearch-action.md) oder [CostInitialize,](costinitialize-action.md)können aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| Header<br/>  | <dl> <dt>Photoacquire.h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



 

 




