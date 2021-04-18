---
description: Die Count-Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im stringlist-Objekt zurückgibt.
ms.assetid: aa85b8d9-344d-4f31-aa86-9e6497c07751
title: Stringlist. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Count
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b880b6d6c7c995c2aff1a40e7e4fcc6908eb7c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354701"
---
# <a name="stringlistcount-property"></a><span data-ttu-id="45f25-103">Stringlist. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="45f25-103">StringList.Count property</span></span>

<span data-ttu-id="45f25-104">Die **count** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die die Anzahl der Elemente im [**stringlist-Objekt**](stringlist-object.md)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="45f25-104">The **Count** property is a read-only property that returns the number of items in the [**StringList object**](stringlist-object.md).</span></span>

<span data-ttu-id="45f25-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="45f25-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f25-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="45f25-106">Syntax</span></span>


```JScript
propVal = StringList.Count
```



## <a name="property-value"></a><span data-ttu-id="45f25-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="45f25-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="45f25-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45f25-108">Remarks</span></span>

<span data-ttu-id="45f25-109">Der Client muss überprüfen, ob das [**stringlist**](stringlist-object.md) -Objekt vorhanden und nicht leer ist, bevor auf die **count** -Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="45f25-109">The client must verify that the [**StringList**](stringlist-object.md) object exists and is not empty before referencing the **Count** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f25-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45f25-110">Requirements</span></span>



| <span data-ttu-id="45f25-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45f25-111">Requirement</span></span> | <span data-ttu-id="45f25-112">Wert</span><span class="sxs-lookup"><span data-stu-id="45f25-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f25-113">Version</span><span class="sxs-lookup"><span data-stu-id="45f25-113">Version</span></span><br/> | <span data-ttu-id="45f25-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="45f25-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="45f25-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="45f25-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="45f25-116">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="45f25-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="45f25-117">DLL</span><span class="sxs-lookup"><span data-stu-id="45f25-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="45f25-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45f25-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="45f25-119">IID</span><span class="sxs-lookup"><span data-stu-id="45f25-119">IID</span></span><br/>     | <span data-ttu-id="45f25-120">IID \_ istringlist ist definiert als 000c1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="45f25-120">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




