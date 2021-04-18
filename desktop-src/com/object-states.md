---
title: Objektzustände
description: Objektzustände
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337145"
---
# <a name="object-states"></a><span data-ttu-id="63c2e-103">Objektzustände</span><span class="sxs-lookup"><span data-stu-id="63c2e-103">Object States</span></span>

<span data-ttu-id="63c2e-104">Ein Verbund Objekt ist in einem von drei Zuständen vorhanden: passiv, geladen oder wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63c2e-104">A compound object exists in one of three states: passive, loaded, or running.</span></span> <span data-ttu-id="63c2e-105">Der Zustand eines Verbund Dokument Objekts beschreibt die Beziehung zwischen dem Objekt in seinem Container und der Anwendung, die für seine Erstellung verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="63c2e-105">A compound-document object's state describes the relationship between the object in its container and the application responsible for its creation.</span></span> <span data-ttu-id="63c2e-106">In der folgenden Tabelle werden diese Zustände zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="63c2e-106">The following table summarizes these states.</span></span>



| <span data-ttu-id="63c2e-107">Objektstatus</span><span class="sxs-lookup"><span data-stu-id="63c2e-107">Object state</span></span>       | <span data-ttu-id="63c2e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63c2e-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63c2e-109">Passiv</span><span class="sxs-lookup"><span data-stu-id="63c2e-109">Passive</span></span><br/> | <span data-ttu-id="63c2e-110">Das Verbund Dokument Objekt ist nur im Speicher vorhanden, entweder auf einem Datenträger oder in einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="63c2e-110">The compound-document object exists only in storage, either on disk or in a database.</span></span> <span data-ttu-id="63c2e-111">In diesem Zustand ist das Objekt zum Anzeigen oder bearbeiten nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="63c2e-111">In this state, the object is unavailable for viewing or editing.</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="63c2e-112">Geladen</span><span class="sxs-lookup"><span data-stu-id="63c2e-112">Loaded</span></span><br/>  | <span data-ttu-id="63c2e-113">Die vom Objekt Handler erstellten Datenstrukturen des Objekts befinden sich im Arbeitsspeicher des Containers.</span><span class="sxs-lookup"><span data-stu-id="63c2e-113">The object's data structures created by the object handler are in the container's memory.</span></span> <span data-ttu-id="63c2e-114">Der Container hat die Kommunikation mit dem Objekt Handler hergestellt, und es stehen zwischengespeicherte Präsentationsdaten zum Rendern des Objekts zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="63c2e-114">The container has established communication with the object handler and there is cached presentation data available for rendering the object.</span></span> <span data-ttu-id="63c2e-115">Aufrufe werden vom Objekt Handler verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="63c2e-115">Calls are processed by the object handler.</span></span> <span data-ttu-id="63c2e-116">Dieser Zustand wird aufgrund des niedrigen Aufwands verwendet, wenn ein Benutzer ein Objekt einfach anzeigen oder drucken kann.</span><span class="sxs-lookup"><span data-stu-id="63c2e-116">This state, because of its low overhead, is used when a user is simply viewing or printing an object.</span></span><br/> |
| <span data-ttu-id="63c2e-117">Wird ausgeführt</span><span class="sxs-lookup"><span data-stu-id="63c2e-117">Running</span></span><br/> | <span data-ttu-id="63c2e-118">Die Objekte, die Remoting steuern, wurden erstellt, und die OLE-Serveranwendung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63c2e-118">The objects that control remoting have been created and the OLE server application is running.</span></span> <span data-ttu-id="63c2e-119">Der Zugriff auf die Schnittstellen des Objekts ist möglich, und der Container kann Benachrichtigungen über Änderungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="63c2e-119">The object's interfaces are accessible, and the container can receive notification of changes.</span></span> <span data-ttu-id="63c2e-120">In diesem Zustand kann ein Endbenutzer das Objekt bearbeiten oder anderweitig bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="63c2e-120">In this state, an end user can edit or otherwise manipulate the object.</span></span><br/>                                                                                                                    |



 

<span data-ttu-id="63c2e-121">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="63c2e-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="63c2e-122">Eingabe des geladenen Zustands</span><span class="sxs-lookup"><span data-stu-id="63c2e-122">Entering the Loaded State</span></span>](entering-the-loaded-state.md)
-   [<span data-ttu-id="63c2e-123">Eingeben des Status "wird ausgeführt"</span><span class="sxs-lookup"><span data-stu-id="63c2e-123">Entering the Running State</span></span>](entering-the-running-state.md)
-   [<span data-ttu-id="63c2e-124">Eingabe des passiven Zustands</span><span class="sxs-lookup"><span data-stu-id="63c2e-124">Entering the Passive State</span></span>](entering-the-passive-state.md)

## <a name="related-topics"></a><span data-ttu-id="63c2e-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63c2e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63c2e-126">Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="63c2e-126">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 





