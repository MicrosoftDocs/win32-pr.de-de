---
description: Stellt eine Methode zum Aufrufen von isearchitem-Objekten bereit.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Isearchprotocolui-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356711"
---
# <a name="isearchprotocolui-interface"></a><span data-ttu-id="0ddb6-103">Isearchprotocolui-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0ddb6-103">ISearchProtocolUI interface</span></span>

<span data-ttu-id="0ddb6-104">Stellt eine Methode zum Aufrufen von [**isearchitem**](-search-isearchitem.md) -Objekten bereit.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-104">Provides a method for invoking [**ISearchItem**](-search-isearchitem.md) objects.</span></span> <span data-ttu-id="0ddb6-105">Methoden in dieser Schnittstelle werden vom Protokoll Host aufgerufen, wenn URLs aus dem Gatherer verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-105">Methods in this interface are called by the protocol host when processing URLs from the gatherer.</span></span> <span data-ttu-id="0ddb6-106">Der Protokollhandler implementiert das Protokoll für den Zugriff auf eine Inhaltsquelle im systemeigenen Format, und diese Schnittstelle implementiert einen benutzerdefinierten Protokollhandler, um die Datenquellen zu erweitern, die indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-106">The protocol handler implements the protocol for accessing a content source in its native format, and this interface implements a custom protocol handler to expand the data sources that can be indexed.</span></span>

## <a name="members"></a><span data-ttu-id="0ddb6-107">Member</span><span class="sxs-lookup"><span data-stu-id="0ddb6-107">Members</span></span>

<span data-ttu-id="0ddb6-108">Die **isearchprotocolui** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-108">The **ISearchProtocolUI** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0ddb6-109">**Isearchprotocolui** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0ddb6-109">**ISearchProtocolUI** also has these types of members:</span></span>

-   [<span data-ttu-id="0ddb6-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0ddb6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0ddb6-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0ddb6-111">Methods</span></span>

<span data-ttu-id="0ddb6-112">Die **isearchprotocolui** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-112">The **ISearchProtocolUI** interface has these methods.</span></span>



| <span data-ttu-id="0ddb6-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0ddb6-113">Method</span></span>                                                                       | <span data-ttu-id="0ddb6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ddb6-114">Description</span></span>                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ddb6-115">**Getsearchitemforurl**</span><span class="sxs-lookup"><span data-stu-id="0ddb6-115">**GetSearchItemForUrl**</span></span>](-search-isearchprotocolui-getsearchitemforurl.md) | <span data-ttu-id="0ddb6-116">Ruft das Suchelement für die angegebenen Daten ab.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-116">Gets the search item for the data specified.</span></span> <span data-ttu-id="0ddb6-117">Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und Ruft einen Zeiger auf das [**isearchitem**](-search-isearchitem.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-117">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ddb6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ddb6-118">Remarks</span></span>

<span data-ttu-id="0ddb6-119">Die **isearchprotocolui** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ddb6-119">The **ISearchProtocolUI** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="0ddb6-120">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler von Drittanbietern auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **isearchprotocolui** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="0ddb6-120">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchProtocolUI** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddb6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ddb6-121">Requirements</span></span>



| <span data-ttu-id="0ddb6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ddb6-122">Requirement</span></span> | <span data-ttu-id="0ddb6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0ddb6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0ddb6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ddb6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddb6-125">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ddb6-125">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0ddb6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ddb6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddb6-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ddb6-127">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0ddb6-128">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0ddb6-128">Redistributable</span></span><br/>          | <span data-ttu-id="0ddb6-129">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="0ddb6-129">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
