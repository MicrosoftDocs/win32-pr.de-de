---
title: Die PutEx-Methode
description: Die IADs-PutEx-Methode verwendet den Namen einer Eigenschaft, um eine Eigenschaft mit einzelnen oder mehreren Werten im Eigenschaften Cache zu speichern.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI, Info
- ADSI ADSI, Beispielcode Visual Basic mit der PutEx-Methode
- Eigenschaften-ADSI, Speichern einer einzelnen Eigenschaft oder einer mehrwertigen Eigenschaft im Eigenschafts Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855240"
---
# <a name="the-putex-method"></a><span data-ttu-id="b17b8-106">Die PutEx-Methode</span><span class="sxs-lookup"><span data-stu-id="b17b8-106">The PutEx Method</span></span>

<span data-ttu-id="b17b8-107">Die [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode verwendet den Namen einer Eigenschaft, um eine Eigenschaft mit einzelnen oder mehreren Werten im Eigenschaften Cache zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b17b8-107">The [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the name of a property to save a property with single or multiple values into the property cache.</span></span> <span data-ttu-id="b17b8-108">Dadurch wird ein beliebiger Wert überschrieben, der sich zurzeit im Eigenschaften Cache</span><span class="sxs-lookup"><span data-stu-id="b17b8-108">This overwrites any value currently in the property cache.</span></span> <span data-ttu-id="b17b8-109">Die Werte im Cache werden erst in den zugrunde liegenden Verzeichnisdienst geschrieben, wenn ein [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) auftritt.</span><span class="sxs-lookup"><span data-stu-id="b17b8-109">The values in the cache are not written to the underlying directory service until an [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) occurs.</span></span> <span data-ttu-id="b17b8-110">Das erste Argument von **PutEx** gibt an, ob Sie vorhandene Werte für die Eigenschaft ersetzen oder hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="b17b8-110">The first argument of **PutEx** indicates whether you want to replace or add to any existing values for the property.</span></span> <span data-ttu-id="b17b8-111">Im folgenden Beispiel werden alle vorhandenen Werte des **Description** -Attributs im Cache gelöscht, wenn **PutEx** aufgerufen wird, und auf dem Server gelöscht, wenn " **ctinfo** " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b17b8-111">In the following example, any existing values of the **description** attribute are erased in the cache when **PutEx** is called, and erased on the server when **SetInfo** is called.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




