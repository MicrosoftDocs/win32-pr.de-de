---
title: WSMan.SessionFlagNoEncryption-Methode (WSManDisp.h)
description: Gibt den Wert des WSManFlagNoEncryption-Authentifizierungsflags für die Verwendung im flags-Parameter der WSMan.CreateSession-Methode zurück.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- SessionFlagNoEncryption-Methode Windows Remoteverwaltung
- SessionFlagNoEncryption-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung, SessionFlagNoEncryption-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagNoEncryption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22b1f3e278a5deafc890ee8aacf21e36174255dac82fc123647e890323a34b28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613500"
---
# <a name="wsmansessionflagnoencryption-method"></a>WSMan.SessionFlagNoEncryption-Methode

Die **WSMan.SessionFlagNoEncryption-Methode** gibt den Wert des **WSManFlagNoEncryption-Authentifizierungsflags** für die Verwendung im *flags-Parameter* der [**WSMan.CreateSession-Methode**](wsman-createsession.md) zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass skripts nicht erforderlich sind, um einen konstanten Wert festzulegen. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonstanten.](session-constants.md)

**WSManFlagNoEncryption** ist eine Konstante in der **\_ \_ WSManSessionFlags-Enumeration.** Weitere Informationen finden Sie unter [Andere Sitzungskonstanten.](other-session-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagNoEncryption( _
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

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 





