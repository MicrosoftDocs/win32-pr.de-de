---
title: CBCreateClientInstance-Funktion (Cbclient.h)
description: Erstellt eine Instanz des Remotedesktopverbindung Broker-RPC-Clients.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- CBCreateClientInstance-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b0873fac5b33370333ec8f5774e5b8dbbcd896f6afb9777a6dd74dd6913dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610147"
---
# <a name="cbcreateclientinstance-function"></a>CBCreateClientInstance-Funktion

Erstellt eine Instanz des Remotedesktopverbindung Broker-RPC-Clients.

## <a name="syntax"></a>Syntax


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Version* \[ In\]
</dt> <dd>

Gibt die Version der Remotedesktopverbindung Broker-Clientschnittstelle an, die angefordert wird. Dies muss der folgende Wert sein.

<dt>

1
</dt> <dd>

Version 1 des Remotedesktopverbindung Broker-Clients.

</dd> </dl> </dd> <dt>

*ppCbClient* \[ out\]
</dt> <dd>

Die Adresse eines [**IConnectionBrokerClient-Schnittstellenzeigers,**](iconnectionbrokerclient.md) der das Remotedesktopverbindung Broker-Clientobjekt empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cbclient.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Cbclient.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





