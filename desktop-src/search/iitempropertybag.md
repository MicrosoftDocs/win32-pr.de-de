---
description: Definiert Methoden zum Abrufen von Informationen zu den Eigenschaften eines Such Elements. Diese Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Iitempropertybag-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128504"
---
# <a name="iitempropertybag-interface"></a><span data-ttu-id="97645-104">Iitempropertybag-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="97645-104">IItemPropertyBag interface</span></span>

<span data-ttu-id="97645-105">Definiert Methoden zum Abrufen von Informationen zu den Eigenschaften eines Such Elements.</span><span class="sxs-lookup"><span data-stu-id="97645-105">Defines methods to obtain information about the properties of a search item.</span></span> <span data-ttu-id="97645-106">Diese Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97645-106">This interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="97645-107">Member</span><span class="sxs-lookup"><span data-stu-id="97645-107">Members</span></span>

<span data-ttu-id="97645-108">Die **iitempropertybag** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="97645-108">The **IItemPropertyBag** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="97645-109">**Iitempropertybag** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="97645-109">**IItemPropertyBag** also has these types of members:</span></span>

-   [<span data-ttu-id="97645-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="97645-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97645-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="97645-111">Methods</span></span>

<span data-ttu-id="97645-112">Die **iitempropertybag** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="97645-112">The **IItemPropertyBag** interface has these methods.</span></span>



| <span data-ttu-id="97645-113">Methode</span><span class="sxs-lookup"><span data-stu-id="97645-113">Method</span></span>                                                      | <span data-ttu-id="97645-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97645-114">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="97645-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="97645-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span></span> | <span data-ttu-id="97645-116">Ruft die Anzahl der Eigenschaften in der Eigenschaften Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="97645-116">Gets a count of the number of properties in the property bag.</span></span><br/>                     |
| [<span data-ttu-id="97645-117">**GetPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="97645-117">**GetPropertyInfo**</span></span>](iitempropertybag-getpropertyinfo.md) | <span data-ttu-id="97645-118">Ruft die Informationen ab, die erforderlich sind, um die Eigenschaften in der Eigenschaften Sammlung zu lesen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="97645-118">Gets the information required to read or save the properties in the property bag.</span></span><br/> |
| [<span data-ttu-id="97645-119">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="97645-119">**Read**</span></span>](iitempropertybag-read.md)                       | <span data-ttu-id="97645-120">Bewirkt, dass eine oder mehrere Eigenschaften aus dem Eigenschaften Behälter gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="97645-120">Causes one or more properties to be read from the property bag.</span></span><br/>                   |
| [<span data-ttu-id="97645-121">**Schreiben**</span><span class="sxs-lookup"><span data-stu-id="97645-121">**Write**</span></span>](iitempropertybag-write.md)                     | <span data-ttu-id="97645-122">Bewirkt, dass eine oder mehrere Eigenschaften im Eigenschaften Behälter gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="97645-122">Causes one or more properties to be saved into the property bag.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="97645-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97645-123">Remarks</span></span>

<span data-ttu-id="97645-124">Die **iitempropertybag** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97645-124">The **IItemPropertyBag** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="97645-125">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **iitempropertybag** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempreviewerext**](-search-iitempreviewerext.md) und [**isearchitem**](-search-isearchitem.md) [**, die-und**](-search-linkinfo.md) [**linktype**](-search-linktype.md) [**-**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) Enumeration.</span><span class="sxs-lookup"><span data-stu-id="97645-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPropertyBag** interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="97645-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97645-126">Requirements</span></span>



| <span data-ttu-id="97645-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97645-127">Requirement</span></span> | <span data-ttu-id="97645-128">Wert</span><span class="sxs-lookup"><span data-stu-id="97645-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97645-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97645-129">Minimum supported client</span></span><br/> | <span data-ttu-id="97645-130">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97645-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97645-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97645-131">Minimum supported server</span></span><br/> | <span data-ttu-id="97645-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97645-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97645-133">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="97645-133">Redistributable</span></span><br/>          | <span data-ttu-id="97645-134">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="97645-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
