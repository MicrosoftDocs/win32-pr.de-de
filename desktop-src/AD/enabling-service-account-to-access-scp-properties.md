---
title: Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften
description: Im folgenden Codebeispiel wird ein paar von Access Control Einträgen (ACEs) für ein Dienst Verbindungspunkt-Objekt (Service Connection Point, SCP) festgelegt.
ms.assetid: 663dcf55-5f0d-49af-8b51-4c1e35b79ef1
ms.tgt_platform: multiple
keywords:
- Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49adcd1b4747b1c13a64a5af54c6cc6a42e6afe
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858149"
---
# <a name="enabling-service-account-to-access-scp-properties"></a>Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften

Im folgenden Codebeispiel wird ein paar von Access Control Einträgen (ACEs) für ein Dienst Verbindungspunkt-Objekt (Service Connection Point, SCP) festgelegt. Die ACEs gewähren Lese-/Schreibzugriff auf das Benutzer-oder Computer Konto, unter dem die Dienst Instanz ausgeführt wird. Das Dienst Installationsprogramm verwendet Code ähnlich dem folgenden, um sicherzustellen, dass der Dienst seine Eigenschaften zur Laufzeit aktualisieren kann. Wenn ACEs ähnlich diesen nicht festgelegt sind, hat der Dienst keinen Zugriff auf die Eigenschaften des Dienst Verbindungs Punkts.

In der Regel legt ein Dienst Installationsprogramm diese ACEs fest, nachdem das SCP-Objekt erstellt wurde. Weitere Informationen und ein Codebeispiel, in dem ein SCP erstellt und diese Funktion aufgerufen wird, [finden Sie unter wie Clients einen Dienst Verbindungspunkt suchen und verwenden](how-clients-find-and-use-a-service-connection-point.md). Wenn der Dienst für die Durchführung unter einem anderen Konto neu konfiguriert wird, müssen die ACEs aktualisiert werden. Dieses Codebeispiel muss im Sicherheitskontext eines Domänen Administrators ausgeführt werden, damit es erfolgreich ausgeführt werden kann.

Der erste Parameter der Beispiel Funktion gibt den Namen des Benutzerkontos an, dem der Zugriff gewährt werden soll. Die Funktion geht davon aus, dass der Name im Format des *Domänen ***\\*** Benutzernamens* Wenn kein Konto angegeben ist, geht die Funktion davon aus, dass der Dienst das LocalSystem-Konto verwendet. Dies bedeutet, dass die Funktion Zugriff auf das Computer Konto des Host Servers gewähren muss, auf dem der-Dienst ausgeführt wird. Zu diesem Zweck Ruft das Codebeispiel die [**getcomputerobjectname**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) -Funktion auf, um die Domäne und den Benutzernamen des lokalen Computers abzurufen.

Das folgende Codebeispiel kann geändert werden, um dem Dienst Vollzugriff auf das SCP-Objekt zu gewähren. es wird jedoch empfohlen, nur die spezifischen Zugriffsrechte zu erteilen, die der Dienst zur Laufzeit benötigt. In diesem Fall gewährt die Funktion Zugriff auf zwei Eigenschaften.



| Eigenschaft                                                              | BESCHREIBUNG                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [**serviceDNSName**](/windows/desktop/ADSchema/a-servicednsname)                       | Der Name des Host Servers, auf dem der Dienst ausgeführt wird.         |
| [**serviceBindingInformation**](/windows/desktop/ADSchema/a-servicebindinginformation) | Informationen zur privaten Bindung, die vom Dienst beim Starten aktualisiert werden. |



 

Jede Eigenschaft wird durch die **schemaIdGUID** der **attributeSchema** -Klasse der Eigenschaft identifiziert. Jede Eigenschaft im Schema weist eine eigene eindeutige **schemaIdGUID** auf. Im folgenden Codebeispiel werden Zeichen folgen verwendet, um die GUIDs anzugeben. Die GUID-Zeichen folgen weisen das folgende Format auf, wobei jedes "X" durch eine hexadezimale Ziffer ersetzt wird: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}.

Auf den Active Directory Schema-Referenzseiten finden Sie die **schemaIdGUID** -Werte, die den Eigenschaften zugewiesen sind, um den Zugriff zu gewähren oder zu verweigern.

Im folgenden Codebeispiel werden die Schnittstellen [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) verwendet, um die folgenden Vorgänge auszuführen.

1.  Rufen Sie die Sicherheits Beschreibung des SCP-Objekts ab.
2.  Legen Sie die entsprechenden ACEs in der Zugriffs Steuerungs Liste (DACL) der Sicherheits Beschreibung fest.
3.  Ändern Sie die Sicherheits Beschreibung des SCP-Objekts.


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



 

 