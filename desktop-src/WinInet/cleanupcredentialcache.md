---
title: CleanupCredentialCache-Funktion
description: Wird von bestimmten Sicherheitsunterstützungsanbietern (Security Support Providers, SSP) implementiert, um den SSP-Anmeldeinformationscache zu leeren.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- CleanupCredentialCache-Funktion WinINet
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
ms.openlocfilehash: 62edb05f401c5ed69092c432f20a7ee96c98afd369e4a4cb0a1acde30e166013
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413020"
---
# <a name="cleanupcredentialcache-function"></a>CleanupCredentialCache-Funktion

Die **CleanupCredentialCache-Funktion** wird von bestimmten Sicherheitsunterstützungsanbietern (Security Support Providers, SSP) implementiert, um den SSP-Anmeldeinformationscache zu leeren.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn die Funktion erfolgreich ausgeführt wird; Andernfalls **FALSE**.

## <a name="remarks"></a>Hinweise

Die **CleanupCredentialCache-Funktion** wird von den folgenden SSPs implementiert:

-   MSNSSPC.dll
-   MSAPSSPC.dll

Die Implementierung von **CleanupCredentialCache** durch diese SSPs gibt immer **TRUE** zurück.

Bevor versucht wird, ein Modulhandle zum Exportieren von **CleanupCredentialCache** abzurufen, muss die Anwendung überprüfen, ob der geladene SSP einer der bekannten SSPs ist, die die **CleanupCredentialCache-Funktion** implementieren.

Um den SSP-Anmeldeinformationscache zu leeren, muss die Anwendung ein Modulhandle für den SSP abrufen, indem sie die [**GetModuleHandle-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) aufruft. Nach dem Abrufen des Moduls sollte die Anwendung die vom SSP implementierte **CleanupCredentialCache-Funktion** exportieren, indem sie die [**GetProcAddress-Funktion aufruft**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und das von **GetModuleHandle** und **CleanupCredentialCache** zurückgegebene Modul als Eingabeparameter übergibt.

Wie alle anderen Aspekte der WinINet-API kann diese Funktion nicht sicher aus DllMain oder den Konstruktoren und Destruktoren globaler Objekte aufgerufen werden.

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                       |
| DLL<br/>                      | <dl> <dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt> </dl> |



 

