---
description: Die Item-Eigenschaft ist eine schreibgeschützte Eigenschaft, die eine Zeichenfolge in der stringlist-Objekt Auflistung zurückgibt.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Stringlist. Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359694"
---
# <a name="stringlistitem-property"></a><span data-ttu-id="d453f-103">Stringlist. Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d453f-103">StringList.Item property</span></span>

<span data-ttu-id="d453f-104">Die **Item** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die eine Zeichenfolge in der [**stringlist-Objekt Auflistung**](stringlist-object.md) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d453f-104">The **Item** property is a read-only property that returns a string in the [**StringList Object**](stringlist-object.md) collection.</span></span>

<span data-ttu-id="d453f-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d453f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d453f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d453f-106">Syntax</span></span>


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a><span data-ttu-id="d453f-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d453f-107">Property value</span></span>

<span data-ttu-id="d453f-108">Index Nummer des Elements mit der Auflistung von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="d453f-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="d453f-109">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d453f-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="d453f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d453f-110">Remarks</span></span>

<span data-ttu-id="d453f-111">Der Client muss überprüfen, ob das [**stringlist-Objekt**](stringlist-object.md) vorhanden und nicht leer ist, bevor auf die **Item** -Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d453f-111">The client must verify that the [**StringList Object**](stringlist-object.md) exists and is not empty before referencing the **Item** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d453f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d453f-112">Requirements</span></span>



| <span data-ttu-id="d453f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d453f-113">Requirement</span></span> | <span data-ttu-id="d453f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d453f-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d453f-115">Version</span><span class="sxs-lookup"><span data-stu-id="d453f-115">Version</span></span><br/> | <span data-ttu-id="d453f-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d453f-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d453f-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d453f-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d453f-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="d453f-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d453f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d453f-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="d453f-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d453f-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d453f-121">IID</span><span class="sxs-lookup"><span data-stu-id="d453f-121">IID</span></span><br/>     | <span data-ttu-id="d453f-122">IID \_ istringlist ist definiert als 000c1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d453f-122">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




