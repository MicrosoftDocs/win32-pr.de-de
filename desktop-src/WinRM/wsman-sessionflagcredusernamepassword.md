---
title: WSMan.SessionFlagCredUsernamePassword-Methode (WSManDisp.h)
description: Gibt den Wert des Authentifizierungsflags WSManFlagCredUsernamePassword für die Verwendung im flags-Parameter der WSMan.CreateSession-Methode zurück.
ms.assetid: 70d12df4-f0ac-499a-8b2f-6ba83b77869e
ms.tgt_platform: multiple
keywords:
- SessionFlagCredUsernamePassword-Methode Windows Remoteverwaltung
- SessionFlagCredUsernamePassword-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung , SessionFlagCredUsernamePassword-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagCredUsernamePassword
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0383d9f9bd5f7e565510bf62b0940fccc2e2d998e6419f770befa35a8a8e727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613510"
---
# <a name="wsmansessionflagcredusernamepassword-method"></a>WSMan.SessionFlagCredUsernamePassword-Methode

Die **WSMan.SessionFlagCredUsernamePassword-Methode** gibt den Wert des Authentifizierungsflags **WSManFlagCredUsernamePassword** für die Verwendung im *flags-Parameter* der [**WSMan.CreateSession-Methode**](wsman-createsession.md) zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass skripts nicht erforderlich sind, um einen konstanten Wert festzulegen. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonstanten.](session-constants.md)

**WSManFlagCredUsernamePassword** ist eine Konstante in der **\_ \_ WSManSessionFlags-Enumeration.** Weitere Informationen finden Sie unter [Authentifizierungskonstanten.](authentication-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagCredUsernamePassword( _
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

 

 





