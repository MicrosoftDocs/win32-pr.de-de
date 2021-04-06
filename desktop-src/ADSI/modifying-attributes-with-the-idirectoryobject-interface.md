---
title: Ändern von Attributen mit der IDirectoryObject-Schnittstelle
description: Zusätzlich zu IADs Put und IADs PutEx können Sie die IDirectoryObject setobjectattributes-Methode verwenden, um Attributwerte zu ändern. Um diese Methode verwenden zu können, müssen Sie \_ \_ für jedes zu ändernde Attribut eine ADS attr Info-Struktur ausfüllen.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Ändern von Attributen mit der IDirectoryObject-Schnittstelle ADSI
- IDirectoryObject ADSI, verwenden zum Ändern von Attributen
- ADSI ADSI, Beispiel Code C/C++, verwenden von IDirectoryObject zum Ändern von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715826d0fc835f3d9ecae914fcc51603883af5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100563"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="b97d6-107">Ändern von Attributen mit der IDirectoryObject-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b97d6-107">Modifying Attributes with the IDirectoryObject Interface</span></span>

<span data-ttu-id="b97d6-108">Zusätzlich zu [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex)können Sie die [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode verwenden, um Attributwerte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b97d6-108">In addition to [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex), you can use the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method to modify attribute values.</span></span> <span data-ttu-id="b97d6-109">Um diese Methode verwenden zu können, müssen Sie für jedes zu ändernde Attribut eine [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="b97d6-109">To use this method, you must fill in an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure for each attribute to modify.</span></span>

<span data-ttu-id="b97d6-110">Mit der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode können Sie sowohl einwertige als auch mehrwertige Attribute ändern.</span><span class="sxs-lookup"><span data-stu-id="b97d6-110">The [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method enables you to modify both single-valued and multi-valued attributes.</span></span> <span data-ttu-id="b97d6-111">Diese Funktion bietet ähnliche operative Steuerelemente, wie z. b. Clear, Append, DELETE und Update, die in der [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="b97d6-111">This function provides similar operational controls, such as clear, append, delete, and update, to those found in the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span> <span data-ttu-id="b97d6-112">Die Steuerelement Konstanten umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b97d6-112">The control constants include:</span></span>

-   [<span data-ttu-id="b97d6-113">**ADS ist \_ \_ klar**</span><span class="sxs-lookup"><span data-stu-id="b97d6-113">**ADS\_ATTR\_CLEAR**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="b97d6-114">**ADS- \_ \_ Update**</span><span class="sxs-lookup"><span data-stu-id="b97d6-114">**ADS\_ATTR\_UPDATE**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="b97d6-115">**Werbung \_ \_ Anfügen**</span><span class="sxs-lookup"><span data-stu-id="b97d6-115">**ADS\_ATTR\_APPEND**</span></span>](adsi-attribute-modification-types.md)
-   [<span data-ttu-id="b97d6-116">**ADS- \_ \_ Löschung**</span><span class="sxs-lookup"><span data-stu-id="b97d6-116">**ADS\_ATTR\_DELETE**</span></span>](adsi-attribute-modification-types.md)

<span data-ttu-id="b97d6-117">Wenn Sie [**ADS \_ attr \_ Update**](adsi-attribute-modification-types.md) angeben, wird ein serverseitiger Vorgang, der ressourcenintensiv sein kann, auslöst.</span><span class="sxs-lookup"><span data-stu-id="b97d6-117">Specifying [**ADS\_ATTR\_UPDATE**](adsi-attribute-modification-types.md) will trigger a server side operation that can be resource-intensive.</span></span> <span data-ttu-id="b97d6-118">Ein Beispiel wäre, den Vorgang zum Aktualisieren einer langen Liste von Gruppenmitgliedschaften zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="b97d6-118">An example would be to initiate the operation to update a long list of group membership.</span></span> <span data-ttu-id="b97d6-119">Im Allgemeinen sollten Sie diesen Vorgang nicht verwenden, es sei denn, die Änderung umfasst eine kleine Anzahl von Attributen im Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b97d6-119">In general, refrain from using this operation unless the modification involves a small number of attributes in the directory.</span></span> <span data-ttu-id="b97d6-120">Um eine lange Liste der Gruppenmitgliedschaften zu ändern, ist es effizienter, die Liste aus dem zugrunde liegenden Verzeichnis zu lesen, Änderungen vorzunehmen und die aktualisierte Liste wieder in das Verzeichnis zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b97d6-120">To modify a long list of group memberships, the more efficient approach would be to read the list from the underlying directory, make modifications, and store the updated list back to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="b97d6-121">Wie [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) mit [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)werden die Attribut Änderungen entweder vollständig committet oder in Active Directory verworfen.</span><span class="sxs-lookup"><span data-stu-id="b97d6-121">Like [**IADs::Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) with [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), the attribute changes are either completely committed or discarded in Active Directory.</span></span> <span data-ttu-id="b97d6-122">Wenn eine oder mehrere der Änderungen nicht zulässig sind und daher nicht ausgeführt werden können, wird für keine der an den Attributen vorgenommenen Änderungen ein Commit an das Verzeichnis übertragen.</span><span class="sxs-lookup"><span data-stu-id="b97d6-122">If one or more of the modifications are not allowed and therefore not able to be performed, then none of the collective modifications made to the attributes are committed to the directory.</span></span>

 

## <a name="example"></a><span data-ttu-id="b97d6-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b97d6-123">Example</span></span>

<span data-ttu-id="b97d6-124">Im folgenden Codebeispiel wird gezeigt, wie ein-Attribut und ein mehr wertiges Attribut mit der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b97d6-124">The following code example shows how to modify both single and multi-valued attributes with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span>


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 




