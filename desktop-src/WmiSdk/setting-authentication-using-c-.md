---
description: Eine der Hauptaufgaben von IWbemLocator::ConnectServer für WMI ist die Rückgabe eines Zeigers auf einen IWbemServices-Proxy.
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Festlegen der Authentifizierung mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b0ef3bcd1e9908815c94dacc3815fec77eaea33f2da48119dbe3178563eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315617"
---
# <a name="setting-authentication-using-c"></a>Festlegen der Authentifizierung mit C++

Eine der Hauptaufgaben von [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) für WMI ist die Rückgabe eines Zeigers auf einen [**IWbemServices-Proxy.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Über den **IWbemServices-Proxy** können Sie auf die Funktionen der WMI-Infrastruktur zugreifen. Der Zeiger auf den **IWbemServices-Proxy** verfügt jedoch über die Identität des Clientanwendungsprozesses und nicht über die Identität des **IWbemServices-Prozesses.** Wenn Sie versuchen, mit dem Zeiger auf **IWbemServices** zu zugreifen, können Sie daher einen Zugriffs verweigerten Code erhalten, z. B. **E \_ ACCESSDENIED**. Um den Fehler "Zugriff verweigert" zu vermeiden, müssen Sie die Identität des neuen Zeigers mit einem Aufruf der [**CoSetProxyBlanket-Schnittstelle**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festlegen.

Ein Anbieter kann die Sicherheit für einen Namespace so festlegen, dass keine Daten zurückgegeben werden, es sei denn, Sie verwenden den Paketdatenschutz **(PktPrivacy)** in Ihrer Verbindung mit diesem Namespace. Dadurch wird sichergestellt, dass Daten verschlüsselt werden, wenn sie das Netzwerk überqueren. Wenn Sie versuchen, eine niedrigere Authentifizierungsebene zu setzen, erhalten Sie die Meldung Zugriff verweigert. Weitere Informationen finden Sie unter [Festlegen von Namepace-Sicherheitsdeskriptoren.](setting-namespace-security-descriptors.md)

Weitere Informationen zum Festlegen der Authentifizierung bei der Skripterstellung finden Sie unter [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Festlegen der Sicherheit auf einer Remote-IUnknown-Schnittstelle

In einigen Situationen ist mehr Zugriff auf einen Server als nur ein Zeiger auf einen Proxy erforderlich. Manchmal müssen Sie möglicherweise eine sichere Verbindung mit der [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) des Proxys herstellen. Mithilfe **von IUnknown** können Sie das Remotesystem nach Schnittstellen und anderen erforderlichen Techniken abfragen.

Wenn sich ein Proxy auf einem Remotecomputer befindet, delegiert der Server alle Aufrufe an die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) des Proxys an die **IUnknown-Schnittstelle.** Wenn Sie beispielsweise [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für einen Proxy aufrufen und die angeforderte Schnittstelle nicht Teil des Proxys war, sendet der Proxy den Aufruf an den Remoteserver. Der Remoteserver sucht wiederum nach der entsprechenden Schnittstellenunterstützung. Wenn der Server die Schnittstelle unterstützt, marshallt COM einen neuen Proxy zurück an den Client, damit die Anwendung die neue Schnittstelle verwenden kann.

Probleme treten auf, wenn der Client nicht über Zugriffsberechtigungen für den Remoteserver verfügt, aber die Anmeldeinformationen eines Benutzers verwendet, der dies tut. In diesem Fall schlägt jeder Versuch fehl, auf [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf dem Remoteserver zu zugreifen. Das endgültige Release auf dem Proxy schlägt auch fehl, da der aktuelle Benutzer keinen Zugriff auf den Remoteserver hat. Ein Symptom dafür ist eine Verzögerung von einer oder zwei Sekunden, bevor die Clientanwendung das endgültige Proxy release nicht unterstützt. Der Fehler tritt auf, weil COM versucht hat, mithilfe der Standardsicherheitseinstellungen des aktuellen Benutzers auf den Remoteserver zu zugreifen, die nicht die geänderten Anmeldeinformationen enthalten, die den Zugriff auf den Server von Anfang an erlaubt haben. Weitere Informationen finden Sie unter Setting the Security on IWbemServices and Other Proxys (Festlegen der Sicherheit für [IWbemServices und andere Proxys).](setting-the-security-on-iwbemservices-and-other-proxies.md)

Um die fehlerhafte Verbindung zu vermeiden, verwenden Sie [**CoSetProxyBlanket,**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) um die Sicherheitsauthentifizierung explizit für den Zeiger fest, der von [**IUnknown zurückgegeben wird.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Mit **coSetProxyBlanket** können Sie sicherstellen, dass der Remoteserver die richtige Authentifizierungsidentität erhält.

Das folgende Codebeispiel zeigt, wie [**CoSetProxyBlanket für**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) den Zugriff auf eine [**IUnknown-Remoteschnittstelle verwendet**](/windows/win32/api/unknwn/nn-unknwn-iunknown) wird.


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> Wenn Sie die Sicherheit für die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) eines Proxys festlegen, erstellt COM eine Kopie des Proxys, die erst freigegeben werden kann, wenn Sie [**CoUninitialize aufrufen.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Authentifizierung in WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
