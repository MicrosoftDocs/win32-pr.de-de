---
title: Die Get-Methode
description: Die IADs Get-Methode wird verwendet, um einzelne benannte Attribute aus einem Verzeichnis Objekt abzurufen.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- ADSI mithilfe von IADs Get
- ADSI ADSI, using, using the IADs get Method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341626"
---
# <a name="the-get-method"></a><span data-ttu-id="207fd-105">Die Get-Methode</span><span class="sxs-lookup"><span data-stu-id="207fd-105">The Get Method</span></span>

<span data-ttu-id="207fd-106">Die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode wird verwendet, um einzelne benannte Attribute aus einem Verzeichnis Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="207fd-106">The [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve individual named attributes from a directory object.</span></span>

<span data-ttu-id="207fd-107">Im folgenden Codebeispiel wird die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode verwendet, um ein benanntes Attribut aus einem-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="207fd-107">The following code example uses the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method to retrieve a named attribute from an object.</span></span>


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



<span data-ttu-id="207fd-108">In Automatisierungs Sprachen können auf benannte Attribute auch direkt mithilfe der Punkt Notation zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="207fd-108">In Automation languages, named attributes can also be accessed directly using the dot notation.</span></span> <span data-ttu-id="207fd-109">Beispielsweise **Object. Get ("Unterscheidung nach Name")** ist identisch mit **Object. unterscheiden Name**.</span><span class="sxs-lookup"><span data-stu-id="207fd-109">For example, **object.Get("distinguishedName")** is identical to **object.distinguishedName**.</span></span>

<span data-ttu-id="207fd-110">Das folgende Codebeispiel ist mit dem vorherigen Beispiel identisch, mit dem Unterschied, dass auf das Attribut "Unterscheidung nach **Name** " mithilfe der Punkt Notation zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="207fd-110">The following code example is identical to the previous example except that the **distinguishedName** attribute is accessed using the dot notation.</span></span>


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



<span data-ttu-id="207fd-111">Wenn für das Objekt kein Wert festgelegt ist, gibt die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode den Fehler "die Eigenschaft wurde nicht im Cache gefunden" zurück.</span><span class="sxs-lookup"><span data-stu-id="207fd-111">If a value is not set on the object, the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method will return the error "Property not found in cache".</span></span>

 

 




