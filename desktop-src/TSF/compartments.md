---
title: Fer
description: Fer
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Text Dienst Framework (TSF), Depots
- TSF (Text Dienst Framework), Depots
- Text Dienste, Depots
- TSF-aktivierte Anwendungen, Depots
- fer
- Text Dienst Framework (TSF), Depot-Typen
- TSF (Text Dienst Framework), Depot-Typen
- Text Dienste, Depot-Typen
- TSF-aktivierte Anwendungen, Depot Typen
- Depot Typen
- Text Dienst Framework (TSF), Depot Änderungs Benachrichtigungen
- TSF (Text Services Framework), Depot Änderungs Benachrichtigungen
- Text Dienste, Depot Änderungs Benachrichtigungen
- TSF-aktivierte Anwendungen, Depot Änderungs Benachrichtigungen
- Depot Änderungs Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206514"
---
# <a name="compartments"></a><span data-ttu-id="1b68d-118">Fer</span><span class="sxs-lookup"><span data-stu-id="1b68d-118">Compartments</span></span>

## <a name="compartment-types"></a><span data-ttu-id="1b68d-119">Depot Typen</span><span class="sxs-lookup"><span data-stu-id="1b68d-119">Compartment Types</span></span>

<span data-ttu-id="1b68d-120">Es gibt mehrere verschiedene Arten von Depots.</span><span class="sxs-lookup"><span data-stu-id="1b68d-120">There are several different types of compartments.</span></span> <span data-ttu-id="1b68d-121">Es gibt ein globales Depot, und jeder Thread-Manager, Dokument-Manager und Kontext kann ein Depot enthalten.</span><span class="sxs-lookup"><span data-stu-id="1b68d-121">There is a global compartment, and each thread manager, document manager, and context can contain a compartment.</span></span>

