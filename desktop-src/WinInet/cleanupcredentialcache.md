---
title: Cleanupkredentialcache-Funktion
description: Wird von bestimmten Security Support Provider (SSP) implementiert, um den SSP-Anmelde Informations Cache zu leeren.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Cleanupkredentialcache-Funktion WinInet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102927"
---
# <a name="cleanupcredentialcache-function"></a>Cleanupkredentialcache-Funktion

Die **cleanupkredentialcache** -Funktion wird von bestimmten SSP (Security Support Providers) implementiert, um den SSP-Anmelde Informations Cache zu leeren.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

**True** , wenn die Funktion erfolgreich ausgeführt wird. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Die **cleanupkredentialcache** -Funktion wird von den folgenden SSPs implementiert:

-   MSNSSPC.dll
-   MSAPSSPC.dll

Die Implementierung von **cleanupkredentialcache** durch diese SSPs gibt immer **true** zurück.

Bevor Sie versuchen, ein Modul Handle zum Exportieren von **cleanupkredentialcache** abzurufen, muss die Anwendung überprüfen, ob es sich bei dem geladenen SSP um eines der bekannten SSPs handelt, die die **cleanupkredentialcache** -Funktion implementieren.

Um den SSP-Anmelde Informations Cache zu leeren, muss die Anwendung ein Modul Handle für den SSP abrufen, indem die [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) -Funktion aufgerufen wird. Nachdem das Modul abgerufen wurde, sollte die Anwendung die vom SSP implementierte **cleanupcredentialcache** -Funktion exportieren, indem Sie die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufruft und das von **GetModuleHandle** und **cleanupcredentialcache** zurückgegebene Modul als Eingabeparameter übergibt.

Wie alle anderen Aspekte der WinInet-API kann diese Funktion nicht sicher innerhalb von DllMain oder den Konstruktoren und Dekonstruktoren von globalen Objekten aufgerufen werden.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                       |
| DLL<br/>                      | <dl> <dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

