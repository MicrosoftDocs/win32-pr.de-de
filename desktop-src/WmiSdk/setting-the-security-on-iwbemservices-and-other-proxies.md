---
description: In C++ können Sie die Sicherheit für den gesamten Prozess festlegen, indem Sie CoInitializeSecurity aufrufen, bevor Sie über IWbemLocator::ConnectServer eine Verbindung mit WMI herstellen.
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Festlegen der Sicherheit für IWbemServices und andere Proxys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da997b9d4a8f91cf31e8619af983209d4a07a571932c85304d372379d7f752b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050268"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Festlegen der Sicherheit für IWbemServices und andere Proxys

In C++ können Sie die Sicherheit für den gesamten Prozess festlegen, indem Sie [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, bevor Sie über [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)eine Verbindung mit WMI herstellen. Sie können auch die Authentifizierungsebene, die Identitätswechselebene oder den Authentifizierungsdienst in einem Aufruf ändern, der einen Zeiger auf einen WMI-Proxy abruft, z. B. [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) oder [**IWbemCallResult.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) Wenn [**Sie CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) aufrufen, können Sie auch den Authentifizierungsdienst (Kerberos, NTLM oder Negotiate) ändern.

Skripts und Visual Basic Anwendungen legen die Sicherheit für Proxys nur indirekt durch Aufrufe von [**SWbemServices**](swbemservices.md) und anderen Automatisierungsobjekten fest. Weitere Informationen zum Festlegen und Ändern der Authentifizierung und des Identitätswechsels im Skript finden Sie unter [Festlegen der Standardprozesssicherheitsstufe mit VBScript.](setting-the-default-process-security-level-using-vbscript.md)

Das Ändern von Sicherheitsebenen oder -diensten ist in erster Linie ein Problem, wenn eine Verbindung mit WMI auf einem Remotecomputer hergestellt wird, auf dem ein anderes Betriebssystem ausgeführt wird. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen.](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)

Eine Clientanwendung stellt mithilfe einer Identität eine Verbindung mit einem WMI-Proxy her. Eine Identität ist ein Datenobjekt, das aus einem Benutzernamen, einem Kennwort und Autoritätseinstellungen besteht. Bei einer WMI-Clientanwendung wird durch den Aufruf der [**IWbemLocator::ConnectServer-Schnittstelle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) die anfängliche Identität erstellt. Die [**ConnectServer-Methode**](swbemlocator-connectserver.md) verwendet die Identität in einem Satz von drei Parametern, die Sie auf **NULL** festlegen können, um den aktuellen Benutzer anzugeben. Sie können auch einen Parameter ungleich **NULL** angeben, um einen bestimmten Benutzer und eine bestimmte Domäne anzugeben. Wenn der Aufruf erfolgreich ist, gibt **ConnectServer** einen Zeiger zurück, über den Sie direkt auf eine Vielzahl von Remoteprozessen zugreifen können, z. B. einen WMI-Dienst oder das Windows Betriebssystem.

Wie viele COM-Schnittstellen gibt [**ConnectServer**](swbemlocator-connectserver.md) einen Zeiger auf einen Proxy zurück. Ein Proxy ist ein Datenobjekt, das einen Remoteprozess darstellt, z. B. WMI oder einen Remoteanbieter. COM verwendet einen Proxy, um Entwicklern den Zugriff auf Remotedaten zu ermöglichen, als wären die Daten lokal.

Die folgenden WMI-Schnittstellen verwenden Proxys:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ([**SWbemServices-Skriptobjekt)**](swbemservices.md)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) ([**SWbemRefresher-Skriptobjekt)**](swbemrefresher.md)

    Die WMI-Aktualisierung ist ein Sonderfall, da ihr ein [**IWbemServices-Zeiger**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) übergeben wird, dessen Sicherheitseinstellungen ordnungsgemäß festgelegt werden müssen. Weitere Informationen zur Verwendung von Aktualisierungsobjekten finden Sie unter [Zugreifen auf Leistungsdaten in C++.](accessing-performance-data-in-c--.md)

Nachdem Sie einen Zeiger auf einen Remoteprozess erhalten haben, können Sie zwei Dinge tun. Wenn Sie wissen, was der Prozess macht, können Sie die Sicherheit für den Zeiger festlegen und normal auf den Prozess zugreifen. Dies ist bei den meisten Zeigern auf einen WMI-Dienst der Fall. Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung.](setting-the-security-levels-on-a-wmi-connection.md) Alternativ müssen Sie über einen Aufruf der [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) auf dem Proxy auf eine andere COM-Schnittstelle wie [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)zugreifen.

## <a name="defaults-and-recommendations"></a>Standardwerte und Empfehlungen

Die verteilte Version des Component Object Model (DCOM) handelt den Standardauthentifizierungsdienst (Kerberos, NTLM oder Negotiate) aus, und Sie können den Standardauthentifizierungsdienst nicht mit [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)angeben. Wenn **Sie RPC \_ C \_ AUTHN \_ DEFAULT** im Authentifizierungsdienstparameter von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) angeben, kann DCOM den entsprechenden Dienst auswählen. Für Remoteverbindungen ist der Standarddienst Negotiate. Dies ist der empfohlene Dienst für Anwendungen, die sowohl in Kerberos- als auch in Nicht-Kerberos-Domänen funktionieren. Für lokale Verbindungen ist der Standardauthentifizierungsdienst NT LAN Manager (NTLM).

Das folgende Codebeispiel zeigt den verwendeten Standardauthentifizierungsdienst.


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



Das Codebeispiel in diesem Thema erfordert den folgenden Verweis und \# include-Anweisungen.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Für die Skripterstellung wird empfohlen, die Standardwerte zu verwenden, die DCOM für Remoteaufrufe auswählt. Auf dem lokalen Computer können Sie keinen Authentifizierungsdienst für WMI-Aufrufe angeben. Weitere Informationen finden Sie unter [Festlegen des Authentifizierungsdiensts mit VBScript](setting-the-authentication-service-using-vbscript.md) und [Erstellen einer Monikerzeichenfolge.](constructing-a-moniker-string.md)

 

 
