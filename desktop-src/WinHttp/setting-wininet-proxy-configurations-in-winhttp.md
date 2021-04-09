---
description: Anwendungen, die von WinInet zu WinHTTP portieren, müssen möglicherweise dieselben aktivierter automatischer Proxy-Einstellungen verwenden, die Sie unter WinInet oder Internet Explorer (IE) abrufen können.
ms.assetid: c3e867d8-9d67-4e6a-8551-1fa846e089ed
title: Festlegen von WinInet-Proxy Konfigurationen in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91306f6591e0aab0f96fa010ee2a83d3f32c8fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960798"
---
# <a name="setting-wininet-proxy-configurations-in-winhttp"></a>Festlegen von WinInet-Proxy Konfigurationen in WinHTTP

## <a name="setting-automatic-proxy-on-winhttp-51"></a>Festlegen des automatischen Proxys unter WinHTTP 5,1

Anwendungen, die von WinInet zu WinHTTP portieren, müssen möglicherweise dieselben aktivierter automatischer Proxy-Einstellungen verwenden, die Sie unter WinInet oder Internet Explorer (IE) abrufen können. Die WinHTTP-API, Version 5,1, kann diese Proxy Einstellungen abrufen und verwenden. Im Allgemeinen gibt WinHTTP die Proxy-und Proxy Umgehungs Server auf Sitzungs Basis an, wenn die Sitzung erstellt wird. Diese Einstellungen können auf Anforderungs Basis überschrieben werden.

Um dieselbe Proxykonfiguration wie WinInet oder IE zu verwenden, sollte der WinHTTP-Client Proxy Einstellungen für die Sitzung festlegen. Wenn IE oder WinInet für die Verwendung von Web Proxy Auto-Discovery (WPAD) konfiguriert ist, muss der WinHTTP-Client, der diese Einstellungen verwendet, die Proxy Einstellungen pro Anforderung festlegen. In den folgenden Abschnitten wird beschrieben, wie Sie die Proxy Einstellungen für eine Sitzung und eine Anforderung angeben:

