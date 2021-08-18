---
title: WSMan.SessionFlagUTF8-Methode (WSManDisp.h)
description: Gibt den Wert des WSManFlagUTF8-Authentifizierungsflags für die Verwendung im flags-Parameter von WSMan.CreateSession zurück.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- SessionFlagUTF8-Methode Windows Remoteverwaltung
- SessionFlagUTF8-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung, SessionFlagUTF8-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fe6cc1b5f18fa316656d2b6974bd47c8209277ed24ef2798479227f9876e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741918"
---
# <a name="wsmansessionflagutf8-method"></a>WSMan.SessionFlagUTF8-Methode

Die **WSMan.SessionFlagUTF8-Methode** gibt den Wert des **WSManFlagUTF8-Authentifizierungsflags** für die Verwendung im *flags-Parameter* von [**WSMan.CreateSession**](wsman-createsession.md)zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass skripts nicht erforderlich sind, um einen konstanten Wert festzulegen. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonstanten.](session-constants.md)

**WSManFlagUTF8** ist eine Konstante in der **\_ \_ WSManSessionFlags-Enumeration.** Weitere Informationen finden Sie unter [Andere Sitzungskonstanten.](other-session-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagUTF8( _
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

 

 





