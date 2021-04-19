---
title: Tlsdisconnectfromserver-Funktion
description: Schließt ein geöffnetes Handle für einen Remotedesktop-Lizenzserver.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Tlsdisconnectfromserver-Funktion Remotedesktopdienste
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
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342669"
---
# <a name="tlsdisconnectfromserver-function"></a>Tlsdisconnectfromserver-Funktion

Schließt ein geöffnetes Handle für einen Remotedesktop-Lizenzserver.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ in\]
</dt> <dd>

Handle für einen Remotedesktop Lizenzserver, der durch einen Rückruf der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Rufen Sie die **tlsdisconnectfromserver** -Funktion als Teil der cleanuproutine Ihres Programms auf, um alle Server Handles zu schließen, die durch Aufrufe der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TLS- \_ handle**](tls-handle.md)
</dt> <dt>

[**Tlsconnecttolsserver**](tlsconnecttolsserver.md)
</dt> </dl>

 

