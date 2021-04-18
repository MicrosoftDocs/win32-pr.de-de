---
title: Die Getex-Methode
description: Einige Attribute können einen oder mehrere Werte speichern.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- Getex ADSI, using IADs Getex
- ADSI ADSI, using, using the IADs Getex Method
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338560"
---
# <a name="the-getex-method"></a><span data-ttu-id="2c2ba-105">Die Getex-Methode</span><span class="sxs-lookup"><span data-stu-id="2c2ba-105">The GetEx Method</span></span>

<span data-ttu-id="2c2ba-106">Einige Attribute können einen oder mehrere Werte speichern.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-106">Some attributes can store one or more values.</span></span> <span data-ttu-id="2c2ba-107">Beispielsweise ist das **OtherTelephone** -Attribut eines Benutzer Objekts in Active Directory eine Eigenschaft, die NULL, einen oder mehrere Werte aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-107">For example, the **otherTelephone** attribute of a user object in Active Directory is a property that can have zero, one, or many values.</span></span> <span data-ttu-id="2c2ba-108">Attribute mit mehreren Werten werden als "mehrwertige Attribute" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-108">Attributes that have multiple values are known as "multi-valued attributes".</span></span> <span data-ttu-id="2c2ba-109">Wenn die [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) -Methode zum Abrufen eines mehrwertigen Attributs verwendet wird, müssen die Ergebnisse anders verarbeitet werden, als wenn das Attribut über einen einzelnen Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-109">If the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve a multi-valued attribute, the results must be processed differently than if the attribute has a single value.</span></span> <span data-ttu-id="2c2ba-110">Die Ergebnisse, die von der [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode bereitgestellt werden, werden jedoch auf die gleiche Weise verarbeitet, unabhängig davon, ob das Attribut einen einzelnen oder mehrere Werte aufweist.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-110">The results provided by the [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, however, are processed in the same manner, regardless if the attribute has a single or multiple values.</span></span> <span data-ttu-id="2c2ba-111">In beiden Fällen gibt die **IADs:: Getex** -Methode die Werte in einem Array zurück.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-111">In both cases, the **IADs::GetEx** method returns the values in an array.</span></span>

<span data-ttu-id="2c2ba-112">Die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode ruft Eigenschaften aus dem Eigenschafts Cache ab.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-112">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method retrieves properties from the property cache.</span></span> <span data-ttu-id="2c2ba-113">Wenn die angegebene Eigenschaft nicht im Cache gefunden wird, führt **IADs:: Getex** einen impliziten [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Aufrufs aus.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-113">If the specified property is not found in the cache, **IADs::GetEx** performs an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span>

<span data-ttu-id="2c2ba-114">Die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode gibt ein Variant-Array von Varianten zurück, unabhängig von der Anzahl von Werten, die vom Server zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-114">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method returns a variant array of variants regardless of the number of values returned from the server.</span></span> <span data-ttu-id="2c2ba-115">Dies gilt auch, wenn das Attribut nur einen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-115">This is true even if the attribute only contains one value.</span></span>


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="2c2ba-116">Die [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) -Methode kann auch für einwertige Attribute verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-116">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method can also be used for single-valued attributes.</span></span> <span data-ttu-id="2c2ba-117">Die Ergebnisse eines einwertigen Attributs werden genauso wie die Ergebnisse für ein mehr wertiges Attribut verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-117">The results of a single-valued attribute are processed the same as the results for a multi-valued attribute.</span></span>


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



<span data-ttu-id="2c2ba-118">Wenn für das Attribut kein Wert festgelegt ist, gibt [**IADs:: Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex) den Fehler "die Eigenschaft wurde im Cache nicht gefunden" zurück.</span><span class="sxs-lookup"><span data-stu-id="2c2ba-118">If no value is set for the attribute, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) returns the error "Property not found in cache".</span></span>

 

 




