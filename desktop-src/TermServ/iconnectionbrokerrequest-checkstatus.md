---
title: Iconnectionbrokerrequest checkStatus-Methode (cbclient. h)
description: Wird aufgerufen, um den Status einer asynchronen Anforderung zu bestimmen.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- CheckStatus-Methode Remotedesktopdienste
- CheckStatus-Methode Remotedesktopdienste, iconnectionbrokerrequest-Schnittstelle
- Iconnectionbrokerrequest-Schnittstelle Remotedesktopdienste, checkStatus-Methode
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392172"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>Iconnectionbrokerrequest:: checkStatus-Methode

Wird aufgerufen, um den Status einer asynchronen Anforderung zu bestimmen.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preqstatus* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer Variablen, die einen Wert der CB- [**\_ Anforderungs \_ Status**](cb-request-status.md) -Enumeration empfängt, der den Status der Anforderung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Header<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconnectionbrokerrequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





