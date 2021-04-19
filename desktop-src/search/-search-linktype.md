---
description: Gibt den Linktyp beim Crawlen oder indizieren an.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Linktype-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343242"
---
# <a name="linktype-enumeration"></a><span data-ttu-id="bf2ef-103">Linktype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="bf2ef-103">LINKTYPE enumeration</span></span>

<span data-ttu-id="bf2ef-104">\[Die **linktype** -Enumeration wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="bf2ef-104">\[The **LINKTYPE** enumeration is supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="bf2ef-105">Gibt den Linktyp beim Crawlen oder indizieren an.</span><span class="sxs-lookup"><span data-stu-id="bf2ef-105">Specifies the type of link when crawling or indexing.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2ef-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf2ef-106">Syntax</span></span>


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a><span data-ttu-id="bf2ef-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bf2ef-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bf2ef-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**linktype- \_ URL**</span><span class="sxs-lookup"><span data-stu-id="bf2ef-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="bf2ef-109">Gibt an, ob der Linktyp der URLs indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf2ef-109">Specifies whether the URLs link type should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ef-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**linktype- \_ Inhalt**</span><span class="sxs-lookup"><span data-stu-id="bf2ef-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE\_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="bf2ef-111">Gibt an, ob der Link Inhalt indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf2ef-111">Specifies whether the link content should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="bf2ef-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**linktype \_ verwandt**</span><span class="sxs-lookup"><span data-stu-id="bf2ef-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE\_RELATED**</span></span>
</dt> <dd>

<span data-ttu-id="bf2ef-113">Gibt einen zugehörigen Link an.</span><span class="sxs-lookup"><span data-stu-id="bf2ef-113">Specifies a related link.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf2ef-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf2ef-114">Remarks</span></span>

<span data-ttu-id="bf2ef-115">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **linktype** -Flags und die folgenden anderen APIs zu verwenden: die Methoden [**iitempreviewerext:: getlinkedcontent**](-search-iitempreviewerext-getlinkedcontent.md) und [**iitempreviewerext:: getrelatedpart**](-search-iitempreviewerext-getrelatedpart.md) und die [**linkinfo**](-search-linkinfo.md) -Struktur</span><span class="sxs-lookup"><span data-stu-id="bf2ef-115">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKTYPE** flags, and the following other APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKINFO**](-search-linkinfo.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2ef-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf2ef-116">Requirements</span></span>



| <span data-ttu-id="bf2ef-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf2ef-117">Requirement</span></span> | <span data-ttu-id="bf2ef-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bf2ef-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf2ef-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf2ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2ef-120">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf2ef-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bf2ef-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf2ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2ef-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf2ef-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




