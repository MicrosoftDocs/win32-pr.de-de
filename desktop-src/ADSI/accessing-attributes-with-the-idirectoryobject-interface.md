---
title: Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle
description: Die IDirectoryObject-Schnittstelle stellt eine Client Anwendung bereit, die in C und C++ mit direktem Zugriff auf Verzeichnisdienst Objekte geschrieben wurde.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle ADSI
- IDirectoryObject ADSI, zugreifen auf Attribute mit
- ADSI ADSI, using mithilfe der IDirectoryObject-Schnittstelle für den Zugriff auf Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947369"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a>Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle

Die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle stellt eine Client Anwendung bereit, die in C und C++ mit direktem Zugriff auf Verzeichnisdienst Objekte geschrieben wurde. Die-Schnittstelle ermöglicht den Zugriff mithilfe eines direkten Netzwerk Protokolls anstelle des ADSI-Attribut Caches. Anstelle der Eigenschaften, die von der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle unterstützt werden, stellt **IDirectoryObject** Methoden bereit, die eine kritische Teilmenge der Wartungsmethoden eines Objekts unterstützen und Zugriff auf seine Attribute bereitstellen. Mit **IDirectoryObject** kann ein Client eine beliebige Anzahl von Objekt Attributen mit einem Methoden Befehl Abrufen oder festlegen. Im Gegensatz zu den entsprechenden Automatisierungsmethoden, die als Batch verarbeitet werden, werden die von **IDirectoryObject** beim Aufrufen von ausgeführt. Da für Methoden in dieser Schnittstelle das Erstellen einer Instanz eines Automation-Verzeichnis Objekts nicht erforderlich ist, ist der Leistungs Aufwand gering.

Clients, die in Sprachen wie C und C++ geschrieben wurden, sollten die Methoden der [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle verwenden, um die Leistung zu optimieren und die systemeigenen Verzeichnisdienst Schnittstellen zu nutzen. Automatisierungs Clients können **IDirectoryObject** nicht verwenden. Stattdessen sollten Sie die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle verwenden.

Die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode ruft Attribute mit einem einzelnen und mehreren Werten ab. Diese Methode nimmt eine Liste der angeforderten Attribute an und gibt eine [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur zurück. ADSI ordnet diese Struktur zu. der Aufrufer muss diesen Arbeitsspeicher freigeben, wenn er nicht mehr benötigt wird, indem die [**freeadsmem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) -Funktion verwendet wird.

Die Reihenfolge der zurückgegebenen Attributwerte ist nicht notwendigerweise identisch mit der Reihenfolge, in der die Attribute angefordert wurden. Daher ist es erforderlich, die von ADSI zurückgegebenen Attributnamen zu vergleichen.

> [!Note]  
> Die [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur gibt nicht alle angeforderten Attribute zurück. Nur die Attribute, die Werte enthalten, sind Teil der zurückgegebenen Struktur.

 

Die Anzahl der zurückgegebenen Attribute wird durch den *dwnumberattributes* -Parameter bestimmt, der an die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode übergeben wird.

Das folgende Codebeispiel bindet an ein-Objekt und verwendet die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode, um Attribute des-Objekts abzurufen.


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



 

 




