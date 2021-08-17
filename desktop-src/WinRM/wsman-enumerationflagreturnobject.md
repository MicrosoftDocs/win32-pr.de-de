---
title: WSMan.EnumerationFlagReturnObject-Methode (WSManDisp.h)
description: Gibt den Wert des Enumerationsflags EnumerationFlagReturnObject zur Verwendung im flags-Parameter von Session.Enumerate zurück.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- EnumerationFlagReturnObject-Methode Windows Remoteverwaltung
- EnumerationFlagReturnObject-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Windows Remoteverwaltung, EnumerationFlagReturnObject-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72d070770cdfe23083dc588ab2111fe9d891d0b8462ee66fa930e2e2fea444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742259"
---
# <a name="wsmanenumerationflagreturnobject-method"></a>WSMan.EnumerationFlagReturnObject-Methode

Die **WSMan.EnumerationFlagReturnObject-Methode** gibt den Wert des Enumerationsflags **EnumerationFlagReturnObject** zur Verwendung im *flags-Parameter* von [**Session.Enumerate zurück.**](session-enumerate.md) Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass Skripts nicht zum Festlegen eines konstanten Werts erforderlich sind. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonst constants](session-constants.md).

**EnumerationFlagReturnObject** ist eine Konstante in der **\_ WSManEnumFlags-Enumeration** und wird unter [**Enumerationskonst constants beschrieben.**](enumeration-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.EnumerationFlagReturnObject( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ out\]
</dt> <dd>

Der Wert der Konstante.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> </dl>

 

 





