---
title: Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle
description: Die IDirectoryObject-Schnittstelle stellt eine in C und C++ geschriebene Clientanwendung mit direktem Zugriff auf Verzeichnisdienstobjekte bereit.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle ADSI
- IDirectoryObject ADSI , Zugreifen auf Attribute mit
- ADSI ADSI mithilfe der IDirectoryObject-Schnittstelle für den Zugriff auf Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fb7f2b8302c2e92a7e604bdc85389fb78acb24a59e467ca42b8bbd3c6c004e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181539"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle

Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) stellt eine in C und C++ geschriebene Clientanwendung mit direktem Zugriff auf Verzeichnisdienstobjekte bereit. Die Schnittstelle ermöglicht den Zugriff über ein direktes Netzwerkprotokoll und nicht über den ADSI-Attributcache. Statt der eigenschaften, die von der [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) unterstützt werden, stellt **IDirectoryObject** Methoden bereit, die eine kritische Teilmenge der Wartungsmethoden eines Objekts unterstützen und Zugriff auf seine Attribute bieten. Mit **IDirectoryObject kann** ein Client eine beliebige Anzahl von Objektattributen mit einem Methodenaufruf erhalten oder festlegen. Im Gegensatz zu den entsprechenden Automation-Methoden, die in Batches ausgeführt werden, werden die **von IDirectoryObject** ausgeführt, wenn sie aufgerufen werden. Da Methoden auf dieser Schnittstelle keine Instanz eines Automation-Verzeichnisobjekts erstellen müssen, ist der Leistungsaufwand gering.

Clients, die in Sprachen wie C und C++ geschrieben wurden, sollten die Methoden der [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) verwenden, um die Leistung zu optimieren und native Verzeichnisdienstschnittstellen zu nutzen. Automation-Clients können **IDirectoryObject nicht verwenden.** Stattdessen sollten sie die [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) verwenden.

Die [**IDirectoryObject::GetObjectAttributes-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) ruft Attribute mit einzelnen und mehreren Werten ab. Diese Methode verwendet eine Liste der angeforderten Attribute und gibt eine [**ADS \_ ATTR \_ INFO-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) zurück. ADSI ordnet diese Struktur zu. Der Aufrufer muss diesen Arbeitsspeicher frei geben, wenn er mit der [**FreeADsMem-Funktion nicht mehr benötigt**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) wird.

Die Reihenfolge der zurückgegebenen Attributwerte ist nicht notwendigerweise mit der Reihenfolge identisch, in der die Attribute angefordert wurden. Daher ist es erforderlich, die von ADSI zurückgegebenen Attributnamen zu vergleichen.

> [!Note]  
> Die [**ADS \_ ATTR \_ INFO-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) gibt nicht alle angeforderten Attribute zurück. Nur die Attribute, die Werte enthalten, sind Teil der zurückgegebenen -Struktur.

 

Die Anzahl der zurückgegebenen Attribute wird durch den *dwNumberAttributes-Parameter* bestimmt, der an die [**IDirectoryObject::GetObjectAttributes-Methode übergeben**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) wird.

Im folgenden Codebeispiel wird an ein -Objekt gebunden und die [**IDirectoryObject::GetObjectAttributes-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) verwendet, um Attribute des Objekts abzurufen.


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




