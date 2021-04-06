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
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="0ea64-106">Zugreifen auf Attribute mit der IDirectoryObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0ea64-106">Accessing Attributes With the IDirectoryObject Interface</span></span>

<span data-ttu-id="0ea64-107">Die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle stellt eine Client Anwendung bereit, die in C und C++ mit direktem Zugriff auf Verzeichnisdienst Objekte geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="0ea64-107">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface provides a client application written in C and C++ with direct access to directory service objects.</span></span> <span data-ttu-id="0ea64-108">Die-Schnittstelle ermöglicht den Zugriff mithilfe eines direkten Netzwerk Protokolls anstelle des ADSI-Attribut Caches.</span><span class="sxs-lookup"><span data-stu-id="0ea64-108">The interface enables access by means of a direct network protocol, rather than through the ADSI attribute cache.</span></span> <span data-ttu-id="0ea64-109">Anstelle der Eigenschaften, die von der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle unterstützt werden, stellt **IDirectoryObject** Methoden bereit, die eine kritische Teilmenge der Wartungsmethoden eines Objekts unterstützen und Zugriff auf seine Attribute bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ea64-109">In place of the properties supported by the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface, **IDirectoryObject** provides methods that support a critical subset of an object's maintenance methods and provide access to its attributes.</span></span> <span data-ttu-id="0ea64-110">Mit **IDirectoryObject** kann ein Client eine beliebige Anzahl von Objekt Attributen mit einem Methoden Befehl Abrufen oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="0ea64-110">With **IDirectoryObject**, a client can get or set any number of object attributes with one method call.</span></span> <span data-ttu-id="0ea64-111">Im Gegensatz zu den entsprechenden Automatisierungsmethoden, die als Batch verarbeitet werden, werden die von **IDirectoryObject** beim Aufrufen von ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ea64-111">Unlike the corresponding Automation methods, which are batched, those of **IDirectoryObject** are executed when called.</span></span> <span data-ttu-id="0ea64-112">Da für Methoden in dieser Schnittstelle das Erstellen einer Instanz eines Automation-Verzeichnis Objekts nicht erforderlich ist, ist der Leistungs Aufwand gering.</span><span class="sxs-lookup"><span data-stu-id="0ea64-112">Because methods on this interface do not require creating an instance of an Automation directory object, the performance overhead is small.</span></span>

<span data-ttu-id="0ea64-113">Clients, die in Sprachen wie C und C++ geschrieben wurden, sollten die Methoden der [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle verwenden, um die Leistung zu optimieren und die systemeigenen Verzeichnisdienst Schnittstellen zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="0ea64-113">Clients written in languages such as C and C++ should use the methods of the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface to optimize performance and take advantage of native directory service interfaces.</span></span> <span data-ttu-id="0ea64-114">Automatisierungs Clients können **IDirectoryObject** nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ea64-114">Automation clients cannot use **IDirectoryObject**.</span></span> <span data-ttu-id="0ea64-115">Stattdessen sollten Sie die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ea64-115">Instead, they should use the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>

<span data-ttu-id="0ea64-116">Die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode ruft Attribute mit einem einzelnen und mehreren Werten ab.</span><span class="sxs-lookup"><span data-stu-id="0ea64-116">The [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method retrieves attributes with both single and multiple values.</span></span> <span data-ttu-id="0ea64-117">Diese Methode nimmt eine Liste der angeforderten Attribute an und gibt eine [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="0ea64-117">This method takes a list of requested attributes and returns an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure.</span></span> <span data-ttu-id="0ea64-118">ADSI ordnet diese Struktur zu. der Aufrufer muss diesen Arbeitsspeicher freigeben, wenn er nicht mehr benötigt wird, indem die [**freeadsmem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ea64-118">ADSI allocates this structure; the caller must free this memory when it is no longer required using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="0ea64-119">Die Reihenfolge der zurückgegebenen Attributwerte ist nicht notwendigerweise identisch mit der Reihenfolge, in der die Attribute angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="0ea64-119">The order of returned attribute values is not necessarily the same as the order in which the attributes were requested.</span></span> <span data-ttu-id="0ea64-120">Daher ist es erforderlich, die von ADSI zurückgegebenen Attributnamen zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="0ea64-120">Therefore, it is necessary to compare the attribute names returned from ADSI.</span></span>

> [!Note]  
> <span data-ttu-id="0ea64-121">Die [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur gibt nicht alle angeforderten Attribute zurück.</span><span class="sxs-lookup"><span data-stu-id="0ea64-121">The [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure does not return all of the attributes requested.</span></span> <span data-ttu-id="0ea64-122">Nur die Attribute, die Werte enthalten, sind Teil der zurückgegebenen Struktur.</span><span class="sxs-lookup"><span data-stu-id="0ea64-122">Only those attributes that contain values are part of the returned structure.</span></span>

 

<span data-ttu-id="0ea64-123">Die Anzahl der zurückgegebenen Attribute wird durch den *dwnumberattributes* -Parameter bestimmt, der an die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0ea64-123">The number of attributes returned is determined by the *dwNumberAttributes* parameter passed to the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>

<span data-ttu-id="0ea64-124">Das folgende Codebeispiel bindet an ein-Objekt und verwendet die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) -Methode, um Attribute des-Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0ea64-124">The following code example binds to an object and uses the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve attributes of the object.</span></span>


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



 

 




