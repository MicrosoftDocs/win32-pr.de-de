---
title: WSMAN. sessionflagnoencryption-Methode (WSManDisp. h)
description: Gibt den Wert des wsmanflagnoencryption-Authentifizierungsflags für die Verwendung im flags-Parameter der WSMAN. kreatesession-Methode zurück.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- Sessionflagnoencryption-Methode Windows-Remoteverwaltung
- Sessionflagnoencryption-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, sessionflagnoencryption-Methode
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
ms.openlocfilehash: ad4c7a85e97afd67ab6b1114248a9c4b3ee3ebbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339932"
---
# <a name="wsmansessionflagnoencryption-method"></a>WSMAN. sessionflagnoencryption-Methode

Die Methode **WSMAN. sessionflagnoencryption** gibt den Wert des **wsmanflagnoencryption** -Authentifizierungsflags zur Verwendung im *Flags* -Parameter der [**WSMAN. kreatesession**](wsman-createsession.md) -Methode zurück. Diese Methode bietet eine effizientere Syntax für die Verwendung der-Konstante, damit Skripts keinen konstanten Wert festlegen müssen. Weitere Informationen zum Abrufen dieser Methode finden Sie unter [Sitzungs Konstanten](session-constants.md).

**Wsmanflagnoencryption** ist eine Konstante in der **\_ \_ wsmansessionflags** -Enumeration. Weitere Informationen finden Sie unter [andere Sitzungs Konstanten](other-session-constants.md).

## <a name="syntax"></a>Syntax


```VB
WSMan.SessionFlagNoEncryption( _
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

 

 





