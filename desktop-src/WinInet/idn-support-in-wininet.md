---
title: IDN-Unterstützung in WinInet
description: Ab Windows Server 2008 und Windows Vista wird der Hostteil der Unicode-URL in den internationalisierten Domänen Namen (IDN) konvertiert.
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390880"
---
# <a name="idn-support-in-wininet"></a>IDN-Unterstützung in WinInet

Ab Windows Server 2008 und Windows Vista wird der Hostteil der Unicode-URL in den internationalisierten Domänen Namen (IDN) konvertiert. Separate Teile der Unicode-URL-Codierung können auch von Konfigurationen geändert werden, die von der Anwendung festgelegt werden. Die ANSI-Versionen der WinInet-API senden die URL weiterhin über das Netzwerk, wie Sie von der Anwendung eingegeben wurde, aber die WinInet-Unicode-Versionen der API entsprechen jetzt dem IDN-Standard (RFC3490) für URL-Codierungen.

Wenn eine URL als Unicode-Parameter eingegeben wird, wird der Hostteil standardmäßig in das IDN-Format konvertiert, sowohl für Proxy-als auch für direkte Verbindungen. Die Anwendung hat die Möglichkeit, die IDN-Host Formatierung zu deaktivieren, indem Sie die Option " **Internet \_ Option \_ IDN** " festlegen. Die IDN-Host Konvertierung kann nur für die direkt-oder Proxy Verbindungen mithilfe der **Internet-Flag IDN \_ \_ \_ Direct** oder **Internet \_ Flag \_ IDN- \_ proxyflags** mit **Internet- \_ Option \_ IDN** aktiviert werden.

Im folgenden Codebeispiel wird veranschaulicht, wie die IDN-Host Konvertierung sowohl für den Proxy als auch für die direkte Verbindung deaktiviert wird.

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

Wenn die IDN-Host Formatierung deaktiviert ist, kann die Anwendung die gewünschte Codepage mithilfe der **Internet \_ Option \_ Codepage** angeben.

Im folgenden Codebeispiel wird gezeigt, wie die japanische Codepage angegeben wird.

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

Der Pfadteil der URL ist standardmäßig UTF8-codiert, und die restlichen Segmente der URL, die Abfrage oder das Fragment, werden in die standardmäßige System Codepage (CP \_ ACP) konvertiert.

Im folgenden Beispiel wird gezeigt, wie die Codepages Koreanisch für den Pfadteil der URL angegeben wird.

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

In der folgenden Tabelle werden die Optionen für die Unterstützung von IDN definiert. Weitere Informationen finden Sie im Thema [Optionsflags](option-flags.md) .



| Option                            | BESCHREIBUNG                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Codepage für Internet- \_ Optionen \_        | Diese Option wird für die Anforderung oder das Verbindungs Handle festgelegt, um ein Code Page-Codierungsschema für den Hostteil der URL anzugeben. Diese Option wird ignoriert, wenn IDN aktiviert ist.                                                      |
| Internet \_ Option \_ Codepage- \_ Pfad  | Diese Option wird für die Anforderung festgelegt, oder das Verbindungs Handle aktiviert das angegebene Codierungsschema für den Pfadteil der URL. Standardmäßig ist der Pfadteil der URL UTF8-codiert.                                         |
| Internet \_ Option \_ Codepage \_ extra | Das Festlegen dieser Option für die Anforderung oder das Verbindungs Handle ermöglicht das angegebene Codierungsschema für den zusätzlichen Teil der URL. Standardmäßig wird der zusätzliche Teil der URL in der standardmäßigen System Codepage (CP \_ ACP) codiert. |
| Internet \_ Option \_ IDN             | Diese Option kann für die Anforderung oder das Verbindungs Handle zum Aktivieren oder Deaktivieren der IDN-Host Konvertierung verwendet werden. Wenn IDN deaktiviert ist, verwendet Wininet die standardmäßige System Codepage, um den Host-oder Autoritäts Teil der URL zu codieren.       |



 

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 