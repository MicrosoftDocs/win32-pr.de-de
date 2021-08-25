---
description: Fehlerbehandlung in WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Fehlerbehandlung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72dac7775934684afe6cc9c9d54bc36bb8f3295c91deef7449e9a00600bc687e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899185"
---
# <a name="error-handling-in-winhttp"></a>Fehlerbehandlung in WinHTTP

Nicht alle WinHTTP-API-Funktionen melden Fehler auf die gleiche Weise.

Einige Funktionen, z. B. [**WinHttpSetTimeouts,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)geben eine **BOOL** zurück, die bei **FALSE** einen Fehler angibt. Wenn **FALSE** zurückgegeben wird, sollten Aufrufer, die an dem Fehler interessiert [**sind, GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen. Wenn **GetLastError** aufgerufen wird, wenn die Funktion erfolgreich ausgeführt wurde (nur **FALSE** zurückgegeben), ist der zurückgegebene Wert unvorhersehbar und kann sich zwischen Windows Versionen, Service Packs oder sogar zwischen Aufrufen derselben Funktion ändern.

Einige Funktionen, z. B. [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)geben ein [HINTERNET-Pseudohandle](hinternet-handles-in-winhttp.md) zurück. Diese Funktionen sind genau identisch, mit dem Unterschied, dass ein Fehler durch Zurückgeben von **NULL** angegeben wird. Wenn **NULL** zurückgegeben wird, sollten Aufrufer, die an dem Fehler interessiert [**sind, GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen. Wenn **GetLastError** aufgerufen wird, wenn die Funktion erfolgreich ausgeführt wurde (alles außer **NULL** zurückgegeben), ist der zurückgegebene Wert unvorhersehbar und kann sich zwischen Windows Versionen, Service Packs oder sogar zwischen Aufrufen derselben Funktion ändern.

Einige Funktionen, z. B. [**WinHttpGetProxyResult,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)geben einen **DWORD-Fehlercode** zurück, und es ist nicht erforderlich, andere Funktionen für weitere Fehlerinformationen aufzurufen. Für diese Funktionen sollte [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) nicht aufgerufen werden. Wenn **GetLastError** unabhängig vom Erfolg oder Fehler der Funktion aufgerufen wird, ist der zurückgegebene Wert unvorhersehbar und kann sich zwischen Windows Versionen, Service Packs oder sogar zwischen Aufrufen derselben Funktion ändern.

 

 
