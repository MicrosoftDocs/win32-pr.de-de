---
description: Anwendungen, die von WinINet zu WinHTTP portieren, müssen möglicherweise die gleichen Autoproxyeinstellungen verwenden, die sie unter WinINet oder Internet Explorer (IE) abrufen können.
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Festlegen von WinINet-Proxykonfigurationen in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa060d24036a02752a5eefacc9ea6672dec9bb77bad30f653c8f382490a487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133053"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Festlegen von WinINet-Proxykonfigurationen in WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Festlegen des automatischen Proxys für WinHTTP 5.1

Anwendungen, die von WinINet zu WinHTTP portieren, müssen möglicherweise die gleichen Autoproxyeinstellungen verwenden, die sie unter WinINet oder Internet Explorer (IE) abrufen können. Die WinHTTP-API der Version 5.1 kann diese Proxyeinstellungen abrufen und verwenden. Im Allgemeinen gibt WinHTTP die Proxy- und Proxyumgehungsserver pro Sitzung an, wenn die Sitzung erstellt wird. Diese Einstellungen können anforderungsbezogen überschrieben werden.

Um dieselbe Proxykonfiguration wie WinINet oder IE zu verwenden, sollte der WinHTTP-Client Proxyeinstellungen für die Sitzung festlegen. Wenn IE oder WinINet für die Verwendung der automatischen Webproxyermittlung (Web Proxy Auto-Discovery, WPAD) konfiguriert sind, muss der WinHTTP-Client, der diese Einstellungen verwendet, proxyeinstellungen auf Anforderungsbasis festlegen. In den folgenden Abschnitten wird beschrieben, wie Sie die Proxyeinstellungen für eine Sitzung und eine Anforderung angeben:

-   [Festlegen der Proxykonfiguration für eine Sitzung](#setting-the-proxy-configuration-on-a-session)
-   [Festlegen der Proxykonfiguration für eine einzelne Anforderung](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Festlegen der Proxykonfiguration für eine Sitzung

## <a name="the-application-is-running-on-a-user-account"></a>Die Anwendung wird unter einem Benutzerkonto ausgeführt.

Bevor eine Sitzung erstellt wird, ruft die Anwendung [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) auf, um die IE-Proxyeinstellungen abzurufen. Die Anwendung muss als Benutzerkonto ausgeführt werden, um diese Einstellungen zu erhalten. Der *pProxyConfig-Parameter* ist ein Zeiger auf eine [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) die den Proxynamen (*lpszProxy*) und die Proxyumgehung (*lpszProxyBypass*) -Server enthält. Die Proxynamen- und Proxyumgehungswerte der **WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG-Struktur** werden dann verwendet, um die WinHTTP-Sitzung zu initialisieren. Die Sitzung wird initialisiert, indem [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) mit den *Parametern pwszProxyName* und *pwszProxyBypass* aufgerufen wird, die von den **lpszProxy-** und **lpszProxyBypass-Membern** der **WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG-Struktur** abgerufen werden.

## <a name="the-application-is-running-as-a-service"></a>Die Anwendung wird als Dienst ausgeführt.

Die Anwendung muss sicherstellen, dass die Registrierungseinstellungen für einen einzelnen Benutzer in die Registrierung geladen werden, bevor [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)aufgerufen wird. Wenn diese Einstellungen nicht in die Registrierung geladen werden, kann **WinHttpGetIEProxyConfigForCurrentUser** die Proxyeinstellungen nicht abrufen. Registrierungseinstellungen für einen einzelnen Benutzer können durch Aufrufen der **LoadUserProfile-Funktion** in die Registrierung geladen werden. Wenn das Laden der Registrierungseinstellungen des Benutzers keine Option ist, kann die Anwendung [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) mit dem **WINHTTP \_ ACCESS TYPE DEFAULT \_ \_ \_ PROXY** aufrufen, der im *dwAcessType-Parameter* angegeben ist. Durch Angeben des Standardproxys im Aufruf von **WinHttpOpen** wird die WinHTTP-API angewiesen, den Proxykonfigurationssatz mithilfe des Hilfsprogramms WinHTTP [**proxycfg.exe**](proxycfg-exe--a-proxy-configuration-tool.md) abzurufen. Nachdem die Registrierungseinstellungen für einen einzelnen Benutzer geladen wurden, führt die Anwendung die unter [Die Anwendung wird in einem Benutzerkonto ausgeführten](#the-application-is-running-on-a-user-account) Schritte aus, um den Proxynamen und die Proxyumgehungsserver festzulegen.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Festlegen der Proxykonfiguration für eine einzelne Anforderung

Bevor die Sitzung erstellt wird, ruft die Anwendung [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) auf, um zu bestimmen, ob WinINet und IE für die Verwendung von WPAD konfiguriert sind. **WinHttpGetIEProxyConfigForCurrentUser** gibt die [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) zurück, die den **fAutoDetect-Member** enthält. Der Wert **TRUE** für diesen Member gibt an, dass WPAD verwendet wird, und das **lpszAutoConfigUrl-Element** enthält die WPAD-URL.

## <a name="automatic-proxy-configuration-is-used"></a>Automatische Proxykonfiguration wird verwendet

Wenn WPAD verwendet wird, ruft die Anwendung [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) auf, um den Proxy für die Anforderung abzurufen. Der *lpwszUrl-Parameter* enthält die URL, an die die Anforderung gesendet wird, und der *pAutoProxyOptions-Parameter* enthält einen Zeiger auf die Struktur ([**WINHTTP \_ AUTOPROXY \_ OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)), die die Autoproxyoptionen enthält. Die Anwendung initialisiert die **WINHTTP \_ AUTOPROXY \_ OPTIONS-Struktur** mit den Einstellungen, die von der [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) im Aufruf von [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)zurückgegeben werden. Das **WINHTTP \_ AUTOPROXY \_ CONFIG \_ URL-Flag** wird im **dwFlags-Member** der **WINHTTP \_ AUTOPROXY \_ OPTIONS-Struktur** angegeben, und das **lpszAutoconfigUrl-Element** enthält die Proxy-URL für die automatische Konfiguration aus der **WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG-Struktur.** Die **WinHttpGetProxyForUrl-Funktion** gibt den Proxynamen und die Proxyumgehungsliste in den **Membern lpszProxy** und **lpszProxyBypass** der [**WINHTTP \_ PROXY \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) zurück.

Nachdem der Proxy für die Anforderung von [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)abgerufen wurde, erstellt die Anwendung die Anforderung mit [**WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) Anschließend wird [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) aufgerufen, um den Proxy für die Anforderung festzulegen, indem das Anforderungshandle im *hInternet-Parameter* angegeben wird. Der *dwOption-Parameter* im Aufruf von **WinHttpSetOption** sollte auf **WINHTTP \_ OPTION \_ PROXY** festgelegt werden, und der *lpBuffer-Parameter* ist ein Zeiger auf eine [**WINHTTP PROXY \_ \_ INFO-Struktur,**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) die den Proxy und die Proxyumgehung enthält, die für die Anforderung verwendet werden sollen.

## <a name="automatic-proxy-configuration-is-not-used"></a>Die automatische Proxykonfiguration wird nicht verwendet.

Wenn der Aufruf von [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) angibt, dass autoproxy nicht verwendet wird, kann die Anwendung die Anforderung einfach mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellen. Die Proxykonfiguration ist für die gesamte Sitzung identisch, und anforderungsspezifische Änderungen sind nicht erforderlich.

 

 



