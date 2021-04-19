---
description: 'Eine der Hauptaufgaben von IWbemLocator:: ConnectServer für WMI ist die Rückgabe eines Zeigers auf einen IWbemServices-Proxy.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Festlegen der Authentifizierung mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349518"
---
# <a name="setting-authentication-using-c"></a>Festlegen der Authentifizierung mithilfe von C++

Eine der Hauptaufgaben von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) für WMI ist die Rückgabe eines Zeigers auf einen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy. Über den **IWbemServices** -Proxy können Sie auf die Funktionen der WMI-Infrastruktur zugreifen. Der Zeiger auf den **IWbemServices** -Proxy hat jedoch die Identität des Client Anwendungsprozesses und nicht die Identität des **IWbemServices** -Prozesses. Wenn Sie also versuchen, mit dem-Zeiger auf **IWbemServices** zuzugreifen, können Sie einen Zugriff verweigerten Code wie z. b. " **E \_ AccessDenied**" erhalten. Um den Fehler "Zugriff verweigert" zu vermeiden, müssen Sie die Identität des neuen Zeigers mit einem Aufrufen der [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) -Schnittstelle festlegen.

Ein Anbieter kann die Sicherheit für einen Namespace so festlegen, dass keine Daten zurückgegeben werden, es sei denn, Sie verwenden den Paket Datenschutz (**PKTPRIVACY**) in der Verbindung mit diesem Namespace. Dadurch wird sichergestellt, dass die Daten beim Überschreiten des Netzwerks verschlüsselt werden. Wenn Sie versuchen, eine niedrigere Authentifizierungs Ebene festzulegen, erhalten Sie die Meldung "Zugriff verweigert". Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).

Weitere Informationen zum Festlegen der Authentifizierung bei der Skripterstellung finden [Sie unter Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Festlegen der Sicherheit für eine IUnknown-Remote Schnittstelle

In einigen Situationen ist mehr Zugriff auf einen Server als nur ein Zeiger auf einen Proxy erforderlich. Manchmal müssen Sie möglicherweise eine sichere Verbindung mit der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Proxys herstellen. Mithilfe von **IUnknown** können Sie das Remote System nach Schnittstellen und anderen notwendigen Techniken Abfragen.

Wenn sich ein Proxy auf einem Remote Computer befindet, delegiert der Server alle Aufrufe an die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Proxys an die **IUnknown** -Schnittstelle. Wenn Sie z. b. [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf einem Proxy aufzurufen und die angeforderte Schnittstelle nicht Teil des Proxys ist, sendet der Proxy den-Aufrufe an den Remote Server. Der Remote Server überprüft wiederum die entsprechende Schnittstellen Unterstützung. Wenn der Server die-Schnittstelle unterstützt, Marshalls com einen neuen Proxy zurück an den Client, damit die Anwendung die neue-Schnittstelle verwenden kann.

Es treten Probleme auf, wenn der Client keine Zugriffsberechtigungen für den Remote Server hat, sondern die Anmelde Informationen eines Benutzers verwendet, der das verwendet. In dieser Situation tritt beim Versuch, auf die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf dem Remote Server zuzugreifen, ein Fehler auf. Die endgültige Version des Proxys schlägt ebenfalls fehl, da der aktuelle Benutzer keinen Zugriff auf den Remote Server hat. Ein Symptom hierfür ist eine Verzögerung von einem oder zwei Sekunden, bevor die Client Anwendung die endgültige Proxy Version misslingt. Der Fehler tritt auf, weil com versucht hat, unter Verwendung der Standard Sicherheitseinstellungen des aktuellen Benutzers auf den Remote Server zuzugreifen, die nicht die geänderten Anmelde Informationen enthalten, die den Zugriff auf den Server an erster Stelle zugelassen haben. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.

Um die fehlgeschlagene Verbindung zu vermeiden, legen Sie mit [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) die Sicherheits Authentifizierung für den von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)zurückgegebenen Zeiger explizit fest. Mithilfe von **CoSetProxyBlanket** können Sie sicherstellen, dass der Remote Server die richtige Authentifizierungs Identität erhält.

Im folgenden Codebeispiel wird gezeigt, wie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) verwendet wird, um auf eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Remote Schnittstelle zuzugreifen.


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
> Wenn Sie die Sicherheit für die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle eines Proxys festlegen, erstellt com eine Kopie des Proxys, die nicht freigegeben werden kann, bis Sie die [**entiinitialisierung**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)aufruft.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Authentifizierung in WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
