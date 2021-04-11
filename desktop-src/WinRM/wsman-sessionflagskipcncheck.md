---
title: WSMAN. sessionflagskipcncheck-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagskipcncheck-Authentifizierungsflags für die Verwendung im flags-Parameter von WSMAN. kreatesession zurück.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Sessionflagskipcncheck-Methode Windows-Remoteverwaltung
- Sessionflagskipcncheck-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagskipcncheck-Methode
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956744"
---
# <a name="wsmansessionflagskipcncheck-method"></a>WSMAN. sessionflagskipcncheck-Methode

Die **WSMAN. sessionflagskipcncheck** -Methode gibt den Wert des **wsmanflagskipcncheck** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter von [**WSMAN. kreatesession**](wsman-createsession.md)zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen. Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).

**Wsmanflagskipcncheck** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration. Weitere Informationen finden Sie unter [**Authentifizierungs Konstanten**](authentication-constants.md).

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagSkipCNCheck( _
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

 

 





