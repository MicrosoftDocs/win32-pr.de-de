---
description: Stellt Methoden zum Bereitstellen von Browsereinstellungen bereit. Die iitempreviewerext-Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: Iitempreviewerext-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958782"
---
# <a name="iitempreviewerext-interface"></a><span data-ttu-id="b07b9-104">Iitempreviewerext-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b07b9-104">IItemPreviewerExt interface</span></span>

<span data-ttu-id="b07b9-105">Stellt Methoden zum Bereitstellen von Browsereinstellungen bereit.</span><span class="sxs-lookup"><span data-stu-id="b07b9-105">Provides methods for supplying browser settings.</span></span> <span data-ttu-id="b07b9-106">Die **iitempreviewerext** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07b9-106">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="b07b9-107">Member</span><span class="sxs-lookup"><span data-stu-id="b07b9-107">Members</span></span>

<span data-ttu-id="b07b9-108">Die **iitempreviewerext** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b07b9-108">The **IItemPreviewerExt** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b07b9-109">**Iitempreviewerext** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b07b9-109">**IItemPreviewerExt** also has these types of members:</span></span>

-   [<span data-ttu-id="b07b9-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="b07b9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b07b9-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b07b9-111">Methods</span></span>

<span data-ttu-id="b07b9-112">Die **iitempreviewerext** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b07b9-112">The **IItemPreviewerExt** interface has these methods.</span></span>



| <span data-ttu-id="b07b9-113">Methode</span><span class="sxs-lookup"><span data-stu-id="b07b9-113">Method</span></span>                                                                               | <span data-ttu-id="b07b9-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b07b9-114">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b07b9-115">**Getlinkedcontent**</span><span class="sxs-lookup"><span data-stu-id="b07b9-115">**GetLinkedContent**</span></span>](-search-iitempreviewerext-getlinkedcontent.md)               | <span data-ttu-id="b07b9-116">Ermöglicht der Erweiterung den umfangreichen Inhalt für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b07b9-116">Permits the extension to rich content for a property.</span></span> <br/>                            |
| [<span data-ttu-id="b07b9-117">**Getrelatedpart**</span><span class="sxs-lookup"><span data-stu-id="b07b9-117">**GetRelatedPart**</span></span>](-search-iitempreviewerext-getrelatedpart.md)                   | <span data-ttu-id="b07b9-118">Ruft einen zugehörigen Textteil zum Einbetten in den MHTML-Ausgabedatenstrom ab.</span><span class="sxs-lookup"><span data-stu-id="b07b9-118">Gets a related body part for embedding into the output MHTML stream.</span></span><br/>              |
| [<span data-ttu-id="b07b9-119">**Processtransformcommand**</span><span class="sxs-lookup"><span data-stu-id="b07b9-119">**ProcessTransformCommand**</span></span>](-search-iitempreviewerext-processtransformcommand.md) | <span data-ttu-id="b07b9-120">Ermöglicht die Verarbeitung eines Transformations Befehls, der in einer Vorschau Vorlage gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="b07b9-120">Permits processing of a transformation command encountered in a preview template.</span></span><br/> |
| [<span data-ttu-id="b07b9-121">**Vorschlags Suchrichtlinie**</span><span class="sxs-lookup"><span data-stu-id="b07b9-121">**SuggestBrowserPolicy**</span></span>](-search-iitempreviewerext-suggestbrowserpolicy.md)       | <span data-ttu-id="b07b9-122">Schlägt die Sicherheitsrichtlinie vor, die auf den Browser angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b07b9-122">Suggests the security policy to be applied to the browser.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="b07b9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b07b9-123">Remarks</span></span>

<span data-ttu-id="b07b9-124">Die **iitempreviewerext** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b07b9-124">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="b07b9-125">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **iitempreviewerext** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="b07b9-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPreviewerExt** interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b07b9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b07b9-126">Requirements</span></span>



| <span data-ttu-id="b07b9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b07b9-127">Requirement</span></span> | <span data-ttu-id="b07b9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b07b9-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b07b9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b07b9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b07b9-130">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b07b9-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b07b9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b07b9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b07b9-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b07b9-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b07b9-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b07b9-133">Redistributable</span></span><br/>          | <span data-ttu-id="b07b9-134">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b07b9-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
