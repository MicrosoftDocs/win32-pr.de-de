---
title: WSMan.EnumerationFlagReturnEPR-Methode (WSManDisp.h)
description: Gibt den Wert des Enumerationsflags EnumerationFlagReturnEPR zur Verwendung im flags-Parameter von Session.Enumerate zurück.
ms.assetid: 5e168aa9-5be1-46b3-bb9b-59895e68a75d
ms.tgt_platform: multiple
keywords:
- EnumerationFlagReturnEPR-Methode Windows Remoteverwaltung
- EnumerationFlagReturnEPR-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Windows Remoteverwaltung, EnumerationFlagReturnEPR-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f464dddc35a7976b5231b116a5e51322b86e2941d9a2cd5a476b86b600130ef1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742269"
---
# <a name="wsmanenumerationflagreturnepr-method"></a>WSMan.EnumerationFlagReturnEPR-Methode

Die **EnumerationFlagReturnEPR-Methode** gibt den Wert des Enumerationsflags **EnumerationFlagReturnEPR** für die Verwendung im *flags-Parameter* von [**Session.Enumerate zurück.**](session-enumerate.md) Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass Skripts nicht zum Festlegen eines konstanten Werts erforderlich sind. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonst constants](session-constants.md).

**EnumerationFlagReturnEPR** ist eine Konstante in der **\_ WSManEnumFlags-Enumeration** und wird unter [**Enumerationskonst constants beschrieben.**](enumeration-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.EnumerationFlagReturnEPR( _
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

 

 





