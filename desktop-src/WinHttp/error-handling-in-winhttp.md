---
description: Fehlerbehandlung in WinHTTP
ms.assetid: 96bceda2-ca96-4f88-ab38-35021889c2dd
title: Fehlerbehandlung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf234220d0973e86c830063e4ecc25312fa2d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364125"
---
# <a name="error-handling-in-winhttp"></a>Fehlerbehandlung in WinHTTP

Nicht alle WinHTTP-API-Funktionen melden Fehler auf die gleiche Weise.

Einige Funktionen, z. b. [**winhttpsettimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts), geben einen **booleschen** Wert zurück, der einen Fehler angibt, wenn **false**. Wenn **false** zurückgegeben wird, sollten Aufrufer, die an dem Fehler interessiert sind, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen. Wenn **GetLastError** aufgerufen wird, wenn die Funktion erfolgreich war (gibt etwas aber **false** zurück), ist der zurückgegebene Wert unvorhersehbar und kann sich zwischen den Windows-Versionen, Service Packs oder sogar zwischen Aufrufen derselben Funktion ändern.

Einige Funktionen, z. b. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), geben ein [HINTERNET](hinternet-handles-in-winhttp.md) -Pseudo Handle zurück. Diese Funktionen sind identisch, mit dem Unterschied, dass der Fehler durch die Rückgabe von **null** angegeben wird. Wenn **null** zurückgegeben wird, sollten Aufrufer, die an dem Fehler interessiert sind, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen. Wenn **GetLastError** aufgerufen wird, wenn die Funktion erfolgreich war (gibt alles als **null** zurück), ist der zurückgegebene Wert unvorhersehbar und kann sich zwischen den Windows-Versionen, Service Packs oder sogar zwischen Aufrufen derselben Funktion ändern.

Einige Funktionen, wie z. b. [**winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult), geben einen **DWORD** -Fehlercode zurück, und es ist nicht erforderlich, andere Funktionen aufzurufen, um weitere Fehlerinformationen zu erhalten. Für diese Funktionen sollte [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) nicht aufgerufen werden. Wenn **GetLastError** aufgerufen wird, unabhängig davon, ob die Funktion erfolgreich war oder fehlgeschlagen ist, ist der zurückgegebene Wert unvorhersehbar und kann sich zwischen den Windows-Versionen, Service Packs oder sogar zwischen Aufrufen derselben Funktion ändern.

 

 
