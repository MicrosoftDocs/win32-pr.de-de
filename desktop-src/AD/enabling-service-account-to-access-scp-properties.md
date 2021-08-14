---
title: Aktivieren des Dienstkontos für den Zugriff auf SCP-Eigenschaften
description: Im folgenden Codebeispiel wird ein Paar von Access Control Einträgen (ACEs) für ein Dienstverbindungspunktobjekt (Service Connection Point, SCP) festgelegt.
ms.assetid: 663dcf55-5f0d-49af-8b51-4c1e35b79ef1
ms.tgt_platform: multiple
keywords:
- Aktivieren des Dienstkontos für den Zugriff auf SCP Properties AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260b08d4a7255813e2811c02ebd0e597a518f153db84f35cdb978a44369e5e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695309"
---
# <a name="enabling-service-account-to-access-scp-properties"></a>Aktivieren des Dienstkontos für den Zugriff auf SCP-Eigenschaften

Im folgenden Codebeispiel wird ein Paar von Access Control Einträgen (ACEs) für ein Dienstverbindungspunktobjekt (Service Connection Point, SCP) festgelegt. Die ACEs gewähren Lese-/Schreibzugriff auf das Benutzer- oder Computerkonto, unter dem die Dienstinstanz ausgeführt wird. Das Dienstinstallationsprogramm verwendet Code ähnlich dem folgenden, um sicherzustellen, dass der Dienst seine Eigenschaften zur Laufzeit aktualisieren kann. Wenn acEs ähnlich wie diese nicht festgelegt sind, hat der Dienst keinen Zugriff auf die Eigenschaften des SCP.

In der Regel legt ein Dienstinstallationsprogramm diese ACEs nach dem Erstellen des SCP-Objekts fest. Weitere Informationen und ein Codebeispiel, das einen SCP erstellt und diese Funktion aufruft, finden Sie unter [Suchen und Verwenden eines Dienstverbindungspunkts](how-clients-find-and-use-a-service-connection-point.md)durch Clients. Wenn der Dienst für die Ausführung unter einem anderen Konto neu konfiguriert ist, müssen die ACEs aktualisiert werden. Um erfolgreich ausgeführt zu werden, muss dieses Codebeispiel im Sicherheitskontext eines Domänenadministrators ausgeführt werden.

Der erste Parameter der Beispielfunktion gibt den Namen des Benutzerkontos an, dem Zugriff gewährt werden soll. Die Funktion geht davon aus, dass der Name im UserName-Format *Domäne* **\\** _vorliegt._ Wenn kein Konto angegeben wird, geht die Funktion davon aus, dass der Dienst das LocalSystem-Konto verwendet. Dies bedeutet, dass die Funktion Zugriff auf das Computerkonto des Hostservers gewähren muss, auf dem der Dienst ausgeführt wird. Zu diesem Zweck ruft das Codebeispiel die [**GetComputerObjectName-Funktion**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) auf, um die Domäne und den Benutzernamen des lokalen Computers abzurufen.

Das folgende Codebeispiel kann geändert werden, um dem Dienst Vollzugriff auf das SCP-Objekt zu gewähren. Die bewährte Methode besteht jedoch darin, nur die spezifischen Zugriffsrechte zu gewähren, die der Dienst zur Laufzeit benötigt. In diesem Fall gewährt die Funktion Zugriff auf zwei Eigenschaften.



| Eigenschaft                                                              | Beschreibung                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [**serviceDNSName**](/windows/desktop/ADSchema/a-servicednsname)                       | Der Name des Hostservers, auf dem der Dienst ausgeführt wird.         |
| [**serviceBindingInformation**](/windows/desktop/ADSchema/a-servicebindinginformation) | Private Bindungsinformationen, die der Dienst beim Start aktualisiert. |



 

Jede Eigenschaft wird durch die **schemaIDGUID** der **attributeSchema-Klasse** der Eigenschaft identifiziert. Jede Eigenschaft im Schema verfügt über ein eigenes eindeutiges **schemaIDGUID-Objekt.** Im folgenden Codebeispiel werden Zeichenfolgen verwendet, um die GUIDs anzugeben. Die GUID-Zeichenfolgen weisen das folgende Format auf, wobei jedes "X" durch eine Hexadezimalziffer ersetzt wird: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}.

Die **schemaIDGUID-Werte,** die den Eigenschaften zugewiesen sind, auf die der Zugriff gewährt oder verweigert werden soll, finden Sie auf den Referenzseiten des Active Directory-Schemas.

Im folgenden Codebeispiel werden die Schnittstellen [**IADsSecurityDescriptor,**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) verwendet, um die folgenden Vorgänge auszuführen.

1.  Rufen Sie den Sicherheitsdeskriptor des SCP-Objekts ab.
2.  Legen Sie die entsprechenden ACEs in der DACL (Discretionary Access Control List) des Sicherheitsdeskriptors fest.
3.  Ändern Sie die Sicherheitsbeschreibung des SCP-Objekts.


