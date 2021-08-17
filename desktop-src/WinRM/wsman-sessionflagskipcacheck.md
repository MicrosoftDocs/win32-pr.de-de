---
title: WSMan.SessionFlagSkipCACheck-Methode (WSManDisp.h)
description: Gibt den Wert des WSManFlagSkipCACheck-Authentifizierungsflags für die Verwendung im flags-Parameter von WSMan.CreateSession zurück.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- SessionFlagSkipCACheck-Methode Windows Remoteverwaltung
- SessionFlagSkipCACheck-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung, SessionFlagSkipCACheck-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe24e10ca7a568a6dc9b3af6efed6e31a3a9fde5acac70e2badab37d24373350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742029"
---
# <a name="wsmansessionflagskipcacheck-method"></a>WSMan.SessionFlagSkipCACheck-Methode

Die **WSMan.SessionFlagSkipCACheck-Methode** gibt den Wert des **WSManFlagSkipCACheck-Authentifizierungsflags** für die Verwendung im *flags-Parameter* von [**WSMan.CreateSession**](wsman-createsession.md)zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass skripts nicht erforderlich sind, um einen konstanten Wert festzulegen. Weitere Informationen zum Aufrufen dieser Methode und Codebeispiele finden Sie unter [Sitzungskonstanten.](session-constants.md)

**WSManFlagSkipCACheck** ist eine Konstante in der **\_ \_ WSManSessionFlags-Enumeration.** Weitere Informationen finden Sie unter [**Authentifizierungskonstanten.**](authentication-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagSkipCACheck( _
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Sitzungskonsistenz**](session.md)
</dt> </dl>

 

 





