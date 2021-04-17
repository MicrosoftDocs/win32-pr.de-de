---
title: WM/wmcollectionid
description: Das WM/wmcollectionid-Attribut enthält eine GUID, die die Auflistung identifiziert.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- WM/wmcollectionid Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389214"
---
# <a name="wmwmcollectionid"></a><span data-ttu-id="4c604-104">WM/wmcollectionid</span><span class="sxs-lookup"><span data-stu-id="4c604-104">WM/WMCollectionID</span></span>

<span data-ttu-id="4c604-105">Das **WM/wmcollectionid-** Attribut enthält eine GUID, die die Auflistung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4c604-105">The **WM/WMCollectionID** attribute contains a GUID identifying the collection.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4c604-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="4c604-106">Global Constant</span></span>

<span data-ttu-id="4c604-107">g \_ wszwmwmcollectionid</span><span class="sxs-lookup"><span data-stu-id="4c604-107">g\_wszWMWMCollectionID</span></span>

## <a name="data-type"></a><span data-ttu-id="4c604-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4c604-108">Data Type</span></span>

<span data-ttu-id="4c604-109">**WMT- \_ Typ- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="4c604-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="4c604-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c604-110">Remarks</span></span>

<span data-ttu-id="4c604-111">Der Inhalt wird von Windows Media-Technologien mithilfe von drei Werten identifiziert: **WM/wmcollectiongroupid**, **WM/wmcollectionid** und **WM/wmcontentid**.</span><span class="sxs-lookup"><span data-stu-id="4c604-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="4c604-112">Mit diesen Werten werden der Inhalt, die Auflistung, zu der er gehört, und die Gruppe, zu der die Auflistung gehört, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4c604-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="4c604-113">Alle drei Werte werden von Windows Media Player aufgefüllt, wenn Metadaten für den Inhalt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4c604-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="4c604-114">Sie können festlegen, dass Ihre Anwendung diese Werte aufzeichnen und Sie verwenden, um Inhalte zu identifizieren, Sie sollten Sie jedoch nicht ändern, wenn Sie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4c604-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c604-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c604-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c604-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="4c604-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




