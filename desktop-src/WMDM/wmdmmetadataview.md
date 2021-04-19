---
title: WMDMMetadataView-Struktur
description: Die WMDMMetadataView-Struktur definiert die Metadatenansicht. Der Inhalt wird basierend auf dieser Definition organisiert.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- WMDMMetadataView Structure Windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369933"
---
# <a name="wmdmmetadataview-structure"></a><span data-ttu-id="8ee07-105">WMDMMetadataView-Struktur</span><span class="sxs-lookup"><span data-stu-id="8ee07-105">WMDMMetadataView structure</span></span>

<span data-ttu-id="8ee07-106">Die **WMDMMetadataView** -Struktur definiert die Metadatenansicht.</span><span class="sxs-lookup"><span data-stu-id="8ee07-106">The **WMDMMetadataView** structure defines the metadata view.</span></span> <span data-ttu-id="8ee07-107">Der Inhalt wird basierend auf dieser Definition organisiert.</span><span class="sxs-lookup"><span data-stu-id="8ee07-107">Content is organized based on this definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee07-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ee07-108">Syntax</span></span>


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a><span data-ttu-id="8ee07-109">Member</span><span class="sxs-lookup"><span data-stu-id="8ee07-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ee07-110">**pwszviewname**</span><span class="sxs-lookup"><span data-stu-id="8ee07-110">**pwszViewName**</span></span>
</dt> <dd>

<span data-ttu-id="8ee07-111">Zeiger auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die den Namen der Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="8ee07-111">Pointer to a wide-character null-terminated string containing the name of the view.</span></span> <span data-ttu-id="8ee07-112">Diese wird als Name des Stamm Knotens verwendet, unter dem diese Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8ee07-112">This is used as the name of the root node under which this view is presented.</span></span>

</dd> <dt>

<span data-ttu-id="8ee07-113">**ntiefe**</span><span class="sxs-lookup"><span data-stu-id="8ee07-113">**nDepth**</span></span>
</dt> <dd>

<span data-ttu-id="8ee07-114">Eine ganze Zahl, die die Tiefe der Ansicht enthält, die angibt, wie viele schachtelte Metadatentags für die Sicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ee07-114">Integer containing the depth of the view, which indicates how many nested metadata tags are used for the view.</span></span>

</dd> <dt>

<span data-ttu-id="8ee07-115">**ppwsztags**</span><span class="sxs-lookup"><span data-stu-id="8ee07-115">**ppwszTags**</span></span>
</dt> <dd>

<span data-ttu-id="8ee07-116">Array von metadatentagzeichenfolgen für die geschachtelte-Tags.</span><span class="sxs-lookup"><span data-stu-id="8ee07-116">Array of metadata tag strings for the nested tags.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8ee07-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ee07-117">Examples</span></span>

<span data-ttu-id="8ee07-118">Der folgende Code erstellt eine Metadatenansicht:</span><span class="sxs-lookup"><span data-stu-id="8ee07-118">The following code creates a metadata view:</span></span>


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



<span data-ttu-id="8ee07-119">Im vorangehenden Code werden die Inhalte wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="8ee07-119">The preceding code organizes content as follows:</span></span>

<dl> <span data-ttu-id="8ee07-120">Meine Ansicht</span><span class="sxs-lookup"><span data-stu-id="8ee07-120">My View</span></span><dl> <span data-ttu-id="8ee07-121">Genre1</span><span class="sxs-lookup"><span data-stu-id="8ee07-121">Genre1</span></span><dl> <span data-ttu-id="8ee07-122">Artist1</span><span class="sxs-lookup"><span data-stu-id="8ee07-122">Artist1</span></span><dl> <span data-ttu-id="8ee07-123">Album1</span><span class="sxs-lookup"><span data-stu-id="8ee07-123">Album1</span></span><dl> <span data-ttu-id="8ee07-124">Song1</span><span class="sxs-lookup"><span data-stu-id="8ee07-124">Song1</span></span>  
<span data-ttu-id="8ee07-125">Song2</span><span class="sxs-lookup"><span data-stu-id="8ee07-125">Song2</span></span>  
<span data-ttu-id="8ee07-126">...</span><span class="sxs-lookup"><span data-stu-id="8ee07-126">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="8ee07-127">Album1</span><span class="sxs-lookup"><span data-stu-id="8ee07-127">Album1</span></span><dl> <span data-ttu-id="8ee07-128">Song1</span><span class="sxs-lookup"><span data-stu-id="8ee07-128">Song1</span></span>  
<span data-ttu-id="8ee07-129">Song2</span><span class="sxs-lookup"><span data-stu-id="8ee07-129">Song2</span></span>  
<span data-ttu-id="8ee07-130">...</span><span class="sxs-lookup"><span data-stu-id="8ee07-130">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> <span data-ttu-id="8ee07-131">Artist1</span><span class="sxs-lookup"><span data-stu-id="8ee07-131">Artist1</span></span><dl> <span data-ttu-id="8ee07-132">Album1</span><span class="sxs-lookup"><span data-stu-id="8ee07-132">Album1</span></span><dl> <span data-ttu-id="8ee07-133">Song1</span><span class="sxs-lookup"><span data-stu-id="8ee07-133">Song1</span></span>  
<span data-ttu-id="8ee07-134">Song2</span><span class="sxs-lookup"><span data-stu-id="8ee07-134">Song2</span></span>  
<span data-ttu-id="8ee07-135">...</span><span class="sxs-lookup"><span data-stu-id="8ee07-135">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> <span data-ttu-id="8ee07-136">Album1</span><span class="sxs-lookup"><span data-stu-id="8ee07-136">Album1</span></span><dl> <span data-ttu-id="8ee07-137">Song1</span><span class="sxs-lookup"><span data-stu-id="8ee07-137">Song1</span></span>  
<span data-ttu-id="8ee07-138">Song2</span><span class="sxs-lookup"><span data-stu-id="8ee07-138">Song2</span></span>  
<span data-ttu-id="8ee07-139">...</span><span class="sxs-lookup"><span data-stu-id="8ee07-139">...</span></span>  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ee07-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ee07-140">Requirements</span></span>



| <span data-ttu-id="8ee07-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ee07-141">Requirement</span></span> | <span data-ttu-id="8ee07-142">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee07-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee07-143">Header</span><span class="sxs-lookup"><span data-stu-id="8ee07-143">Header</span></span><br/> | <dl> <span data-ttu-id="8ee07-144"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ee07-144"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee07-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ee07-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee07-146">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="8ee07-146">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





