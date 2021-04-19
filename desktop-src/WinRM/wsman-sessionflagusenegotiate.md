---
title: WSMAN. sessionflagusenegotiate-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagusenegotiate-Authentifizierungsflags für die Verwendung im flags-Parameter der WSMAN. kreatesession-Methode zurück.
ms.assetid: 86d8ed13-5eae-4a06-8ceb-b0ec067f4a4c
ms.tgt_platform: multiple
keywords:
- Sessionflagusenegotiate-Methode Windows-Remoteverwaltung
- Sessionflagusenegotiate-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagusenegotiate-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNegotiate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b57e463ccf71f22f12a964b1e1de72f426963c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342431"
---
# <a name="wsmansessionflagusenegotiate-method"></a>WSMAN. sessionflagusenegotiate-Methode

Die **WSMAN. sessionflagusenegotiate** -Methode gibt den Wert des **wsmanflagusenegotiate** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen. Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).

**Wsmanflagusenegotiate** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration. Weitere Informationen finden Sie unter [Authentifizierungs Konstanten](authentication-constants.md).

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagUseNegotiate( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Der Wert der Konstante.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WSMAN**](wsman.md)
</dt> <dt>

[**Sitzung**](session.md)
</dt> </dl>

 

 