-   [Festlegen der Proxy Konfiguration für eine Sitzung](#setting-the-proxy-configuration-on-a-session)
-   [Festlegen der Proxy Konfiguration für eine einzelne Anforderung](#setting-the-proxy-configuration-on-a-single-request)

## <a name="setting-the-proxy-configuration-on-a-session"></a>Festlegen der Proxy Konfiguration für eine Sitzung

## <a name="the-application-is-running-on-a-user-account"></a>Die Anwendung wird auf einem Benutzerkonto ausgeführt.

Bevor eine Sitzung erstellt wird, ruft die Anwendung [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) auf, um die Internet Explorer-Proxy Einstellungen zu erhalten. Die Anwendung muss als Benutzerkonto ausgeführt werden, um diese Einstellungen zu erhalten. Der *pproxyconfig* -Parameter ist ein Zeiger auf eine aktuelle WinHTTP-Benutzer-/proxykonfigurationsstruktur, die den Proxy Namen (*lpszProxy*) und Proxy Umgehungs Server (*lpszProxyBypass*) enthält. [**\_ \_ \_ \_ \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) Der Proxy Name und die Proxy Umgehungs Werte der Kontext Konfigurations Struktur des **aktuellen WinHTTP- \_ \_ Benutzers \_ \_ \_** werden dann verwendet, um die WinHTTP-Sitzung zu initialisieren. Die Sitzung wird durch Aufrufen von [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) mit den Parametern *pwszproxyname* und *pwszproxybypass* initialisiert, die von den **lpszProxy** -und **lpszProxyBypass** -Membern der Konfigurations Struktur des **aktuellen WinHTTP- \_ Benutzers ( \_ \_ IE \_ \_** ) abgerufen wurden.

## <a name="the-application-is-running-as-a-service"></a>Die Anwendung wird als Dienst ausgeführt.

Die Anwendung muss sicherstellen, dass die Registrierungs Einstellungen für einen einzelnen Benutzer in die Registrierung geladen werden, bevor [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)aufgerufen wird. Wenn diese Einstellungen nicht in die Registrierung geladen werden, kann **WinHttpGetIEProxyConfigForCurrentUser** die Proxy Einstellungen nicht abrufen. Registrierungs Einstellungen für einen einzelnen Benutzer können durch Aufrufen der **LoadUserProfile** -Funktion in die Registrierung geladen werden. Wenn das Laden der Registrierungs Einstellungen des Benutzers keine Option ist, kann die Anwendung [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) mit dem **Standard Proxy für den WinHTTP- \_ \_ Zugriffstyp \_ \_** aufrufen, der im *dwacesstype* -Parameter angegeben ist. Das Angeben des Standard Proxys im Aufrufen von **WinHttpOpen** weist die WinHTTP-API an, den Proxy Konfigurationssatz mithilfe des WinHTTP- [**proxycfg.exe**](proxycfg-exe--a-proxy-configuration-tool.md) Hilfsprogramms abzurufen. Nachdem die Registrierungs Einstellungen für einen einzelnen Benutzer geladen wurden, führt die Anwendung die unter [der Anwendung wird auf einem Benutzerkonto ausgeführt wird](#the-application-is-running-on-a-user-account) beschriebenen Schritte aus, um den Proxy Namen und die Proxy Umgehungs Server festzulegen.

## <a name="setting-the-proxy-configuration-on-a-single-request"></a>Festlegen der Proxy Konfiguration für eine einzelne Anforderung

Bevor die Sitzung erstellt wird, ruft die Anwendung [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) auf, um zu ermitteln, ob WinInet und IE für die Verwendung von WPAD konfiguriert sind. **WinHttpGetIEProxyConfigForCurrentUser** gibt die Struktur des [**aktuellen WinHTTP- \_ Benutzers der IE- \_ \_ \_ Proxy \_ Konfiguration**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) zurück, die das **fAutoDetect** -Element enthält. Der Wert **true** für diesen Member gibt an, dass WPAD verwendet wird und der Member **lpszAutoConfigUrl** die WPAD-URL enthält.

## <a name="automatic-proxy-configuration-is-used"></a>Automatische Proxy Konfiguration wird verwendet

Wenn WPAD verwendet wird, ruft die Anwendung [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) zum Abrufen des Proxys für die Anforderung auf. Der *lpwszurl* -Parameter enthält die URL, an die die Anforderung gesendet wird, und der Parameter " *pautoproxyoptions* " enthält einen Zeiger auf die Struktur ([**WinHTTP \_ aktivierter automatischer Proxy- \_ Optionen**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)), die die aktivierter automatischer Proxy-Optionen enthält. Die Anwendung initialisiert die **WinHTTP \_ AutoProxy \_ options** -Struktur mit den Einstellungen, die von der WinHTTP-Struktur des [**\_ aktuellen \_ Benutzers der IE- \_ \_ Proxy \_ Konfiguration**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) im Aufrufen von [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)zurückgegeben werden. Das Flag " **WinHTTP \_ AutoProxy \_ config \_ URL** " ist im **dwFlags** -Member der **WinHTTP- \_ AutoProxy \_ options** -Struktur angegeben, und das **lpszAutoConfigUrl** -Element enthält die URL für die automatische Proxykonfiguration aus der **\_ \_ \_ \_ \_ Konfigurations Struktur des aktuellen WinHTTP-Benutzers** . Die **WinHttpGetProxyForUrl** -Funktion gibt den Proxy Namen und die Proxy Umgehungs Liste in den **lpszProxy** -und **lpszProxyBypass** -Membern der [**WinHTTP- \_ Proxy \_ Info**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) -Struktur zurück.

Nachdem der Proxy für die Anforderung von [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)abgerufen wurde, erstellt die Anwendung die Anforderung mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Anschließend wird " [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) " aufgerufen, um den Proxy für die Anforderung festzulegen, indem das Anforderungs Handle im *HINTERNET* -Parameter angegeben wird. Der Parameter " *dwOption* " im Aufrufen von " **WinHttpSetOption** " sollte auf die **WinHTTP- \_ Option " \_ Proxy** " festgelegt werden, und der *lpBuffer* -Parameter ist ein Zeiger auf eine [**WinHTTP- \_ Proxy \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) Struktur, die den Proxy und die Proxy Umgehung enthält, die für die Anforderung verwendet werden.

## <a name="automatic-proxy-configuration-is-not-used"></a>Die automatische Proxy Konfiguration wird nicht verwendet.

Wenn der Aufrufen von [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) anzeigt, dass aktivierter automatischer Proxy nicht verwendet wird, kann die Anwendung die Anforderung einfach mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)erstellen. Die Proxykonfiguration ist für die gesamte Sitzung identisch, und Anforderungs spezifische Änderungen sind nicht erforderlich.

 

 



