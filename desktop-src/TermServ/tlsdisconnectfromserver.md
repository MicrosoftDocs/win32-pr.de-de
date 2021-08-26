---
title: TLSDisconnectFromServer-Funktion
description: Schließt ein geöffnetes Handle für einen Remotedesktop Lizenzserver.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- TLSDisconnectFromServer-Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95911536eda4bd87e45fd034626cf83d88f4d9fc768e4837316ee93abfe3c3d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869410"
---
# <a name="tlsdisconnectfromserver-function"></a>TLSDisconnectFromServer-Funktion

Schließt ein geöffnetes Handle für einen Remotedesktop Lizenzserver.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mstlsapi.dll.

 

## <a name="syntax"></a>Syntax


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ In\]
</dt> <dd>

Handle für einen Remotedesktop Lizenzserver, der durch einen Aufruf der [**TLSConnectToLsServer-Funktion geöffnet**](tlsconnecttolsserver.md) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie **die TLSDisconnectFromServer-Funktion** als Teil der Bereinigungsroutine Ihres Programms auf, um alle Serverhandles zu schließen, die durch Aufrufe der [**TLSConnectToLsServer-Funktion geöffnet**](tlsconnecttolsserver.md) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_TLS-HANDLE**](tls-handle.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> </dl>

 

