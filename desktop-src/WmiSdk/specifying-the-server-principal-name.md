---
description: Der Kerberos-Authentifizierungsdienst gibt den Serverprinzipalnamen an, um die Identität des Computers sicherzustellen, mit dem eine Verbindung hergestellt wird.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Angeben des Serverprinzipalnamens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b3d05d6933653a7d2a1737d36f00f6ca65c39bd7739e5f2e9f4232eb507f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816423"
---
# <a name="specifying-the-server-principal-name"></a>Angeben des Serverprinzipalnamens

Der Kerberos-Authentifizierungsdienst gibt den Serverprinzipalnamen an, um die Identität des Computers sicherzustellen, mit dem eine Verbindung hergestellt wird. Geben Sie den Serverprinzipalnamen im Aufruf der Skriptmethode [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) an, indem Sie den Namen des Remotecomputers angeben. Geben Sie in C++ den Serverprinzipalnamen im *Parameter pServerPrincName* an, wenn [**Sie CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) für den Proxy aufrufen. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

Dieser Parameter ist erforderlich, damit Kerberos die gegenseitige Authentifizierung unterstützt. Die Verwendung des Standardnamens des Serverprinzipals lässt jedoch keine gegenseitige Authentifizierung zu. Clients, für die gegenseitige Authentifizierung wichtig ist, müssen einen Serverprinzipalnamen angeben, der mit der Serveridentität übereinstimmt, die der WMI-Dienst verwendet. Weitere Informationen zum Festlegen der Proxysicherheit und ein C++-Beispiel zum Festlegen des Serverprinzipalnamens finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere Proxys.](setting-the-security-on-iwbemservices-and-other-proxies.md)

Weitere Informationen zum Festlegen des Serverprinzipalnamens im Skript und Visual Basic finden Sie unter [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) und [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

Im Gegensatz zu den meisten Sicherheitsprotokollen für Windows Management Instrumentation (WMI) und Component Object Model (COM) können Sie den Serverprinzipal nicht in einem Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)festlegen. Sie können den Serverprinzipal jedoch mit dem *bstrAuthority-Parameter* für [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)oder dem *Parameter pServerPrincName* für [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)festlegen.

Das Codebeispiel in diesem Thema erfordert die folgende \# include-Anweisung, um ordnungsgemäß zu kompilieren.


```C++
#include <wbemidl.h>
```



Das folgende Codebeispiel zeigt, wie der Serverprinzipalname mit ConnectServer festgelegt [**wird.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)


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

[Festlegen des Authentifizierungsdiensts mit VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Festlegen der Authentifizierung mit C++](setting-authentication-using-c-.md)
</dt> <dt>

[Festlegen der Sicherheit für IWbemServices und andere Proxys](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
