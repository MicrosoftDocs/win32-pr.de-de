---
description: 'In C++ können Sie die Sicherheit für den gesamten Prozess festlegen, indem Sie CoInitializeSecurity aufrufen, bevor Sie eine Verbindung mit WMI über IWbemLocator:: ConnectServer herstellen.'
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Festlegen der Sicherheit für IWbemServices und andere Proxys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d593c52091182b1f0580908624e0b4068ed3f8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360847"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Festlegen der Sicherheit für IWbemServices und andere Proxys

In C++ können Sie die Sicherheit für den gesamten Prozess festlegen, indem Sie [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, bevor Sie eine Verbindung mit WMI über [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)herstellen. Sie können auch die Authentifizierungs Ebene, die Identitätswechsel Ebene oder den Authentifizierungsdienst in einem Aufruf ändern, der einen Zeiger auf einen WMI-Proxy (z. b. [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) oder [**iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)) erhält. Durch Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) können Sie auch den Authentifizierungsdienst (Kerberos, NTLM oder aushandeln) ändern.

Skripts und Visual Basic Anwendungen legen die Sicherheit für Proxys nur indirekt durch Aufrufe von [**Swap Services**](swbemservices.md) und anderen Automatisierungs Objekten fest. Weitere Informationen zum Festlegen und Ändern der Authentifizierung und des Identitäts Wechsels in Skripts finden [Sie unter Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

Beim Herstellen einer Verbindung mit WMI auf einem Remote Computer, auf dem ein anderes Betriebssystem ausgeführt wird, ist das Ändern von Sicherheitsstufen oder Diensten vor allem von Bedeutung. Weitere Informationen finden Sie unter [Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Eine Client Anwendung stellt eine Verbindung mit einem WMI-Proxy mithilfe einer Identität her. Eine Identität ist ein Datenobjekt, das aus den Einstellungen Benutzername, Kennwort und Autorität besteht. Bei einer WMI-Client Anwendung wird durch den-Befehl an die [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Schnittstelle die anfängliche Identität erstellt. Die Methode [**ConnectServer**](swbemlocator-connectserver.md) übernimmt die Identität in einem Satz von drei Parametern, die Sie auf **null** festlegen können, um den aktuellen Benutzer anzugeben. Sie können auch einen nicht-**null** -Parameter angeben, um einen bestimmten Benutzer und eine bestimmte Domäne anzugeben. Wenn der-Vorgang erfolgreich ist, gibt **ConnectServer** einen Zeiger zurück, über den Sie auf eine Vielzahl von Remote Prozessen zugreifen können, z. b. auf einen WMI-Dienst oder das Windows-Betriebssystem.

Wie viele COM-Schnittstellen gibt [**ConnectServer**](swbemlocator-connectserver.md) einen Zeiger auf einen Proxy zurück. Bei einem Proxy handelt es sich um ein Datenobjekt, das einen Remote Prozess darstellt, z. b. WMI oder einen Remote Anbieter. COM verwendet einen Proxy, um Entwicklern den Zugriff auf Remote Daten zu ermöglichen, als wären die Daten lokal.

Die folgenden WMI-Schnittstellen verwenden Proxys:

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) (Skript Objekt für [**Austausch**](swbemservices.md) Vorgänge)
-   [**Ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**Iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**Iwbemaktualisierer**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) (Skript Objekt für [**Austausch**](swbemrefresher.md) Vorgänge)

    Das WMI-Aktualisierungs Programm ist ein Sonderfall, da es einen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger gibt, dessen Sicherheitseinstellungen ordnungsgemäß festgelegt werden müssen. Weitere Informationen zum Verwenden von Aktualisierungs Objekten finden Sie unter [zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md).

Nachdem Sie einen Zeiger auf einen Remote Prozess erhalten haben, können Sie eine von zwei Aktionen ausführen. Wenn Sie wissen, wie der Prozess funktioniert, können Sie festlegen, dass die Sicherheit für den Zeiger festgelegt wird, und auf den Prozess normal zugreifen. Dies ist der Fall bei den meisten Zeigern auf einen WMI-Dienst. Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md). Alternativ müssen Sie auf eine andere COM-Schnittstelle auf dem Proxy zugreifen, z. b. [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), indem Sie die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Proxys aufrufen.

## <a name="defaults-and-recommendations"></a>Standardwerte und Empfehlungen

Die verteilte Version des Component Object Model (DCOM) aushandelt den Standard Authentifizierungsdienst (Kerberos, NTLM oder Aushandlung), und Sie können den Standard Authentifizierungsdienst nicht mithilfe von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)angeben. Wenn Sie den **RPC \_ C \_ authn \_ default** im Authentifizierungsdienst Parameter von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) angeben, kann DCOM den entsprechenden Dienst auswählen. Bei Remote Verbindungen wird der Standard Dienst ausgehandelt. Dies ist der empfohlene Dienst für Anwendungen, die in Kerberos-und nicht-Kerberos-Domänen funktionieren. Für lokale Verbindungen ist der Standard Authentifizierungsdienst NT-LAN-Manager (NTLM).

Das folgende Codebeispiel zeigt den verwendeten Standard Authentifizierungsdienst.


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



Für das Codebeispiel in diesem Thema sind die folgenden Referenz-und \# include-Anweisungen erforderlich.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Bei der Skripterstellung wird empfohlen, die Standardwerte zu verwenden, die von DCOM für Remote Aufrufe ausgewählt werden. Auf dem lokalen Computer können Sie keinen Authentifizierungsdienst für Aufrufe von WMI angeben. Weitere Informationen finden Sie unter [Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript](setting-the-authentication-service-using-vbscript.md) und [Erstellen einer Monikerzeichenfolge](constructing-a-moniker-string.md).

 

 
