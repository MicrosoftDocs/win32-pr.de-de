---
description: Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die im Echt Zeit Tablettstift verwendet werden.
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: RealTimeStylus-Klassen und-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866132"
---
# <a name="realtimestylus-classes-and-interfaces"></a><span data-ttu-id="cab39-103">RealTimeStylus-Klassen und-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cab39-103">RealTimeStylus Classes and Interfaces</span></span>

<span data-ttu-id="cab39-104">Dieser Abschnitt enthält Informationen zu den Schnittstellen und Klassen, die im Echt Zeit Tablettstift verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cab39-104">This section contains information about the interfaces and classes used in the real time stylus.</span></span>

> [!Note]  
> <span data-ttu-id="cab39-105">Die Klassen und Schnittstellen für echt Zeit Stile sind nicht Automatisierungs konform.</span><span class="sxs-lookup"><span data-stu-id="cab39-105">The real time stylus classes and interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="cab39-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cab39-106">In This Section</span></span>



| <span data-ttu-id="cab39-107">Klasse</span><span class="sxs-lookup"><span data-stu-id="cab39-107">Class</span></span>                                                      | <span data-ttu-id="cab39-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cab39-108">Description</span></span>                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cab39-109">**RealTimeStylus-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cab39-109">**RealTimeStylus Class**</span></span>](realtimestylus-class.md)       | <span data-ttu-id="cab39-110">Implementiert die [**irealtimestylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cab39-110">Implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) interface.</span></span><br/>                 |
| <span data-ttu-id="cab39-111">[**DynamicRenderer-Klasse**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cab39-111">[**DynamicRenderer Class**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>     | <span data-ttu-id="cab39-112">Implementiert die [**Schnittstelle der idynamicrenderer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) .</span><span class="sxs-lookup"><span data-stu-id="cab39-112">Implements the [**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) interface.</span></span><br/>     |
| [<span data-ttu-id="cab39-113">**GestureRecognizer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cab39-113">**GestureRecognizer Class**</span></span>](gesturerecognizer-class.md) | <span data-ttu-id="cab39-114">Implementiert die [**igesturerecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cab39-114">Implements the [**IGestureRecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) interface.</span></span><br/> |
| [<span data-ttu-id="cab39-115">**Strokebuilder-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cab39-115">**StrokeBuilder Class**</span></span>](strokebuilder-class.md)         | <span data-ttu-id="cab39-116">Implementiert die [**istrokebuilder-Schnittstellen**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cab39-116">Implements the [**IStrokeBuilder Interface**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) interface.</span></span><br/>         |



 

## <a name="interfaces"></a><span data-ttu-id="cab39-117">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cab39-117">Interfaces</span></span>



| <span data-ttu-id="cab39-118">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cab39-118">Interface</span></span>                                                                          | <span data-ttu-id="cab39-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cab39-119">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cab39-120">**Idynamicrenderer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cab39-120">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | <span data-ttu-id="cab39-121">Macht Methoden verfügbar, mit denen Sie die Anzeige von Tablettstiftdaten in Echtzeit steuern können, wenn die Daten vom [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cab39-121">Exposes methods enabling you to control the display of stylus data in real time as the data is being handled by the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/> |
| [<span data-ttu-id="cab39-122">**Igesturerecognizer-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cab39-122">**IGestureRecognizer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | <span data-ttu-id="cab39-123">Macht Methoden verfügbar, mit denen Sie auf Ereignisse reagieren können, indem Sie Stift Bewegungen erkennen und Daten zur Eingabe Warteschlange hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cab39-123">Exposes methods enabling you to react to events by recognizing stylus gestures and enabling you to add data to the input queue.</span></span><br/>                                                  |
| [<span data-ttu-id="cab39-124">**Irealtimestylus**</span><span class="sxs-lookup"><span data-stu-id="cab39-124">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | <span data-ttu-id="cab39-125">Verarbeitet die tablettstiftpaketdaten von einem Digitalisierer in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="cab39-125">Handles the stylus packet data from a digitizer in real time.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="cab39-126">**IRealTimeStylus2**</span><span class="sxs-lookup"><span data-stu-id="cab39-126">**IRealTimeStylus2**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | <span data-ttu-id="cab39-127">Erweitert die irealtimestylus-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cab39-127">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="cab39-128">**IRealTimeStylus3**</span><span class="sxs-lookup"><span data-stu-id="cab39-128">**IRealTimeStylus3**</span></span>](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | <span data-ttu-id="cab39-129">Erweitert die irealtimestylus-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cab39-129">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="cab39-130">**Irealtimestylussynchronization-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cab39-130">**IRealTimeStylusSynchronization Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | <span data-ttu-id="cab39-131">Synchronisiert den Zugriff auf das [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="cab39-131">Synchronizes access to the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/>                                                                                          |
| [<span data-ttu-id="cab39-132">**Istrokebuilder-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cab39-132">**IStrokeBuilder Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | <span data-ttu-id="cab39-133">Macht Methoden verfügbar, die es Ihnen ermöglichen, Striche Programm gesteuert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cab39-133">Exposes methods that enable you to programmatically create strokes.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="cab39-134">**Istylusplugin-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cab39-134">**IStylusPlugin Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | <span data-ttu-id="cab39-135">Macht Methoden verfügbar, mit denen Sie Benachrichtigungen zu Ereignissen empfangen und auf der Grundlage dieser Ereignisse eine benutzerdefinierte Verarbeitung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="cab39-135">Exposes methods enabling you to receive notifications of events and to perform custom processing based on those events.</span></span><br/>                                                          |
| [<span data-ttu-id="cab39-136">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="cab39-136">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | <span data-ttu-id="cab39-137">Stellt ein asynchrones Plug-in dar, das der asynchronen Plug-in-Auflistung der [**RealTimeStylus-Klasse**](realtimestylus-class.md) hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cab39-137">Represents an asynchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) asynchronous plug-in collection.</span></span><br/>                                |
| [<span data-ttu-id="cab39-138">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="cab39-138">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | <span data-ttu-id="cab39-139">Stellt ein synchrones Plug-in dar, das der synchronen Plug-in-Auflistung der [**RealTimeStylus-Klasse**](realtimestylus-class.md) hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cab39-139">Represents a synchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) synchronous plug-in collection.</span></span><br/>                                   |



 

## <a name="return-values"></a><span data-ttu-id="cab39-140">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cab39-140">Return Values</span></span>

<span data-ttu-id="cab39-141">Methoden in der com-Bibliothek geben Werte von **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="cab39-141">Methods in the COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="cab39-142">Sofern nicht anders angegeben, werden die Bedeutungen der **HRESULT** -Werte in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cab39-142">Unless otherwise noted, the meanings of the **HRESULT** values are described in the following table.</span></span>



| <span data-ttu-id="cab39-143">HRESULT-Wert</span><span class="sxs-lookup"><span data-stu-id="cab39-143">HRESULT value</span></span>                                   | <span data-ttu-id="cab39-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cab39-144">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cab39-145">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="cab39-145">S\_OK</span></span><br/>                                | <span data-ttu-id="cab39-146">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cab39-146">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="cab39-147">E- \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="cab39-147">E\_POINTER</span></span><br/>                           | <span data-ttu-id="cab39-148">Mindestens ein Zeiger (entweder für einen Eingabe-oder einen Output-Parameter) ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cab39-148">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="cab39-149">E \_ invalidArg</span><span class="sxs-lookup"><span data-stu-id="cab39-149">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="cab39-150">Der Member hat versucht, ein ungültiges Argument zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cab39-150">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="cab39-151">E- \_ Ink- \_ Ausnahme</span><span class="sxs-lookup"><span data-stu-id="cab39-151">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="cab39-152">Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="cab39-152">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="cab39-153">E \_ outo-Memory</span><span class="sxs-lookup"><span data-stu-id="cab39-153">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="cab39-154">Das System kann keinen Arbeitsspeicher zuweisen, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cab39-154">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="cab39-155">E \_ fehlschlagen</span><span class="sxs-lookup"><span data-stu-id="cab39-155">E\_FAIL</span></span><br/>                              | <span data-ttu-id="cab39-156">Ein nicht spezifizierter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="cab39-156">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="cab39-157">E \_ InvalidOperation</span><span class="sxs-lookup"><span data-stu-id="cab39-157">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="cab39-158">Der Member hat versucht, einen ungültigen Vorgang zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cab39-158">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="cab39-159">TPC \_ E \_ ungültiger \_ Modus</span><span class="sxs-lookup"><span data-stu-id="cab39-159">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="cab39-160">Der Member hat versucht, einen ungültigen Modus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cab39-160">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="cab39-161">TPC \_ E \_ - \_ Konfiguration ungültig</span><span class="sxs-lookup"><span data-stu-id="cab39-161">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="cab39-162">Der Member hat versucht, eine ungültige Konfiguration zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cab39-162">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="cab39-163">TPC \_ E \_ ungültige \_ Paket \_ Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cab39-163">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="cab39-164">Der Member hat versucht, eine ungültige Paketbeschreibung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cab39-164">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="cab39-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cab39-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cab39-166">RealTimeStylus-Referenz</span><span class="sxs-lookup"><span data-stu-id="cab39-166">RealTimeStylus Reference</span></span>](realtimestylus-reference.md)
</dt> </dl>

 

 
