---
title: Optionale Methoden
description: Optionale Methoden
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102382"
---
# <a name="optional-methods"></a><span data-ttu-id="fa774-103">Optionale Methoden</span><span class="sxs-lookup"><span data-stu-id="fa774-103">Optional Methods</span></span>

<span data-ttu-id="fa774-104">Eine OLE-Komponente kann eine Schnittstelle implementieren, ohne dass die gesamte Semantik jeder Methode in der Schnittstelle implementiert wird. stattdessen wird "E \_ notimpl" oder "S OK" zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="fa774-104">An OLE component can implement an interface without implementing all the semantics of every method in the interface, instead returning E\_NOTIMPL or S\_OK as appropriate.</span></span> <span data-ttu-id="fa774-105">In der folgenden Tabelle werden die Methoden beschrieben, die von einem ActiveX-Steuerelement Container nicht implementiert werden müssen (d. h., der Steuerelement Container kann e \_ notimpl zurückgeben).</span><span class="sxs-lookup"><span data-stu-id="fa774-105">The following table describes those methods that an ActiveX control container is not required to implement (i.e. the control container can return E\_NOTIMPL).</span></span>

<span data-ttu-id="fa774-106">In der folgenden Tabelle werden optionale Methoden beschrieben: Beachten Sie, dass die Methode weiterhin vorhanden sein muss, aber einfach E notimpl zurückgeben kann, \_ anstatt eine wirkliche Semantik zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="fa774-106">The table below describes optional methods; note that the method must still exist, but can simply return E\_NOTIMPL instead of implementing real semantics.</span></span> <span data-ttu-id="fa774-107">Beachten Sie, dass jede Methode aus einer obligatorischen Schnittstelle, die nicht unten aufgeführt ist, als obligatorisch angesehen werden muss und E \_ notimpl nicht zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fa774-107">Note that any method from a mandatory interface that is not listed below must be considered mandatory and may not return E\_NOTIMPL.</span></span>

## <a name="ioleclientsite"></a><span data-ttu-id="fa774-108">IOleClientSite</span><span class="sxs-lookup"><span data-stu-id="fa774-108">IOleClientSite</span></span>