<span data-ttu-id="1b68d-122">Mit dem globalen Depot können Clients Daten Prozess übergreifend freigeben.</span><span class="sxs-lookup"><span data-stu-id="1b68d-122">The global compartment enables clients to share data across processes.</span></span> <span data-ttu-id="1b68d-123">Rufen Sie zum Abrufen des globalen Depot-Managers [**ITfThreadMgr:: getglobaldepot**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)auf.</span><span class="sxs-lookup"><span data-stu-id="1b68d-123">To obtain the global compartment manager, call [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span></span>

<span data-ttu-id="1b68d-124">Der Thread-Manager enthält einen Depot-Manager, der Depots pro Thread enthält.</span><span class="sxs-lookup"><span data-stu-id="1b68d-124">The thread manager contains a compartment manager that contains compartments on a per-thread basis.</span></span> <span data-ttu-id="1b68d-125">Dadurch können Daten in einem Thread freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b68d-125">This allows data to be shared within a thread.</span></span> <span data-ttu-id="1b68d-126">Um einen Thread-Manager-Depot-Manager zu erhalten, rufen Sie **ITfThreadMgr:: QueryInterface** mit IID \_ itfgliementmgr auf.</span><span class="sxs-lookup"><span data-stu-id="1b68d-126">To obtain a thread manager compartment manager, call **ITfThreadMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="1b68d-127">Jeder erstellte Dokument-Manager enthält auch einen Depot-Manager.</span><span class="sxs-lookup"><span data-stu-id="1b68d-127">Each document manager created also contains a compartment manager.</span></span> <span data-ttu-id="1b68d-128">Dadurch können Daten in einem bestimmten Dokument-Manager freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b68d-128">This allows data to be shared within a specific document manager.</span></span> <span data-ttu-id="1b68d-129">Um den Depot-Manager für den Dokument-Manager zu erhalten, rufen Sie **ITfDocumentMgr:: QueryInterface** mit IID \_ itfgliementmgr auf.</span><span class="sxs-lookup"><span data-stu-id="1b68d-129">To obtain the document manager compartment manager, call **ITfDocumentMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="1b68d-130">Jeder erstellte Kontext enthält auch einen Depot-Manager.</span><span class="sxs-lookup"><span data-stu-id="1b68d-130">Each context created also contains a compartment manager.</span></span> <span data-ttu-id="1b68d-131">Dadurch können Daten in einem bestimmten kontextfrei gegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b68d-131">This allows data to be shared within a specific context.</span></span> <span data-ttu-id="1b68d-132">Rufen Sie zum Abrufen eines Kontext Depot-Managers **ITfContext:: QueryInterface** mit IID \_ itfgliementmgr auf.</span><span class="sxs-lookup"><span data-stu-id="1b68d-132">To obtain a context compartment manager, call **ITfContext::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

## <a name="creating-and-deleting-a-compartment"></a><span data-ttu-id="1b68d-133">Erstellen und Löschen eines Depots</span><span class="sxs-lookup"><span data-stu-id="1b68d-133">Creating and Deleting a Compartment</span></span>

<span data-ttu-id="1b68d-134">Ein Depot wird erstellt, wenn [**itfgliementmgr:: getdepot**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) mit der Depot-GUID aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1b68d-134">A compartment is created the first time [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) is called with the compartment GUID.</span></span> <span data-ttu-id="1b68d-135">Der Installations Client sollte den Anfangswert des Depots mithilfe von [**itsdepot:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)festlegen.</span><span class="sxs-lookup"><span data-stu-id="1b68d-135">The installing client should set the initial value of the compartment using [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span></span> <span data-ttu-id="1b68d-136">Der Depot Wert ist leer, bis ein Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1b68d-136">Until a value is set, the compartment value is empty.</span></span> <span data-ttu-id="1b68d-137">Daher gibt es keine Möglichkeit, zu überprüfen, ob das Depot vorhanden war, bevor **getdepot** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="1b68d-137">Because of this, there is no way to verify that the compartment existed before **GetCompartment** was called.</span></span> <span data-ttu-id="1b68d-138">Um diese Situation zu vermeiden, sollte der Installations Client den Wert auf einen Anfangswert festlegen, damit andere Clients ermitteln können, ob das Depot bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1b68d-138">To avoid this situation, the installing client should set the value to some initial value so that other clients can determine if the compartment already exists.</span></span>

<span data-ttu-id="1b68d-139">Die [**itfgliementmgr:: cleardepot**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) -Methode wird zum Entfernen eines Depots verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b68d-139">The [**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) method is used to remove a compartment.</span></span> <span data-ttu-id="1b68d-140">Alle vorhandenen Verweise auf das Depot werden als ungültig markiert.</span><span class="sxs-lookup"><span data-stu-id="1b68d-140">Any existing references to the compartment are marked invalid.</span></span>

## <a name="obtaining-compartments"></a><span data-ttu-id="1b68d-141">Abrufen von Depots</span><span class="sxs-lookup"><span data-stu-id="1b68d-141">Obtaining Compartments</span></span>

<span data-ttu-id="1b68d-142">Mithilfe der [**itfgliementmgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) -Schnittstelle kann ein Client Depots durch Aufrufen von [**itfgliementmgr:: enumdepots**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)aufzählen.</span><span class="sxs-lookup"><span data-stu-id="1b68d-142">Using the [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) interface, a client can enumerate compartments by calling [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span></span> <span data-ttu-id="1b68d-143">Diese Methode stellt ein **ienumguid** -Objekt bereit, das die GUIDs aller installierten Depots enthält.</span><span class="sxs-lookup"><span data-stu-id="1b68d-143">This method provides an **IEnumGUID** object that contains the GUIDs of all of the installed compartments.</span></span>

<span data-ttu-id="1b68d-144">Mithilfe der Depot-GUID wird **itfgliementmgr:: getdepot** zum Abrufen eines bestimmten Depots verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b68d-144">Using the compartment GUID , **ITfCompartmentMgr::GetCompartment** is used to obtain a specific compartment.</span></span> <span data-ttu-id="1b68d-145">Diese Methode stellt dem Aufrufer ein [**itfdepot**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) -Objekt zur Verfügung, das die Depotdaten abrufen und festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="1b68d-145">This method provides the caller with an [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) object that can obtain and set the compartment data.</span></span>

## <a name="receiving-compartment-change-notifications"></a><span data-ttu-id="1b68d-146">Empfangen von Depot Änderungs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="1b68d-146">Receiving Compartment Change Notifications</span></span>

<span data-ttu-id="1b68d-147">Wenn sich der Wert eines Depots ändert, benachrichtigt der TSF-Manager alle installierten Empfehlung-senken, die das Depot geändert hat.</span><span class="sxs-lookup"><span data-stu-id="1b68d-147">When the value of a compartment changes, the TSF manager notifies any installed advise sinks that the compartment has changed.</span></span> <span data-ttu-id="1b68d-148">Erstellen Sie ein Objekt, das [**itfmenmenteventsink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)implementiert, um eine Depot-Änderungs-Senke zu installieren.</span><span class="sxs-lookup"><span data-stu-id="1b68d-148">To install a compartment change advise sink, create an object that implements [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span></span> <span data-ttu-id="1b68d-149">Rufen Sie dann **itfdepot:: QueryInterface** mit IID \_ itfsource für das Depot-Objekt auf, das überwacht werden soll, um eine [**itfsource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b68d-149">Then call **ITfCompartment::QueryInterface** with IID\_ITfSource on the compartment object to be monitored to obtain an [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) interface.</span></span> <span data-ttu-id="1b68d-150">Nennen Sie nun [**itfsource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) mit IID \_ itfmenmenteventsink und den Zeiger auf das **itfzersplimenteventsink** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b68d-150">Now call [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfCompartmentEventSink and the pointer to the **ITfCompartmentEventSink** object.</span></span> <span data-ttu-id="1b68d-151">Wenn sich der Wert des Depots ändert, wird die [**itfmenmenteventsink:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) -Eigenschaft der Benachrichtigungs Senke mit der GUID des Depots aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1b68d-151">When the value of the compartment changes, the advise sink's [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) is called with the GUID of the compartment.</span></span> <span data-ttu-id="1b68d-152">Die Hinweis Senke kann [**itfdepot:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) aufrufen, um den neuen Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b68d-152">The advise sink can call [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) to obtain the new value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b68d-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b68d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b68d-154">**ITF-mentmgr**</span><span class="sxs-lookup"><span data-stu-id="1b68d-154">**ITfCompartmentMgr**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[<span data-ttu-id="1b68d-155">**Itmadepot**</span><span class="sxs-lookup"><span data-stu-id="1b68d-155">**ITfCompartment**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[<span data-ttu-id="1b68d-156">**ITF-menteventsink**</span><span class="sxs-lookup"><span data-stu-id="1b68d-156">**ITfCompartmentEventSink**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[<span data-ttu-id="1b68d-157">**Tfclientid**</span><span class="sxs-lookup"><span data-stu-id="1b68d-157">**TfClientId**</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="1b68d-158">**ITfThreadMgr:: getglobaldepot**</span><span class="sxs-lookup"><span data-stu-id="1b68d-158">**ITfThreadMgr::GetGlobalCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[<span data-ttu-id="1b68d-159">**ITF-mentmgr:: getdepot**</span><span class="sxs-lookup"><span data-stu-id="1b68d-159">**ITfCompartmentMgr::GetCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[<span data-ttu-id="1b68d-160">**ITF Depot:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="1b68d-160">**ITfCompartment::SetValue**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[<span data-ttu-id="1b68d-161">**ITF-mentmgr:: cleardepot**</span><span class="sxs-lookup"><span data-stu-id="1b68d-161">**ITfCompartmentMgr::ClearCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[<span data-ttu-id="1b68d-162">**ITF-mentmgr:: enumdepots**</span><span class="sxs-lookup"><span data-stu-id="1b68d-162">**ITfCompartmentMgr::EnumCompartments**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[<span data-ttu-id="1b68d-163">**ITF-Quelle**</span><span class="sxs-lookup"><span data-stu-id="1b68d-163">**ITfSource**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[<span data-ttu-id="1b68d-164">**ITF Source:: AdviseSink**</span><span class="sxs-lookup"><span data-stu-id="1b68d-164">**ITfSource::AdviseSink**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[<span data-ttu-id="1b68d-165">**ITF-menteventsink:: OnChange**</span><span class="sxs-lookup"><span data-stu-id="1b68d-165">**ITfCompartmentEventSink::OnChange**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




