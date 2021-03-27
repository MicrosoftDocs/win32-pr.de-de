---
description: Macht Methoden verfügbar, mit denen HTML-Seiten aktiviert werden, die in einer Assistenten Erweiterung gehostet werden, um mit dem Assistenten zu kommunizieren.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Webwizardhost-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959678"
---
# <a name="webwizardhost-object"></a><span data-ttu-id="1ed93-103">Webwizardhost-Objekt</span><span class="sxs-lookup"><span data-stu-id="1ed93-103">WebWizardHost object</span></span>

<span data-ttu-id="1ed93-104">Macht Methoden verfügbar, mit denen HTML-Seiten aktiviert werden, die in einer Assistenten Erweiterung gehostet werden, um mit dem Assistenten zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1ed93-104">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span>

## <a name="members"></a><span data-ttu-id="1ed93-105">Member</span><span class="sxs-lookup"><span data-stu-id="1ed93-105">Members</span></span>

<span data-ttu-id="1ed93-106">Das **webwizardhost** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ed93-106">The **WebWizardHost** object has these types of members:</span></span>

-   [<span data-ttu-id="1ed93-107">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ed93-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ed93-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ed93-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ed93-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ed93-109">Methods</span></span>

<span data-ttu-id="1ed93-110">Das **webwizardhost** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1ed93-110">The **WebWizardHost** object has these methods.</span></span>



| <span data-ttu-id="1ed93-111">Methode</span><span class="sxs-lookup"><span data-stu-id="1ed93-111">Method</span></span>                                                      | <span data-ttu-id="1ed93-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ed93-112">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ed93-113">**Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="1ed93-113">**Cancel**</span></span>](iwebwizardhost-cancel.md)                     | <span data-ttu-id="1ed93-114">Simuliert das Klicken auf die Schaltfläche " **Abbrechen** ".</span><span class="sxs-lookup"><span data-stu-id="1ed93-114">Simulates a **Cancel** button click.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="1ed93-115">**Finalback**</span><span class="sxs-lookup"><span data-stu-id="1ed93-115">**FinalBack**</span></span>](iwebwizardhost-finalback.md)               | <span data-ttu-id="1ed93-116">Navigiert zur Client seitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="1ed93-116">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span><br/>                                                                    |
| [<span data-ttu-id="1ed93-117">**Finalnext**</span><span class="sxs-lookup"><span data-stu-id="1ed93-117">**FinalNext**</span></span>](iwebwizardhost-finalnext.md)               | <span data-ttu-id="1ed93-118">Navigiert zur Client seitigen Assistenten Seite, die der Seite folgt, auf der die serverseitigen HTML-Seiten gehostet werden, oder schließt den Assistenten ab, wenn keine weiteren Client seitigen Seiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1ed93-118">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span><br/> |
| [<span data-ttu-id="1ed93-119">**"Abadertext"**</span><span class="sxs-lookup"><span data-stu-id="1ed93-119">**SetHeaderText**</span></span>](iwebwizardhost-setheadertext.md)       | <span data-ttu-id="1ed93-120">Legt den Titel und den Untertitel fest, die im Assistenten Header angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1ed93-120">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="1ed93-121">Im Allgemeinen zeigt der Client den Header oberhalb von HTML und unterhalb der Titelleiste an.</span><span class="sxs-lookup"><span data-stu-id="1ed93-121">In general, the client will display the header above the HTML and below the title bar.</span></span><br/>                    |
| [<span data-ttu-id="1ed93-122">**""-Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="1ed93-122">**SetWizardButtons**</span></span>](iwebwizardhost-setwizardbuttons.md) | <span data-ttu-id="1ed93-123">Aktualisiert die Schaltflächen **zurück**, **weiter** und **Fertig** stellen im Assistenten Rahmen des Clients.</span><span class="sxs-lookup"><span data-stu-id="1ed93-123">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="1ed93-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ed93-124">Properties</span></span>

<span data-ttu-id="1ed93-125">Das **webwizardhost** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ed93-125">The **WebWizardHost** object has these properties.</span></span>



| <span data-ttu-id="1ed93-126">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ed93-126">Property</span></span>                                               | <span data-ttu-id="1ed93-127">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1ed93-127">Access type</span></span>           | <span data-ttu-id="1ed93-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ed93-128">Description</span></span>                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="1ed93-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1ed93-129">**Caption**</span></span>](iwebwizardhost-caption.md)<br/>   | <span data-ttu-id="1ed93-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1ed93-130">Read/write</span></span><br/> | <span data-ttu-id="1ed93-131">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1ed93-131">Not implemented.</span></span><br/>                              |
| [<span data-ttu-id="1ed93-132">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="1ed93-132">**Property**</span></span>](iwebwizardhost-property.md)<br/> | <span data-ttu-id="1ed93-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1ed93-133">Read/write</span></span><br/> | <span data-ttu-id="1ed93-134">Legt den aktuellen Wert einer Eigenschaft fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="1ed93-134">Sets or retrieves a property's current value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ed93-135">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1ed93-135">Requirements</span></span>



| <span data-ttu-id="1ed93-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ed93-136">Requirement</span></span> | <span data-ttu-id="1ed93-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1ed93-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed93-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ed93-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed93-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ed93-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1ed93-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ed93-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed93-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ed93-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1ed93-142">Header</span><span class="sxs-lookup"><span data-stu-id="1ed93-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ed93-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed93-143"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ed93-144">IDL</span><span class="sxs-lookup"><span data-stu-id="1ed93-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ed93-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ed93-145"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="1ed93-146">IID</span><span class="sxs-lookup"><span data-stu-id="1ed93-146">IID</span></span><br/>                      | <span data-ttu-id="1ed93-147">CLSID \_ webwizardhost</span><span class="sxs-lookup"><span data-stu-id="1ed93-147">CLSID\_WebWizardHost</span></span><br/>                                                        |



 

 




