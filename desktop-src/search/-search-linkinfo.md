---
description: Speichert Informationen zu Linktypen und wird von der iitempreviewerext-Schnittstelle verwendet.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Linkinfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214461"
---
# <a name="linkinfo-structure"></a><span data-ttu-id="9e22d-103">Linkinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="9e22d-103">LINKINFO structure</span></span>

<span data-ttu-id="9e22d-104">\[**Linkinfo** und [**iitempreviewerext**](-search-iitempreviewerext.md) werden nur unter Windows XP und Windows Server 2003 unterstützt und sollten nicht mehr verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="9e22d-104">\[**LINKINFO** and [**IItemPreviewerExt**](-search-iitempreviewerext.md) are supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="9e22d-105">Speichert Informationen zu Linktypen und wird von der [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e22d-105">Stores information about link types, and is used by the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e22d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e22d-106">Syntax</span></span>


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a><span data-ttu-id="9e22d-107">Member</span><span class="sxs-lookup"><span data-stu-id="9e22d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e22d-108">**type**</span><span class="sxs-lookup"><span data-stu-id="9e22d-108">**type**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-109">Typ: **[ **linktype**](-search-linktype.md)**</span><span class="sxs-lookup"><span data-stu-id="9e22d-109">Type: **[**LINKTYPE**](-search-linktype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-110">Der Linktyp, der beim Crawlen oder indizieren angegeben wird, angegeben durch eine [**linktype**](-search-linktype.md) -Konstante.</span><span class="sxs-lookup"><span data-stu-id="9e22d-110">The type of link specified when crawling or indexing indicated by a [**LINKTYPE**](-search-linktype.md) constant.</span></span>

</dd> <dt>

<span data-ttu-id="9e22d-111">**bstrincontenttype**</span><span class="sxs-lookup"><span data-stu-id="9e22d-111">**bstrContentType**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-112">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9e22d-112">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-113">Ein **BSTR** -Wert, der den Inhaltstyp angibt.</span><span class="sxs-lookup"><span data-stu-id="9e22d-113">A **BSTR** value that specifies the content type.</span></span>

</dd> <dt>

<span data-ttu-id="9e22d-114">**bstrencoding**</span><span class="sxs-lookup"><span data-stu-id="9e22d-114">**bstrEncoding**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-115">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9e22d-115">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-116">Ein encodingStyle-Attribut, das in der Web Services Description Language (WSDL)-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9e22d-116">An EncodingStyle attribute specified in the Web Services Description Language (WSDL) file.</span></span>

</dd> <dt>

<span data-ttu-id="9e22d-117">**bstraufileext**</span><span class="sxs-lookup"><span data-stu-id="9e22d-117">**bstrFileExt**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-118">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9e22d-118">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-119">Ein **BSTR** -Wert, der die Dateinamenerweiterung angibt.</span><span class="sxs-lookup"><span data-stu-id="9e22d-119">A **BSTR** value that specifies the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="9e22d-120">**VARDATA**</span><span class="sxs-lookup"><span data-stu-id="9e22d-120">**varData**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-121">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9e22d-121">Type: **VARIANT**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-122">Eine Variante, die den Variablen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="9e22d-122">A variant that specifies the variable value.</span></span>

</dd> <dt>

<span data-ttu-id="9e22d-123">**dwrelatedparts**</span><span class="sxs-lookup"><span data-stu-id="9e22d-123">**dwRelatedParts**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-124">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e22d-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-125">Ein **DWORD** , das die zugehörigen Teile angibt.</span><span class="sxs-lookup"><span data-stu-id="9e22d-125">A **DWORD** that specifies the related parts.</span></span>

</dd> <dt>

<span data-ttu-id="9e22d-126">**bstrinrelatedcid**</span><span class="sxs-lookup"><span data-stu-id="9e22d-126">**bstrRelatedCid**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-127">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9e22d-127">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-128">Ein **BSTR** -Wert, der eine CID-Eigenschaft angibt, eine nicht aufgefüllte, dezimale Zeichenfolge mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="9e22d-128">A **BSTR** value that specifies a Cid property, a non-padded, signed decimal string.</span></span>

</dd> <dt>

<span data-ttu-id="9e22d-129">**lcodepage**</span><span class="sxs-lookup"><span data-stu-id="9e22d-129">**lCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="9e22d-130">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="9e22d-130">Type: **Long**</span></span>

</dd> <dd>

<span data-ttu-id="9e22d-131">Die Codepage, die zum Codieren der Zeichenfolge verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e22d-131">The code page to use for encoding the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e22d-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e22d-132">Remarks</span></span>

<span data-ttu-id="9e22d-133">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **linkinfo** -Struktur und die folgenden APIs zu verwenden: die Methoden [**iitempreviewerext:: getlinkedcontent**](-search-iitempreviewerext-getlinkedcontent.md) und [**iitempreviewerext:: getrelatedpart**](-search-iitempreviewerext-getrelatedpart.md) und die [**linktype**](-search-linktype.md) -Enumeration</span><span class="sxs-lookup"><span data-stu-id="9e22d-133">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKINFO** structure, and the following APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e22d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e22d-134">Requirements</span></span>



| <span data-ttu-id="9e22d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e22d-135">Requirement</span></span> | <span data-ttu-id="9e22d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9e22d-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e22d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e22d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9e22d-138">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e22d-138">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9e22d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e22d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9e22d-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e22d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9e22d-141">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="9e22d-141">Redistributable</span></span><br/>          | <span data-ttu-id="9e22d-142">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="9e22d-142">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 




