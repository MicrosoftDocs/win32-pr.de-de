---
description: Die Item-Eigenschaft ist eine schreibgeschützte Eigenschaft, die einen Datensatz in einer RecordList-Objekt Auflistung zurückgibt.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList. Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364739"
---
# <a name="recordlistitem-property"></a><span data-ttu-id="be719-103">RecordList. Item-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="be719-103">RecordList.Item property</span></span>

<span data-ttu-id="be719-104">Die **Item** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die einen Datensatz in einer [**RecordList**](recordlist-object.md) -Objekt Auflistung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="be719-104">The **Item** property is a read-only property that returns a record in a [**RecordList**](recordlist-object.md) Object collection.</span></span>

<span data-ttu-id="be719-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="be719-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be719-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="be719-106">Syntax</span></span>


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a><span data-ttu-id="be719-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="be719-107">Property value</span></span>

<span data-ttu-id="be719-108">Index Nummer des Elements mit der Auflistung von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="be719-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="be719-109">Der Index ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be719-109">Index is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="be719-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be719-110">Remarks</span></span>

<span data-ttu-id="be719-111">Der Client muss überprüfen, ob das [**RecordList**](recordlist-object.md) -Objekt vorhanden und nicht leer ist, bevor auf die Item-Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="be719-111">The client must verify that the [**RecordList**](recordlist-object.md) object exists and is not empty before referencing the Item property.</span></span>

## <a name="requirements"></a><span data-ttu-id="be719-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be719-112">Requirements</span></span>



| <span data-ttu-id="be719-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be719-113">Requirement</span></span> | <span data-ttu-id="be719-114">Wert</span><span class="sxs-lookup"><span data-stu-id="be719-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be719-115">Version</span><span class="sxs-lookup"><span data-stu-id="be719-115">Version</span></span><br/> | <span data-ttu-id="be719-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be719-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be719-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be719-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be719-118">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="be719-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="be719-119">DLL</span><span class="sxs-lookup"><span data-stu-id="be719-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="be719-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be719-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="be719-121">IID</span><span class="sxs-lookup"><span data-stu-id="be719-121">IID</span></span><br/>     | <span data-ttu-id="be719-122">IID \_ irecordlist ist definiert als 000c1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="be719-122">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




