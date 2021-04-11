---
description: Der CimType-Qualifizierer enthält Text, der den Typ einer Eigenschaft beschreibt.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: CimType-Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131984"
---
# <a name="cimtype-qualifier"></a><span data-ttu-id="35dc4-103">CimType-Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="35dc4-103">CIMType Qualifier</span></span>

<span data-ttu-id="35dc4-104">Der **CimType-Qualifizierer** enthält Text, der den Typ einer Eigenschaft beschreibt.</span><span class="sxs-lookup"><span data-stu-id="35dc4-104">The **CIMType** qualifier contains text describing the type of a property.</span></span>

<span data-ttu-id="35dc4-105">Dieser Text kann der MOF-Typ sein, z. b. "String" und "sint32", oder der CIM-Typ, z. b. "CIM \_ String" und "CIM \_ sint32".</span><span class="sxs-lookup"><span data-stu-id="35dc4-105">This text can be the MOF type such as "string" and "sint32" or the CIM type such as "CIM\_STRING" and "CIM\_SINT32".</span></span> <span data-ttu-id="35dc4-106">Zwischen dem **CimType-Qualifizierer** und dem Typ der Eigenschaft, der im *pvttype* -Parameter der [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) -Methode verwendet wird, besteht eine eins-zu-eins-Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="35dc4-106">There is a one-to-one correspondence between the **CIMType** qualifier and the type of the property used in the *pvtType* parameter of the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="35dc4-107">Die beiden Ausnahmen lauten:</span><span class="sxs-lookup"><span data-stu-id="35dc4-107">The two exceptions are:</span></span>

-   <span data-ttu-id="35dc4-108">[*Verweis Eigenschaften*](gloss-r.md)mit dem Type- **CIM- \_ Verweis**, der den Wert "Ref: ClassName" enthält.</span><span class="sxs-lookup"><span data-stu-id="35dc4-108">[*Reference properties*](gloss-r.md), which have the type **CIM\_REFERENCE**, that contains the "REF:classname" value.</span></span> <span data-ttu-id="35dc4-109">Der ClassName-Wert beschreibt den Klassentyp der Verweis Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="35dc4-109">The classname value describes the class type of the reference property.</span></span>
-   <span data-ttu-id="35dc4-110">Eigenschaften von eingebetteten Objekten, die den **CIM \_ -Objekttyp** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="35dc4-110">Embedded object properties, which have the **CIM\_OBJECT** type.</span></span>

<span data-ttu-id="35dc4-111">Beachten Sie jedoch, dass der **CimType-Qualifizierer** und verwendet werden kann, um eine Verweis Eigenschaft genauer einzugeben.</span><span class="sxs-lookup"><span data-stu-id="35dc4-111">Please note, however, that the **CIMType** qualifier can and should be used to type a reference property more exactly.</span></span> <span data-ttu-id="35dc4-112">Wenn sich die-Eigenschaft beispielsweise immer auf Instanzen der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse bezieht, sollte der **CimType-Qualifizierer** auf Folgendes festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="35dc4-112">For example, if the property always refers to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class, its **CIMType** qualifier should be set to:</span></span>


```mof
"ref:Win32_LogicalDisk"
```



<span data-ttu-id="35dc4-113">Standardmäßig hat der **CimType-Qualifizierer** einer Verweis Eigenschaft den Typ **ref**.</span><span class="sxs-lookup"><span data-stu-id="35dc4-113">By default, the **CIMType** qualifier of a reference property has the type **ref**.</span></span>

<span data-ttu-id="35dc4-114">Wie bei den Verweis Eigenschaften sollte der **CimType-Qualifizierer** zum Eingeben einer eingebetteten Objekt Eigenschaft genau mit der folgenden Syntax verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="35dc4-114">As with reference properties, the **CIMType** qualifier should used to type an embedded object property more exactly with the following syntax:</span></span>


```mof
"object:EmbedClass"
```



<span data-ttu-id="35dc4-115">Da WMI mehr Typen zulässt, als durch Standard Konstanten mit dem VT-Präfix ausgedrückt werden können \_ , kann der **CimType-Qualifizierer** helfen, Typwerte zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="35dc4-115">Because WMI allows more types than can be expressed by standard constants with the VT\_ prefix, the **CIMType** qualifier can help interpret type values.</span></span> <span data-ttu-id="35dc4-116">Der **CimType-Qualifizierer** wird automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="35dc4-116">The **CIMType** qualifier is added automatically.</span></span> <span data-ttu-id="35dc4-117">Weitere Informationen finden Sie unter [MOF-Datentypen](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="35dc4-117">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35dc4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35dc4-118">Requirements</span></span>



| <span data-ttu-id="35dc4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35dc4-119">Requirement</span></span> | <span data-ttu-id="35dc4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="35dc4-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="35dc4-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35dc4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35dc4-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35dc4-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="35dc4-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35dc4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35dc4-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35dc4-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35dc4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35dc4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dc4-126">**WMI-Standard Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="35dc4-126">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="35dc4-127">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="35dc4-127">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="35dc4-128">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="35dc4-128">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

