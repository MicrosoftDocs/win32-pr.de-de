---
title: Die Edge-Benutzeroberfläche wird in Szenarios mit "in-out-in" und "Trägheit" unterdrückt.
description: Die Edge-Benutzeroberfläche wird in Szenarios mit "in-out-in" und "Trägheit" unterdrückt.
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207315"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a><span data-ttu-id="e5933-103">Die Edge-Benutzeroberfläche wird in Szenarios mit "in-out-in" und "Trägheit" unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="e5933-103">Edge UI is suppressed in “in-out-in” and “inertia” scenarios</span></span>

## <a name="platform"></a><span data-ttu-id="e5933-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="e5933-104">Platform</span></span>

<dl> <span data-ttu-id="e5933-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e5933-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="e5933-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5933-106">Description</span></span>

<span data-ttu-id="e5933-107">In einigen Fällen kann es vorkommen, dass Benutzer versehentlich Edge-UI aufrufen (Charms, App-Leiste, App-Wechsel).</span><span class="sxs-lookup"><span data-stu-id="e5933-107">There are some cases where users may unintentionally invoke Edge UI (Charms, App Bar, app switching).</span></span> <span data-ttu-id="e5933-108">Wir haben eine Funktion eingeführt, die es Entwicklern ermöglicht, Ihre Benutzeroberfläche für den gesamten Bildschirm zu entwerfen, ohne dass Sie eine Fülle (z. b. Rahmen) erstellen müssen, um zu verhindern, dass der Benutzer versehentlich die Ränder</span><span class="sxs-lookup"><span data-stu-id="e5933-108">We have introduced a feature to allow developers to design their UI for the whole screen without making affordances (for example, borders) to prevent the user from accidentally hitting the edges.</span></span>

<span data-ttu-id="e5933-109">Es gibt zwei Fälle, die in den meisten Fällen dazu führen können, dass unbeabsichtigte Kanten geroutete Kanten entstehen:</span><span class="sxs-lookup"><span data-stu-id="e5933-109">There are two cases that might lead most often to inadvertent edge swipes:</span></span>

-   <span data-ttu-id="e5933-110">Beim schnellen schwenken können die Geschwindigkeit und die Ungenauigkeit der Interaktion gelegentlich bewirken, dass Sie vom Bildschirmrand ausgehen.</span><span class="sxs-lookup"><span data-stu-id="e5933-110">In fast panning, the speed and imprecision of the interaction can occasionally cause them to come in from the edge of the screen</span></span>
-   <span data-ttu-id="e5933-111">Wenn Benutzer den Bildschirmbereich beim Binden mit dem Finger, z. b. in einer Zeichnungs-APP, schnell verlassen und erneut eingeben, kann dieses Voreingegebene Verhalten versehentlich die Edge-Benutzeroberfläche auslöst und die Benutzeroberfläche unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="e5933-111">If users rapidly leave and re-enter the screen area while inking with their finger, for example, in a painting app, this in-out-in behavior can mistakenly trigger the Edge UI and interrupt the user experience</span></span>

<span data-ttu-id="e5933-112">Um die Benutzer-und Entwickler Oberfläche zu verbessern, wird die Edge-Benutzeroberfläche nun in zwei bestimmten Instanzen unterdrückt:</span><span class="sxs-lookup"><span data-stu-id="e5933-112">To improve the user and developer experience, the Edge UI will now be suppressed in two specific instances:</span></span>

-   <span data-ttu-id="e5933-113">Wenn ein Benutzer in einer Anwendung, die dmanip-Trägheit unterstützt und während der Trägheit auftritt, auf den Bildschirm zeigt, wird die Edge-Benutzeroberfläche nicht innerhalb eines Timeout Fensters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e5933-113">When a user is panning in an application that supports DManip Inertia and swipes outside of the screen while inertia is occurring, the Edge UI will not be invoked within a timeout window</span></span>
-   <span data-ttu-id="e5933-114">Auf zertifizierten Geräten wird die Edge-Benutzeroberfläche nicht aufgerufen, wenn ein Benutzer innerhalb bestimmter Parameter schnell vom Bildschirm auf den Bildschirm außerhalb des Bildschirms und wieder in (in-out-of-Motion) aufzieht.</span><span class="sxs-lookup"><span data-stu-id="e5933-114">On certified devices, when a user quickly swipes from within the screen to outside the screen and back inside (in-out-in motion) within certain parameters, the Edge UI will not be invoked</span></span>

## <a name="manifestations"></a><span data-ttu-id="e5933-115">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="e5933-115">Manifestations</span></span>

<span data-ttu-id="e5933-116">Benutzer können schnell auf den Rand schwenken, während bei der Verwendung einer App eine Abnahme des unbeabsichtigten Edge-Aufforderungen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e5933-116">Users quickly swiping against the edge while using an app will see a decrease in unintentional edge invocation.</span></span>

## <a name="solution"></a><span data-ttu-id="e5933-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="e5933-117">Solution</span></span>

<span data-ttu-id="e5933-118">Entwickler sollten diese entschärfungen berücksichtigen und sollten in der Lage sein, den Vollbildmodus zu verwenden, ohne zu befürchten, dass Benutzer bei der Interaktion mit der Anwendung auf dem Edge versehentlich die Edge-Benutzeroberfläche auslöst.</span><span class="sxs-lookup"><span data-stu-id="e5933-118">Developers should keep these mitigations in mind and should be able to use the full screen without fear that users will accidentally trigger the Edge UI while interacting with the application along the edge.</span></span>

 

 




