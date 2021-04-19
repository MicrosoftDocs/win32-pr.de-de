---
title: Downloadstatus-Element (msfeeds. h)
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Downloadstatus-Element (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Download Status-Element Fenster Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370171"
---
# <a name="downloadstatus-element"></a><span data-ttu-id="54489-105">Downloadstatus-Element</span><span class="sxs-lookup"><span data-stu-id="54489-105">DownloadStatus Element</span></span>

> [!Note]  
> <span data-ttu-id="54489-106">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="54489-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="54489-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54489-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="54489-108">Das **Downloadstatus** -Element gibt eine URL an, die der Windows-Media Player als Link anzeigt, damit Benutzer den Download Status anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="54489-108">The **DownloadStatus** element specifies a URL the Windows Media Player displays as a link to enable users to view download status.</span></span>

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="54489-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="54489-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="54489-110"><span id="URL"></span><span id="url"></span>Urne</span><span class="sxs-lookup"><span data-stu-id="54489-110"><span id="URL"></span><span id="url"></span>URL</span></span>
</dt> <dd>

<span data-ttu-id="54489-111">Die URL für die Webseite, die im Online Store angezeigt wird, um den Download Status für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="54489-111">URL for the webpage that the online store displays to show download status to the user.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="54489-112">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="54489-112">Parent/Child Elements</span></span>



| <span data-ttu-id="54489-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="54489-113">Hierarchy</span></span>       | <span data-ttu-id="54489-114">Element</span><span class="sxs-lookup"><span data-stu-id="54489-114">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="54489-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54489-115">Parent elements</span></span> | <span data-ttu-id="54489-116">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="54489-116">**ServiceInfo**</span></span> |
| <span data-ttu-id="54489-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54489-117">Child elements</span></span>  | <span data-ttu-id="54489-118">Keine</span><span class="sxs-lookup"><span data-stu-id="54489-118">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="54489-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54489-119">Remarks</span></span>

<span data-ttu-id="54489-120">Windows Media Player zeigt Benutzern eine Meldung an, wenn ein Download ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54489-120">Windows Media Player displays a message to users when a download is in progress.</span></span> <span data-ttu-id="54489-121">Wenn die aktuellen aktiven Dienste eine Download Status-URL definieren, kann der Benutzer auf den Meldungs Text klicken.</span><span class="sxs-lookup"><span data-stu-id="54489-121">If the current active services defines a download status URL, the user can click the message text.</span></span> <span data-ttu-id="54489-122">Wenn der Benutzer auf die Meldung klickt, navigiert der Spieler zu der URL, die vom **Downloadstatus** -Element angegeben wird, sodass der aktuelle aktive Speicher Details zu den zurzeit ausgeführten Downloads bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="54489-122">When the user clicks the message, the Player navigates to the URL specified by the **DownloadStatus** element so the current active store can provide details about downloads in progress.</span></span>

## <a name="requirements"></a><span data-ttu-id="54489-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54489-123">Requirements</span></span>



| <span data-ttu-id="54489-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54489-124">Requirement</span></span> | <span data-ttu-id="54489-125">Wert</span><span class="sxs-lookup"><span data-stu-id="54489-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54489-126">Version</span><span class="sxs-lookup"><span data-stu-id="54489-126">Version</span></span><br/> | <span data-ttu-id="54489-127">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="54489-127">Windows Media Player 10 or later</span></span><br/>                                          |
| <span data-ttu-id="54489-128">Header</span><span class="sxs-lookup"><span data-stu-id="54489-128">Header</span></span><br/>  | <dl> <span data-ttu-id="54489-129"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="54489-129"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54489-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54489-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54489-131">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="54489-131">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="54489-132">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="54489-132">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="54489-133">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="54489-133">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





