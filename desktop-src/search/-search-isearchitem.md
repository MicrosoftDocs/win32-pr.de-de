---
description: Stellt Methoden bereit, die die Interaktion zwischen einer Benutzeroberfläche (UI) und den durch den Indexer erstellten suchnamespace-Objekten definieren.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Isearchitem-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393462"
---
# <a name="isearchitem-interface"></a><span data-ttu-id="93cd6-103">Isearchitem-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="93cd6-103">ISearchItem interface</span></span>

<span data-ttu-id="93cd6-104">Stellt Methoden bereit, die die Interaktion zwischen einer Benutzeroberfläche (UI) und den durch den Indexer erstellten suchnamespace-Objekten definieren.</span><span class="sxs-lookup"><span data-stu-id="93cd6-104">Provides methods that define interaction between a user interface (UI) and the Search namespace objects created by the indexer.</span></span>

## <a name="members"></a><span data-ttu-id="93cd6-105">Member</span><span class="sxs-lookup"><span data-stu-id="93cd6-105">Members</span></span>

<span data-ttu-id="93cd6-106">Die **isearchitem** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="93cd6-106">The **ISearchItem** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="93cd6-107">**Isearchitem** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="93cd6-107">**ISearchItem** also has these types of members:</span></span>

-   [<span data-ttu-id="93cd6-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="93cd6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93cd6-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="93cd6-109">Methods</span></span>

<span data-ttu-id="93cd6-110">Die **isearchitem** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="93cd6-110">The **ISearchItem** interface has these methods.</span></span>



| <span data-ttu-id="93cd6-111">Methode</span><span class="sxs-lookup"><span data-stu-id="93cd6-111">Method</span></span>                                                         | <span data-ttu-id="93cd6-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93cd6-112">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93cd6-113">**Getpartfolder**</span><span class="sxs-lookup"><span data-stu-id="93cd6-113">**GetParentFolder**</span></span>](-search-isearchitem-getparentfolder.md) | <span data-ttu-id="93cd6-114">Ruft das **isearchitem** -Objekt ab, wenn die URL eine tatsächliche shelldatenquelle darstellt (wird auch als Shellnamespace-Erweiterung bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="93cd6-114">Gets the **ISearchItem** object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span><br/> |
| <span data-ttu-id="93cd6-115">[**Getuiobjectof**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93cd6-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span></span>     | <span data-ttu-id="93cd6-116">Ruft das Benutzeroberflächen Objekt (UI) von **isearchitem** ab.</span><span class="sxs-lookup"><span data-stu-id="93cd6-116">Gets the user interface (UI) object of **ISearchItem**.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="93cd6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93cd6-117">Remarks</span></span>

<span data-ttu-id="93cd6-118">[**Isearchitem:: getzientfolder**](-search-isearchitem-getparentfolder.md) wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93cd6-118">The [**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="93cd6-119">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **isearchitem** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md)und [**isearchprotocolui**](-search-isearchprotocolui.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="93cd6-119">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchItem** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="93cd6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93cd6-120">Requirements</span></span>



| <span data-ttu-id="93cd6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93cd6-121">Requirement</span></span> | <span data-ttu-id="93cd6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="93cd6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93cd6-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93cd6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="93cd6-124">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93cd6-124">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93cd6-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93cd6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="93cd6-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93cd6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93cd6-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="93cd6-127">Redistributable</span></span><br/>          | <span data-ttu-id="93cd6-128">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="93cd6-128">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