| <span data-ttu-id="fa774-109">Methode</span><span class="sxs-lookup"><span data-stu-id="fa774-109">Method</span></span>                                                     | <span data-ttu-id="fa774-110">Kommentare</span><span class="sxs-lookup"><span data-stu-id="fa774-110">Comments</span></span>                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa774-111">**Saveobject**</span><span class="sxs-lookup"><span data-stu-id="fa774-111">**SaveObject**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | <span data-ttu-id="fa774-112">Erforderlich, damit die Persistenz erfolgreich unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fa774-112">Necessary for persistence to be successfully supported.</span></span><br/>                                       |
| [<span data-ttu-id="fa774-113">**GetMoniker**</span><span class="sxs-lookup"><span data-stu-id="fa774-113">**GetMoniker**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | <span data-ttu-id="fa774-114">Nur erforderlich, wenn der Container das Verknüpfen mit Steuerelementen in einem eigenen Formular oder Dokument unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa774-114">Necessary only if the container supports linking to controls within its own form or document.</span></span><br/> |



 

## <a name="ioleinplacesite"></a><span data-ttu-id="fa774-115">Ioleingeplacesite</span><span class="sxs-lookup"><span data-stu-id="fa774-115">IOleInPlaceSite</span></span>



| <span data-ttu-id="fa774-116">Methode</span><span class="sxs-lookup"><span data-stu-id="fa774-116">Method</span></span>                                                                     | <span data-ttu-id="fa774-117">Kommentare</span><span class="sxs-lookup"><span data-stu-id="fa774-117">Comments</span></span>                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="fa774-118">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="fa774-118">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | <span data-ttu-id="fa774-119">Optional</span><span class="sxs-lookup"><span data-stu-id="fa774-119">Optional</span></span><br/>                                      |
| [<span data-ttu-id="fa774-120">**Scroll**</span><span class="sxs-lookup"><span data-stu-id="fa774-120">**Scroll**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | <span data-ttu-id="fa774-121">Gibt möglicherweise \_ den Wert S false ohne Aktion zurück.</span><span class="sxs-lookup"><span data-stu-id="fa774-121">May return S\_FALSE with no action.</span></span><br/>           |
| [<span data-ttu-id="fa774-122">**Verwerfen von dostate**</span><span class="sxs-lookup"><span data-stu-id="fa774-122">**DiscardUndoState**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | <span data-ttu-id="fa774-123">Kann S \_ OK ohne Aktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fa774-123">Can return S\_OK with no action.</span></span><br/>              |
| [<span data-ttu-id="fa774-124">**"Deaktiviert"**</span><span class="sxs-lookup"><span data-stu-id="fa774-124">**DeactivateAndUndo**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | <span data-ttu-id="fa774-125">Die Aktivierung ist obligatorisch. Rückgängigmachen ist optional.</span><span class="sxs-lookup"><span data-stu-id="fa774-125">Deactivation is mandatory; Undo is optional.</span></span> <br/> |



 

## <a name="iolecontrolsite"></a><span data-ttu-id="fa774-126">IOleControlSite</span><span class="sxs-lookup"><span data-stu-id="fa774-126">IOleControlSite</span></span>



| <span data-ttu-id="fa774-127">Methode</span><span class="sxs-lookup"><span data-stu-id="fa774-127">Method</span></span>                                                                          | <span data-ttu-id="fa774-128">Kommentare</span><span class="sxs-lookup"><span data-stu-id="fa774-128">Comments</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa774-129">**Getextendebug-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="fa774-129">**GetExtendedControl**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | <span data-ttu-id="fa774-130">Erforderlich für Container, die erweiterte Steuerelemente unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fa774-130">Necessary for containers that support extended controls.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="fa774-131">**Showpropertyframe**</span><span class="sxs-lookup"><span data-stu-id="fa774-131">**ShowPropertyFrame**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | <span data-ttu-id="fa774-132">Erforderlich für Container, die eigene Eigenschaften Seiten einschließen möchten, um erweiterte Steuerelement Eigenschaften zusätzlich zu den von einem Steuerelement bereitgestellten Eigenschaften zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fa774-132">Necessary for containers that wish to include their own property pages to handle extended control properties in addition to those provided by a control.</span></span><br/> |
| [<span data-ttu-id="fa774-133">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="fa774-133">**TranslateAccelerator**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | <span data-ttu-id="fa774-134">Gibt möglicherweise \_ den Wert S false ohne Aktion zurück.</span><span class="sxs-lookup"><span data-stu-id="fa774-134">May return S\_FALSE with no action.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="fa774-135">**Lockinplaceactive**</span><span class="sxs-lookup"><span data-stu-id="fa774-135">**LockInPlaceActive**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | <span data-ttu-id="fa774-136">Optional</span><span class="sxs-lookup"><span data-stu-id="fa774-136">Optional</span></span><br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a><span data-ttu-id="fa774-137">IDispatch (Ambient-Eigenschaften)</span><span class="sxs-lookup"><span data-stu-id="fa774-137">IDispatch (Ambient properties)</span></span>



| <span data-ttu-id="fa774-138">Methode</span><span class="sxs-lookup"><span data-stu-id="fa774-138">Method</span></span>                      | <span data-ttu-id="fa774-139">Kommentare</span><span class="sxs-lookup"><span data-stu-id="fa774-139">Comments</span></span>                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fa774-140">Gettypeingefocount</span><span class="sxs-lookup"><span data-stu-id="fa774-140">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="fa774-141">Erforderlich für Container, die nicht standardmäßige Ambient-Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fa774-141">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="fa774-142">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="fa774-142">GetTypeInfo</span></span><br/>      | <span data-ttu-id="fa774-143">Erforderlich für Container, die nicht standardmäßige Ambient-Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fa774-143">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="fa774-144">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="fa774-144">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="fa774-145">Erforderlich für Container, die nicht standardmäßige Ambient-Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fa774-145">Necessary for containers that support non-standard ambient properties.</span></span><br/> |



 

## <a name="idispatch-event-sink"></a><span data-ttu-id="fa774-146">IDispatch (Ereignis Senke)</span><span class="sxs-lookup"><span data-stu-id="fa774-146">IDispatch (Event sink)</span></span>



| <span data-ttu-id="fa774-147">Methode</span><span class="sxs-lookup"><span data-stu-id="fa774-147">Method</span></span>                      | <span data-ttu-id="fa774-148">Kommentare</span><span class="sxs-lookup"><span data-stu-id="fa774-148">Comments</span></span>                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa774-149">Gettypeingefocount</span><span class="sxs-lookup"><span data-stu-id="fa774-149">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="fa774-150">Das Steuerelement kennt seine eigenen Typinformationen, sodass es nicht aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="fa774-150">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="fa774-151">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="fa774-151">GetTypeInfo</span></span><br/>      | <span data-ttu-id="fa774-152">Das Steuerelement kennt seine eigenen Typinformationen, sodass es nicht aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="fa774-152">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="fa774-153">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="fa774-153">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="fa774-154">Das Steuerelement kennt seine eigenen Typinformationen, sodass es nicht aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="fa774-154">The control knows its own type information, so it has no need to call this.</span></span><br/> |



 

## <a name="ioleinplaceframe"></a><span data-ttu-id="fa774-155">IOleInPlaceFrame</span><span class="sxs-lookup"><span data-stu-id="fa774-155">IOleInPlaceFrame</span></span>



| <span data-ttu-id="fa774-156">Methode</span><span class="sxs-lookup"><span data-stu-id="fa774-156">Method</span></span>                                                                           | <span data-ttu-id="fa774-157">Kommentare</span><span class="sxs-lookup"><span data-stu-id="fa774-157">Comments</span></span>                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="fa774-158">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="fa774-158">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [<span data-ttu-id="fa774-159">**GetBorder**</span><span class="sxs-lookup"><span data-stu-id="fa774-159">**GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | <span data-ttu-id="fa774-160">Erforderlich für Container mit der Symbolleisten-Benutzeroberfläche (optional)</span><span class="sxs-lookup"><span data-stu-id="fa774-160">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="fa774-161">**RequestBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="fa774-161">**RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | <span data-ttu-id="fa774-162">Erforderlich für Container mit der Symbolleisten-Benutzeroberfläche (optional)</span><span class="sxs-lookup"><span data-stu-id="fa774-162">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="fa774-163">**SetBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="fa774-163">**SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | <span data-ttu-id="fa774-164">Erforderlich für Container mit der Symbolleisten-Benutzeroberfläche (optional)</span><span class="sxs-lookup"><span data-stu-id="fa774-164">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="fa774-165">**Insertmenüs**</span><span class="sxs-lookup"><span data-stu-id="fa774-165">**InsertMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | <span data-ttu-id="fa774-166">Erforderlich für Container mit Menü Benutzeroberfläche (optional)</span><span class="sxs-lookup"><span data-stu-id="fa774-166">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="fa774-167">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="fa774-167">**SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | <span data-ttu-id="fa774-168">Erforderlich für Container mit Menü Benutzeroberfläche (optional)</span><span class="sxs-lookup"><span data-stu-id="fa774-168">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="fa774-169">**Removemenus**</span><span class="sxs-lookup"><span data-stu-id="fa774-169">**RemoveMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | <span data-ttu-id="fa774-170">Erforderlich für Container mit Menü Benutzeroberfläche (optional)</span><span class="sxs-lookup"><span data-stu-id="fa774-170">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="fa774-171">**SetStatusText**</span><span class="sxs-lookup"><span data-stu-id="fa774-171">**SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | <span data-ttu-id="fa774-172">Nur für Container mit einer Statuszeile erforderlich</span><span class="sxs-lookup"><span data-stu-id="fa774-172">Necessary only for containers that have a status line</span></span><br/>        |
| [<span data-ttu-id="fa774-173">**Enablemodeless**</span><span class="sxs-lookup"><span data-stu-id="fa774-173">**EnableModeless**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | <span data-ttu-id="fa774-174">Optional</span><span class="sxs-lookup"><span data-stu-id="fa774-174">Optional</span></span><br/>                                                     |
| [<span data-ttu-id="fa774-175">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="fa774-175">**TranslateAccelerator**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | <span data-ttu-id="fa774-176">Optional</span><span class="sxs-lookup"><span data-stu-id="fa774-176">Optional</span></span><br/>                                                     |



 

## <a name="iolecontainer"></a><span data-ttu-id="fa774-177">IOleContainer</span><span class="sxs-lookup"><span data-stu-id="fa774-177">IOleContainer</span></span>



| <span data-ttu-id="fa774-178">Methode</span><span class="sxs-lookup"><span data-stu-id="fa774-178">Method</span></span>                                                                    | <span data-ttu-id="fa774-179">Kommentare</span><span class="sxs-lookup"><span data-stu-id="fa774-179">Comments</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa774-180">**Name des Parametern**</span><span class="sxs-lookup"><span data-stu-id="fa774-180">**ParseDisplayName**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | <span data-ttu-id="fa774-181">Nur, wenn das Verknüpfen mit Steuerelementen oder anderen Einbettungen im Container unterstützt wird, da dies für die Monikerbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fa774-181">Only if linking to controls or other embeddings in the container is supported, as this is necessary for moniker binding.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="fa774-182">**Lockcontainer**</span><span class="sxs-lookup"><span data-stu-id="fa774-182">**LockContainer**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | <span data-ttu-id="fa774-183">Wie für "Parser Name"</span><span class="sxs-lookup"><span data-stu-id="fa774-183">As for ParseDisplayName</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="fa774-184">**EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="fa774-184">**EnumObjects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | <span data-ttu-id="fa774-185">Gibt alle ActiveX-Steuerelemente durch einen Enumerator mit [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown)zurück, jedoch nicht notwendigerweise alle-Objekte (da es keine Garantie gibt, dass alle Objekte ActiveX-Steuerelemente sind; einige können reguläre Windows-Steuerelemente sein).</span><span class="sxs-lookup"><span data-stu-id="fa774-185">Returns all ActiveX controls through an enumerator with [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), but not necessarily all objects (because there's no guarantee that all objects are ActiveX controls; some may be regular Windows controls).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fa774-186">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa774-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa774-187">Container</span><span class="sxs-lookup"><span data-stu-id="fa774-187">Containers</span></span>](containers.md)
</dt> </dl>

 

