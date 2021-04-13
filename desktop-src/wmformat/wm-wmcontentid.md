---
title: WM/wmcontentid
description: Das WM/wmcontentid-Attribut enthält eine GUID, die den Inhalt identifiziert.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- WM/wmcontentid Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389212"
---
# <a name="wmwmcontentid"></a><span data-ttu-id="53fb9-104">WM/wmcontentid</span><span class="sxs-lookup"><span data-stu-id="53fb9-104">WM/WMContentID</span></span>

<span data-ttu-id="53fb9-105">Das **WM/wmcontentid-** Attribut enthält eine GUID, die den Inhalt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="53fb9-105">The **WM/WMContentID** attribute contains a GUID identifying the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="53fb9-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="53fb9-106">Global Constant</span></span>

<span data-ttu-id="53fb9-107">g \_ wszwmwmcontentid</span><span class="sxs-lookup"><span data-stu-id="53fb9-107">g\_wszWMWMContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="53fb9-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="53fb9-108">Data Type</span></span>

<span data-ttu-id="53fb9-109">**WMT- \_ Typ- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="53fb9-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="53fb9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53fb9-110">Remarks</span></span>

<span data-ttu-id="53fb9-111">Der Inhalt wird von Windows Media-Technologien mithilfe von drei Werten identifiziert: **WM/wmcollectiongroupid**, **WM/wmcollectionid** und **WM/wmcontentid**.</span><span class="sxs-lookup"><span data-stu-id="53fb9-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="53fb9-112">Mit diesen Werten werden der Inhalt, die Auflistung, zu der er gehört, und die Gruppe, zu der die Auflistung gehört, identifiziert.</span><span class="sxs-lookup"><span data-stu-id="53fb9-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="53fb9-113">Alle drei Werte werden von Windows Media Player aufgefüllt, wenn Metadaten für den Inhalt abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="53fb9-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="53fb9-114">Sie können festlegen, dass Ihre Anwendung diese Werte aufzeichnen und Sie verwenden, um Inhalte zu identifizieren, Sie sollten Sie jedoch nicht ändern, wenn Sie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="53fb9-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="53fb9-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53fb9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fb9-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="53fb9-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




