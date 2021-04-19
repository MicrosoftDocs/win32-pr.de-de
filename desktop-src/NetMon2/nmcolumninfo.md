---
description: Die nmcolumninfo-Struktur definiert eine Spalte im oberen Bereich der Ereignisanzeige.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Nmcolumninfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373354"
---
# <a name="nmcolumninfo-structure"></a><span data-ttu-id="0bc19-103">Nmcolumninfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="0bc19-103">NMCOLUMNINFO structure</span></span>

<span data-ttu-id="0bc19-104">Die **nmcolumninfo** -Struktur definiert eine Spalte im oberen Bereich der Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="0bc19-104">The **NMCOLUMNINFO** structure defines one column in the top pane of the Event Viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bc19-105">Syntax</span></span>


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a><span data-ttu-id="0bc19-106">Member</span><span class="sxs-lookup"><span data-stu-id="0bc19-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0bc19-107">**szcolumnname**</span><span class="sxs-lookup"><span data-stu-id="0bc19-107">**szColumnName**</span></span>
</dt> <dd>

<span data-ttu-id="0bc19-108">Der anzeigbare Name einer bestimmten Spalte.</span><span class="sxs-lookup"><span data-stu-id="0bc19-108">Displayable name of a specific column.</span></span> <span data-ttu-id="0bc19-109">Wenn der Name zu lang ist, wird er in der Standard Ereignisanzeige Konfiguration nicht vollständig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0bc19-109">If the name is too long, it will not be completely visible in the default Event Viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0bc19-110">**Variantdata**</span><span class="sxs-lookup"><span data-stu-id="0bc19-110">**VariantData**</span></span>
</dt> <dd>

<span data-ttu-id="0bc19-111">Die in die Spalte eingefügten Daten.</span><span class="sxs-lookup"><span data-stu-id="0bc19-111">The data inserted into the column.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bc19-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bc19-112">Requirements</span></span>



| <span data-ttu-id="0bc19-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bc19-113">Requirement</span></span> | <span data-ttu-id="0bc19-114">Wert</span><span class="sxs-lookup"><span data-stu-id="0bc19-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc19-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bc19-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0bc19-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bc19-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0bc19-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bc19-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0bc19-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bc19-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0bc19-119">Header</span><span class="sxs-lookup"><span data-stu-id="0bc19-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bc19-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc19-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




