---
title: WSMan.SessionFlagUseCredSsp-Methode (WSManDisp.h)
description: Gibt den Wert des WSManFlagUseCredSsp-Authentifizierungsflags für die Verwendung im flags-Parameter der WSMan.CreateSession-Methode zurück.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- SessionFlagUseCredSsp-Methode Windows Remoteverwaltung
- SessionFlagUseCredSsp-Methode Windows Remoteverwaltung, WSMan-Objekt
- WSMan-Objekt Windows Remoteverwaltung , SessionFlagUseCredSsp-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb96f1de72bbcceafd40c0ccbcfdd3b990ed2134739195bd29e130dbac5a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642230"
---
# <a name="wsmansessionflagusecredssp-method"></a>WSMan.SessionFlagUseCredSsp-Methode

Gibt den Wert des **WSManFlagUseCredSsp-Authentifizierungsflags** für die Verwendung im *flags-Parameter* der [**WSMan.CreateSession-Methode**](wsman-createsession.md) zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der -Konstante, sodass skripts nicht erforderlich sind, um einen konstanten Wert festzulegen. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Sitzungskonstanten.](session-constants.md)

**WSManFlagUseCredSsp** ist eine Konstante in der **\_ \_ WSManSessionFlags-Enumeration.** Weitere Informationen finden Sie unter [Authentifizierungskonstanten.](authentication-constants.md)

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagUseCredSsp( _
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
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Verteilbare Komponente<br/>          | Windows Management Framework auf Windows Server 2008 mit SP2, Windows Vista mit SP1 und Windows Vista mit SP2<br/> |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>                                      |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl>                                    |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wsman**](wsman.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 





