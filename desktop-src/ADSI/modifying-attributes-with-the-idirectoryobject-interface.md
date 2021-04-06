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
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Ändern von Attributen mit der IDirectoryObject-Schnittstelle

Zusätzlich zu [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex)können Sie die [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode verwenden, um Attributwerte zu ändern. Um diese Methode verwenden zu können, müssen Sie für jedes zu ändernde Attribut eine [**ADS \_ attr \_ Info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) -Struktur ausfüllen.

Mit der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode können Sie sowohl einwertige als auch mehrwertige Attribute ändern. Diese Funktion bietet ähnliche operative Steuerelemente, wie z. b. Clear, Append, DELETE und Update, die in der [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode gefunden werden. Die Steuerelement Konstanten umfassen Folgendes:

-   [**ADS ist \_ \_ klar**](adsi-attribute-modification-types.md)
-   [**ADS- \_ \_ Update**](adsi-attribute-modification-types.md)
-   [**Werbung \_ \_ Anfügen**](adsi-attribute-modification-types.md)
-   [**ADS- \_ \_ Löschung**](adsi-attribute-modification-types.md)

Wenn Sie [**ADS \_ attr \_ Update**](adsi-attribute-modification-types.md) angeben, wird ein serverseitiger Vorgang, der ressourcenintensiv sein kann, auslöst. Ein Beispiel wäre, den Vorgang zum Aktualisieren einer langen Liste von Gruppenmitgliedschaften zu initiieren. Im Allgemeinen sollten Sie diesen Vorgang nicht verwenden, es sei denn, die Änderung umfasst eine kleine Anzahl von Attributen im Verzeichnis. Um eine lange Liste der Gruppenmitgliedschaften zu ändern, ist es effizienter, die Liste aus dem zugrunde liegenden Verzeichnis zu lesen, Änderungen vorzunehmen und die aktualisierte Liste wieder in das Verzeichnis zu speichern.

> [!Note]  
> Wie [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) mit [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)werden die Attribut Änderungen entweder vollständig committet oder in Active Directory verworfen. Wenn eine oder mehrere der Änderungen nicht zulässig sind und daher nicht ausgeführt werden können, wird für keine der an den Attributen vorgenommenen Änderungen ein Commit an das Verzeichnis übertragen.

 

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird gezeigt, wie ein-Attribut und ein mehr wertiges Attribut mit der [**IDirectoryObject:: setobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) -Methode geändert werden.


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



 

 




