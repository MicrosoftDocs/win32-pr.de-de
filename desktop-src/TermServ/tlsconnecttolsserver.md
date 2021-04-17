---
title: Tlsconnecttolsserver-Funktion
description: Öffnet ein Handle für die angegebene Remotedesktop Lizenzservers.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Tlsconnecttolsserver-Funktion Remotedesktopdienste
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
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392015"
---
# <a name="tlsconnecttolsserver-function"></a>Tlsconnecttolsserver-Funktion

Öffnet ein Handle für die angegebene Remotedesktop Lizenzservers.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszlsserver* \[ in\]
</dt> <dd>

Zeiger auf eine mit **null** endenden Zeichenfolge, die den NetBIOS-Namen des Remotedesktop Lizenzservers angibt. Wenn der Wert dieses Parameters **null** ist, ist der angegebene Server der lokale Computer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Handle für den angegebenen Server.

Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**. Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.

## <a name="remarks"></a>Bemerkungen

Wenn Sie mit der Verwendung des Handles, das von der **tlsconnecttolsserver** -Funktion zurückgegeben wird, fertig sind, geben Sie es durch Aufrufen der [**tlsdisconnectfromserver**](tlsdisconnectfromserver.md) -Funktion frei.

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

[**Tlsdisconnectfromserver**](tlsdisconnectfromserver.md)
</dt> </dl>

 

