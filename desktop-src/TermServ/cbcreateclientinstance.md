---
title: Cbkreateclientinstance-Funktion (cbclient. h)
description: Erstellt eine Instanz des Remotedesktopverbindung Broker-RPC-Clients.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der cbkreateclientinstance-Funktion
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
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360437"
---
# <a name="cbcreateclientinstance-function"></a>Cbkreateclientinstance-Funktion

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

*Version* \[ in\]
</dt> <dd>

Gibt die Version der angeforderten Remotedesktopverbindung Broker-Client Schnittstelle an. Dabei muss es sich um den folgenden Wert handeln.

<dt>

1
</dt> <dd>

Version 1 des Remotedesktopverbindung Broker-Clients.

</dd> </dl> </dd> <dt>

*ppcbclient* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines [**iconnectionbrokerclient**](iconnectionbrokerclient.md) -Schnittstellen Zeigers, der das Remotedesktopverbindung Broker-Client Objekt empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cbclient. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