```C++
#include <atlbase.h>

//******************************
//
//  AllowAccessToScpProperties()
//
//******************************

HRESULT AllowAccessToScpProperties(
    LPWSTR wszAccountSAM,   // Service account to allow access.
    IADs *pSCPObject)       // IADs pointer to the SCP object.
{
    HRESULT hr = E_FAIL;
    IADsAccessControlList *pACL = NULL;
    IADsSecurityDescriptor *pSD = NULL;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE1 = NULL;
    IADsAccessControlEntry *pACE2 = NULL;
    IDispatch *pDispACE = NULL;
    long lFlags = 0L;
    CComBSTR sbstrTrustee;
    CComBSTR sbstrSecurityDescriptor = L"nTSecurityDescriptor";
    VARIANT varSD;

    if(NULL == pSCPObject)
    {
        return E_INVALIDARG;
    }
    
    VariantInit(&varSD);
     
    /*
    If no service account is specified, service runs under 
    LocalSystem. Allow access to the computer account of the 
    service's host.
    */
    if (wszAccountSAM) 
    {
        sbstrTrustee = wszAccountSAM;
    }
    else
    {
        LPWSTR pwszComputerName;
        DWORD dwLen;
        
        // Get the size required for the SAM account name.
        dwLen = 0;
        GetComputerObjectNameW(NameSamCompatible, 
            NULL, &dwLen);
        
        pwszComputerName = new WCHAR[dwLen + 1];
        if(NULL == pwszComputerName)
        {
            hr = E_OUTOFMEMORY;
            goto cleanup;
        }

        /*
        Get the SAM account name of the computer object for 
        the server.
        */
        if(!GetComputerObjectNameW(NameSamCompatible,
            pwszComputerName, &dwLen))
        {
            delete pwszComputerName;
            
            hr = HRESULT_FROM_WIN32(GetLastError());
            goto cleanup;
        }

        sbstrTrustee = pwszComputerName;
        wprintf(L"GetComputerObjectName: %s\n", pwszComputerName);
        delete pwszComputerName;
    } 

    // Get the nTSecurityDescriptor.
    hr = pSCPObject->Get(sbstrSecurityDescriptor, &varSD);
    if (FAILED(hr) || (varSD.vt != VT_DISPATCH)) 
    {
        _tprintf(TEXT("Get nTSecurityDescriptor failed: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    /*
    Use the V_DISPATCH macro to get the IDispatch pointer from 
    VARIANT structure and QueryInterface for an 
    IADsSecurityDescriptor pointer.
    */
    hr = V_DISPATCH( &varSD )->QueryInterface(
        IID_IADsSecurityDescriptor,
        (void**)&pSD);
    if (FAILED(hr)) 
    {
        _tprintf(
            TEXT("Cannot get IADsSecurityDescriptor: 0x%x\n"), 
            hr);
        goto cleanup;
    } 
     
    /*
    Get an IADsAccessControlList pointer to the security 
    descriptor's DACL.
    */
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(
            IID_IADsAccessControlList,
            (void**)&pACL);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot get DACL: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Create the COM object for the first ACE.
    hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE1);
     
    // Create the COM object for the second ACE.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE2);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot create ACEs: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Set the properties of the two ACEs.
                                
    // Allow read and write access to the property.
    hr = pACE1->put_AccessMask(
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
    hr = pACE2->put_AccessMask( 
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
                                
    // Set the trustee, which is either the service account or the 
    // host computer account.
    hr = pACE1->put_Trustee( sbstrTrustee );
    hr = pACE2->put_Trustee( sbstrTrustee );
                                
    // Set the ACE type.
    hr = pACE1->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
    hr = pACE2->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
                                
    // Set AceFlags to zero because ACE is not inheritable.
    hr = pACE1->put_AceFlags( 0 );
    hr = pACE2->put_AceFlags( 0 );
     
    // Set Flags to indicate an ACE that protects a specified object.
    hr = pACE1->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
    hr = pACE2->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
     
    // Set ObjectType to the schemaIDGUID of the attribute.
    // serviceDNSName
    hr = pACE1->put_ObjectType( 
        L"{28630eb8-41d5-11d1-a9c1-0000f80367c1}"); 
    // serviceBindingInformation
    hr = pACE2->put_ObjectType( 
        L"{b7b1311c-b82e-11d0-afee-0000f80367c1}"); 
     
    /*
    Add the ACEs to the DACL. Need an IDispatch pointer for 
    each ACE to pass to the AddAce method.
    */
    hr = pACE1->QueryInterface(IID_IDispatch,(void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add first ACE: 0x%x\n"), hr);
        goto cleanup;
    }
    else 
    {
        if (pDispACE)
            pDispACE->Release();
    
        pDispACE = NULL;
    }
     
    // Repeat for the second ACE.
    hr = pACE2->QueryInterface(IID_IDispatch, (void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add second ACE: 0x%x\n"), hr);
        goto cleanup;
    }
     
    // Write the modified DACL back to the security descriptor.
    hr = pSD->put_DiscretionaryAcl(pDisp);
    if (SUCCEEDED(hr))
    {
        /*
        Write the ntSecurityDescriptor property to the 
        property cache.
        */
        hr = pSCPObject->Put(sbstrSecurityDescriptor, varSD);
        if (SUCCEEDED(hr))
        {
            // SetInfo updates the SCP object in the directory.
            hr = pSCPObject->SetInfo();
        }
    }
                                    
    cleanup:
    if (pDispACE)
        pDispACE->Release();
                        
    if (pACE1)
        pACE1->Release();
                    
    if (pACE2)
        pACE2->Release();
                    
    if (pACL)
        pACL->Release();
               
    if (pDisp)
        pDisp->Release();
            
    if (pSD)
        pSD->Release();
 
    VariantClear(&varSD);
 
    return hr;
}
```



 

 