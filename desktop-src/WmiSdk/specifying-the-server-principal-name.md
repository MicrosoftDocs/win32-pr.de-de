---
description: Der Kerberos-Authentifizierungsdienst gibt den Server Prinzipal Namen an, um die Identität des Computers sicherzustellen, mit dem die Verbindung hergestellt wird.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Angeben des Server Prinzipal namens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131004"
---
# <a name="specifying-the-server-principal-name"></a>Angeben des Server Prinzipal namens

Der Kerberos-Authentifizierungsdienst gibt den Server Prinzipal Namen an, um die Identität des Computers sicherzustellen, mit dem die Verbindung hergestellt wird. Geben Sie den Server Prinzipal Namen im aufzurufenden Skript für die Skript Methode " [**taubemlocator. ConnectServer**](swbemlocator-connectserver.md) " an, indem Sie den Namen des Remote Computers eingeben. Geben Sie in C++ den Server Prinzipal Namen im *pserverprincname* -Parameter an, wenn Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) für den Proxy aufrufen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

Dieser Parameter ist für Kerberos erforderlich, um die gegenseitige Authentifizierung zu unterstützen. Allerdings lässt die Verwendung des standardmäßigen Server Prinzipal namens keine gegenseitige Authentifizierung zu. Clients, für die die gegenseitige Authentifizierung wichtig ist, müssen einen Server Prinzipal Namen angeben, der mit der Server Identität übereinstimmt, die vom WMI-Dienst verwendet wird. Weitere Informationen zum Festlegen der Proxy Sicherheit und ein C++-Beispiel, das zeigt, wie der Server Prinzipal Name festgelegt wird, finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.

Weitere Informationen zum Festlegen des Server Prinzipal namens im Skript und Visual Basic finden Sie unter "WS- [**Locator. ConnectServer**](swbemlocator-connectserver.md) " und [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

Im Gegensatz zu den meisten Sicherheitsprotokollen für Windows-Verwaltungsinstrumentation (WMI) und Component Object Model (com) können Sie den Server Prinzipal nicht in einem [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)-aufrufswert festlegen. Sie können jedoch den Server Prinzipal mit dem *bstrauauthority* -Parameter für [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)oder dem *pserverprincname* -Parameter für [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)festlegen.

Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.


```C++
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird gezeigt, wie der Server Prinzipal Name mit [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)festgelegt wird.


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen des Authentifizierungs Dienstanbieter mithilfe von VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Festlegen der Authentifizierung mithilfe von C++](setting-authentication-using-c-.md)
</dt> <dt>

[Festlegen der Sicherheit für IWbemServices und andere Proxys](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
