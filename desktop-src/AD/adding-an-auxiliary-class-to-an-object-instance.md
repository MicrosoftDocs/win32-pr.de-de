---
title: Hinzufügen einer Hilfsklasse zu einer Objektinstanz
description: In den folgenden Codebeispielen wird veranschaulicht, wie ADSI und LDAP verwendet werden, um einer vorhandenen Objektinstanz dynamisch eine Hilfsklasse hinzuzufügen.
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038810"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a>Hinzufügen einer Hilfsklasse zu einer Objektinstanz

In den folgenden Codebeispielen wird veranschaulicht, wie ADSI und LDAP verwendet werden, um einer vorhandenen Objektinstanz dynamisch eine Hilfsklasse hinzuzufügen. In den Beispielen wird davon ausgegangen, dass eine zusätzliche Klasse mit dem Namen **Vehicle** im Active Directory Schema definiert ist und dass die **Vehicle** -Klasse über ein **Vin** -Attribut verfügt.

Wenn Sie einer Objektinstanz dynamisch eine Hilfsklasse hinzufügen, müssen Sie gleichzeitig Werte für alle obligatorischen **musthave** -Attribute in der-Klasse angeben. In den folgenden Beispielen wird gezeigt, wie Sie dies mit dem "Vin"-Attribut durchführen, das als obligatorisch angesehen wird.

Das folgende C++-Beispiel bindet an ein-Objekt und verwendet [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) , um die Erweiterungs Klasse an die Liste der Klassen in der **objectClass** -Eigenschaft des Objekts anzufügen. Im Beispiel wird " [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put) " verwendet, um den Wert des " **Vin** "-Attributs festzulegen. Schließlich wird " [**IADs. abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) " aufgerufen, um die Änderungen im Verzeichnis zu übertragen.


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 