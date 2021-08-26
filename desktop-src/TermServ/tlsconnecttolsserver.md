---
title: TLSConnectToLsServer-Funktion
description: Öffnet ein Handle für den angegebenen Remotedesktop Lizenzserver.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- TLSConnectToLsServer-Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbfc3c1e365a97b8199df34c2e55a8362f48b7f6a2a43e524e3c6e937de5cb0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986970"
---
# <a name="tlsconnecttolsserver-function"></a>TLSConnectToLsServer-Funktion

Öffnet ein Handle für den angegebenen Remotedesktop Lizenzserver.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mstlsapi.dll.

 

## <a name="syntax"></a>Syntax


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszLsServer* \[ In\]
</dt> <dd>

Zeiger auf eine mit **NULL beendete** Zeichenfolge, die den NetBIOS-Namen des Remotedesktop angibt. Wenn der Wert dieses Parameters **NULL ist,** ist der angegebene Server der lokale Computer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle für den angegebenen Server.

Wenn die Funktion fehlschlägt, ist der Rückgabewert **NULL.** Um erweiterte Fehlerinformationen zu erhalten, rufen Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Hinweise

Wenn Sie das von der **TLSConnectToLsServer-Funktion** zurückgegebene Handle nicht mehr verwenden, geben Sie es frei, indem Sie die [**TLSDisconnectFromServer-Funktion**](tlsdisconnectfromserver.md) aufrufen.

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

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

