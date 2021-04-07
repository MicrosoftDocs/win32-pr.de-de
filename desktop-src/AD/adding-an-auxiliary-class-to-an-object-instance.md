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
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a><span data-ttu-id="7d5b2-103">Hinzufügen einer Hilfsklasse zu einer Objektinstanz</span><span class="sxs-lookup"><span data-stu-id="7d5b2-103">Adding an Auxiliary Class to an Object Instance</span></span>

<span data-ttu-id="7d5b2-104">In den folgenden Codebeispielen wird veranschaulicht, wie ADSI und LDAP verwendet werden, um einer vorhandenen Objektinstanz dynamisch eine Hilfsklasse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d5b2-104">The following code examples show how to use ADSI and LDAP to dynamically add an auxiliary class to an existing object instance.</span></span> <span data-ttu-id="7d5b2-105">In den Beispielen wird davon ausgegangen, dass eine zusätzliche Klasse mit dem Namen **Vehicle** im Active Directory Schema definiert ist und dass die **Vehicle** -Klasse über ein **Vin** -Attribut verfügt.</span><span class="sxs-lookup"><span data-stu-id="7d5b2-105">The examples assume that an auxiliary class named **vehicle** is defined in the Active Directory schema, and that the **vehicle** class has a **vin** attribute.</span></span>

<span data-ttu-id="7d5b2-106">Wenn Sie einer Objektinstanz dynamisch eine Hilfsklasse hinzufügen, müssen Sie gleichzeitig Werte für alle obligatorischen **musthave** -Attribute in der-Klasse angeben.</span><span class="sxs-lookup"><span data-stu-id="7d5b2-106">When you dynamically add an auxiliary class to an object instance, you must simultaneously specify values for any mandatory **mustHave** attributes in the class.</span></span> <span data-ttu-id="7d5b2-107">In den folgenden Beispielen wird gezeigt, wie Sie dies mit dem "Vin"-Attribut durchführen, das als obligatorisch angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="7d5b2-107">The following examples show how to do this with the "vin" attribute, which is assumed to be mandatory.</span></span>

<span data-ttu-id="7d5b2-108">Das folgende C++-Beispiel bindet an ein-Objekt und verwendet [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) , um die Erweiterungs Klasse an die Liste der Klassen in der **objectClass** -Eigenschaft des Objekts anzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d5b2-108">The following C++ example binds to an object, and uses [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) to append the auxiliary class to the list of classes in the object's **objectClass** property.</span></span> <span data-ttu-id="7d5b2-109">Im Beispiel wird " [**IADs. Put**](/windows/desktop/api/iads/nf-iads-iads-put) " verwendet, um den Wert des " **Vin** "-Attributs festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7d5b2-109">Then the example uses [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put) to set the value of the **vin** attribute.</span></span> <span data-ttu-id="7d5b2-110">Schließlich wird " [**IADs. abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) " aufgerufen, um die Änderungen im Verzeichnis zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="7d5b2-110">Finally, it calls [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the changes to the directory.</span></span>


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



 

 