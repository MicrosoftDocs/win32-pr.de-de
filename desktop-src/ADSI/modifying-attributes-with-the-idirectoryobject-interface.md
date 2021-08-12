---
title: Ändern von Attributen mit der IDirectoryObject-Schnittstelle
description: Zusätzlich zu IADs Put und IADs PutEx können Sie die IDirectoryObject SetObjectAttributes-Methode verwenden, um Attributwerte zu ändern. Um diese Methode zu verwenden, müssen Sie eine ADS \_ ATTR \_ INFO-Struktur für jedes zu ändernde Attribut ausfüllen.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Ändern von Attributen mit der IDirectoryObject-Schnittstelle ADSI
- IDirectoryObject ADSI , verwenden zum Ändern von Attributen
- ADSI ADSI , Beispielcode C/C++, Verwenden von IDirectoryObject zum Ändern von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fa7d75d3e0dce489f676dafb36992c95a1cba2e9856bbbaf49f14806a6c1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179028"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Ändern von Attributen mit der IDirectoryObject-Schnittstelle

Zusätzlich zu [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex)können Sie die [**IDirectoryObject::SetObjectAttributes-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) verwenden, um Attributwerte zu ändern. Um diese Methode zu verwenden, müssen Sie eine [**ADS \_ ATTR \_ INFO-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) für jedes zu ändernde Attribut ausfüllen.

Mit [**der IDirectoryObject::SetObjectAttributes-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) können Sie sowohl einwertige als auch mehrwertige Attribute ändern. Diese Funktion stellt ähnliche betriebsbereite Steuerelemente wie Clear, Append, Delete und Update für diejenigen bereit, die in der [**IADs::P utEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-putex) gefunden werden. Zu den Steuerelementkonstanten gehören:

-   [**ADS \_ ATTR \_ CLEAR**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ UPDATE**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ APPEND**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ DELETE**](adsi-attribute-modification-types.md)

Die Angabe von [**ADS \_ ATTR \_ UPDATE**](adsi-attribute-modification-types.md) löst einen serverseitigen Vorgang aus, der ressourcenintensiv sein kann. Ein Beispiel wäre das Initiieren des Vorgangs zum Aktualisieren einer langen Liste von Gruppenmitgliedschaften. Im Allgemeinen sollten Sie diesen Vorgang nicht verwenden, es sei denn, die Änderung umfasst eine kleine Anzahl von Attributen im Verzeichnis. Um eine lange Liste von Gruppenmitgliedschaften zu ändern, besteht der effizientere Ansatz darin, die Liste aus dem zugrunde liegenden Verzeichnis zu lesen, Änderungen vorzunehmen und die aktualisierte Liste wieder im Verzeichnis zu speichern.

> [!Note]  
> Wie [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) mit [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)werden die Attributänderungen in Active Directory entweder vollständig ausgeführt oder verworfen. Wenn eine oder mehrere der Änderungen nicht zulässig sind und daher nicht ausgeführt werden können, wird für keine der an den Attributen vorgenommenen gemeinsamen Änderungen ein Commit für das Verzeichnis ausgeführt.

 

## <a name="example"></a>Beispiel

Das folgende Codebeispiel zeigt, wie Sie sowohl einzelne als auch mehrwertige Attribute mit der [**IDirectoryObject::SetObjectAttributes-Methode**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) ändern.


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



 

 




