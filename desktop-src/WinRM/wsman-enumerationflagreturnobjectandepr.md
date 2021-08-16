---
title: WSMan.EnumerationFlagReturnObjectAndEPR-Methode (WSManDisp.h)
description: Gibt den Wert des Enumerationsflags EnumerationFlagReturnObjectAndEPR zur Verwendung im flags-Parameter von Session.Enumerate zurück.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- EnumerationFlagReturnObjectAndEPR-Methode Windows Remoteverwaltung
- EnumerationFlagReturnObjectAndEPR-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Windows Remoteverwaltung, EnumerationFlagReturnObjectAndEPR-Methode
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObjectAndEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa63e84770010a05e144c702a10a814aea4cf8323681f6e95c8bf2facc1dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742279"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a>WSMan.EnumerationFlagReturnObjectAndEPR-Methode

Die **EnumerationFlagReturnObjectAndEPR-Methode** gibt den Wert des Enumerationsflags **EnumerationFlagReturnObjectAndEPR** zur Verwendung im *flags-Parameter* von [**Session.Enumerate**](session-enumerate.md)zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass Skripts nicht zum Festlegen eines konstanten Werts erforderlich sind. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonst constants](session-constants.md).

**EnumerationFlagReturnObjectAndEPR** ist eine Konstante in der **\_ WSManEnumFlags-Enumeration** und wird unter [**Enumerationskonst constants beschrieben.**](enumeration-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
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

 

 





