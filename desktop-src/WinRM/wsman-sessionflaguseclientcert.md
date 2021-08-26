---
title: WSMan.SessionFlagUseClientCertificate-Methode (WSManDisp.h)
description: Gibt den Wert des WSManFlagUseClientCertificate-Authentifizierungsflags zur Verwendung im flags-Parameter der WSMan.CreateSession-Methode zurück.
ms.assetid: b0ec4dbb-3a98-45e8-8f6b-74b858d6c3fc
ms.tgt_platform: multiple
keywords:
- SessionFlagUseClientCertificate-Methode Windows Remoteverwaltung
- SessionFlagUseClientCertificate-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Windows Remoteverwaltung, SessionFlagUseClientCertificate-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseClientCertificate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59220e3ead9e37579b354b82a97b8443ce8f66f93a7fffeff618c6563e7278d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997207"
---
# <a name="wsmansessionflaguseclientcertificate-method"></a>WSMan.SessionFlagUseClientCertificate-Methode

Die **WSMan.SessionFlagUseClientCertificate-Methode** gibt den Wert des **WSManFlagUseClientCertificate-Authentifizierungsflags** zur Verwendung im *flags-Parameter* der [**WSMan.CreateSession-Methode**](wsman-createsession.md) zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass Skripts nicht zum Festlegen eines konstanten Werts erforderlich sind. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonst constants](session-constants.md).

**WSManFlagUseClientCertificate** ist eine Konstante in der **\_ \_ WSManAuthenticationFlags-Enumeration.** Weitere Informationen finden Sie unter [Authentifizierungskonst konstanten](authentication-constants.md).

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagUseClientCertificate( _
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

 

 





