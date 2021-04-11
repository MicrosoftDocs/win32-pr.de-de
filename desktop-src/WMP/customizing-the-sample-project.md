---
title: Anpassen des Beispielprojekts
description: Anpassen des Beispielprojekts
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player Online Stores, Anpassen von Beispielprojekten
- Online Stores, Anpassen von Beispielprojekten
- Geben Sie 2 Online Stores ein, und passen Sie Beispiel Projekte an.
- Windows Media Player Online Stores, Beispiel Projekte
- Online Stores, Beispiel Projekte
- Typ 2 Online Stores, Beispiel Projekte
- Anpassen von Beispielprojekten
- Beispiele, Typ 2 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948003"
---
# <a name="customizing-the-sample-project"></a><span data-ttu-id="a6409-111">Anpassen des Beispielprojekts</span><span class="sxs-lookup"><span data-stu-id="a6409-111">Customizing the Sample Project</span></span>

<span data-ttu-id="a6409-112">Beim Erstellen eines eigenen Online Stores möchten Sie die Implementierungen der folgenden Methoden in der Datei "yourproject. cpp" ändern:</span><span class="sxs-lookup"><span data-stu-id="a6409-112">When creating your own online store, you will want to change the implementations of the following methods in the file named YourProject.cpp:</span></span>

-   <span data-ttu-id="a6409-113">**Cyourproject:: allowplay**.</span><span class="sxs-lookup"><span data-stu-id="a6409-113">**CYourProject::allowPlay**.</span></span> <span data-ttu-id="a6409-114">Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, um die Wiedergabe geschützter Inhalte zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="a6409-114">Use this function to apply your business rules for permitting playback of protected content.</span></span>
-   <span data-ttu-id="a6409-115">**Cyourproject:: lässt cdburn** zu.</span><span class="sxs-lookup"><span data-stu-id="a6409-115">**CYourProject::allow CDBurn**.</span></span> <span data-ttu-id="a6409-116">Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf eine CD kopieren können.</span><span class="sxs-lookup"><span data-stu-id="a6409-116">Use this function to apply your business rules for allowing users to copy protected content to a CD.</span></span>
-   <span data-ttu-id="a6409-117">**Cyourproject:: allowpdatransfer**.</span><span class="sxs-lookup"><span data-stu-id="a6409-117">**CYourProject::allowPDATransfer**.</span></span> <span data-ttu-id="a6409-118">Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf ein tragbares Gerät übertragen können.</span><span class="sxs-lookup"><span data-stu-id="a6409-118">Use this function to apply your business rules for allowing users to transfer protected content to a portable device.</span></span>
-   <span data-ttu-id="a6409-119">**Cyourproject:: startbackgroundprocessing**.</span><span class="sxs-lookup"><span data-stu-id="a6409-119">**CYourProject::startBackgroundProcessing**.</span></span> <span data-ttu-id="a6409-120">Verwenden Sie diese Funktion, um alle erforderlichen Hintergrund Verarbeitungsaufgaben zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="a6409-120">Use this function to initiate any background processing tasks you require.</span></span> <span data-ttu-id="a6409-121">Beispielsweise können Sie dies als Gelegenheit zum Überprüfen auf abgelaufene Lizenzen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6409-121">For example, you might use this as an opportunity to check for expired licenses.</span></span>
-   <span data-ttu-id="a6409-122">**Cyourproject::d** entfernen.</span><span class="sxs-lookup"><span data-stu-id="a6409-122">**CYourProject::deviceAvailable**.</span></span> <span data-ttu-id="a6409-123">Verwenden Sie diese Funktion, um alle Aufgaben im Zusammenhang mit einem verbundenen Gerät zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="a6409-123">Use this function to initiate any tasks related to a connected device.</span></span>
-   <span data-ttu-id="a6409-124">**Cyourproject::p Analyse forsync**.</span><span class="sxs-lookup"><span data-stu-id="a6409-124">**CYourProject::prepareForSync**.</span></span> <span data-ttu-id="a6409-125">Verwenden Sie diese Funktion, um erforderliche Aufgaben auszuführen, bevor Sie digitale Medien mit dem Gerät synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="a6409-125">Use this function to perform necessary tasks just before synchronizing digital media to the device.</span></span>
-   <span data-ttu-id="a6409-126">**Cyourproject:: Service Event**.</span><span class="sxs-lookup"><span data-stu-id="a6409-126">**CYourProject::serviceEvent**.</span></span> <span data-ttu-id="a6409-127">Verwenden Sie diese Funktion, um Aufgaben zu starten und zu beenden, die Sie ausführen möchten, wenn Ihr Online Store aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a6409-127">Use this function to begin and end tasks that you want to run when your online store is the active one.</span></span>
-   <span data-ttu-id="a6409-128">**Cyourproject:: stopbackgroundprocessing**.</span><span class="sxs-lookup"><span data-stu-id="a6409-128">**CYourProject::stopBackgroundProcessing**.</span></span> <span data-ttu-id="a6409-129">Verwenden Sie diese Funktion, um alle Hintergrund Verarbeitungsaufgaben zu beenden, die Sie gestartet haben, als Windows Media Player den Namen **cyourproject:: startbackgroundprocessing** hat.</span><span class="sxs-lookup"><span data-stu-id="a6409-129">Use this function to stop any background processing tasks you started when Windows Media Player called **CYourProject::startBackgroundProcessing**.</span></span>

## <a name="working-with-media-and-playlist-objects"></a><span data-ttu-id="a6409-130">Arbeiten mit Medien-und Wiedergabelisten Objekten</span><span class="sxs-lookup"><span data-stu-id="a6409-130">Working with Media and Playlist Objects</span></span>

<span data-ttu-id="a6409-131">Die **allowplay** -Methode stellt einen Zeiger auf die **iwmpmedia** -Schnittstelle als Parameter bereit.</span><span class="sxs-lookup"><span data-stu-id="a6409-131">The **allowPlay** method provides a pointer to the **IWMPMedia** interface as a parameter.</span></span> <span data-ttu-id="a6409-132">Diese Schnittstelle ist die Windows Media Player-Schnittstelle, die Medienobjekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6409-132">This interface is the Windows Media Player interface that represents media objects.</span></span> <span data-ttu-id="a6409-133">Indem Sie die-Methoden für diese Schnittstelle aufrufen, können Sie mit den Attributen und Eigenschaften eines einzelnen Medien Elements arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a6409-133">By calling the methods on this interface, you can work with the attributes and properties of an individual media item.</span></span>

<span data-ttu-id="a6409-134">Die Methoden **allowcdburn** und **allowpdatransfer** stellen einen Zeiger auf die **iwmpwiedergabe** -Schnittstelle als Parameter bereit.</span><span class="sxs-lookup"><span data-stu-id="a6409-134">The **allowCDBurn** and **allowPDATransfer** methods provide a pointer to the **IWMPPlaylist** interface as a parameter.</span></span> <span data-ttu-id="a6409-135">Diese Schnittstelle ist die Windows Media Player-Schnittstelle, die Wiedergabelisten Objekte darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6409-135">This interface is the Windows Media Player interface that represents playlist objects.</span></span> <span data-ttu-id="a6409-136">Indem Sie die-Methoden für diese Schnittstelle aufrufen, können Sie mit den Attributen und Eigenschaften einer Wiedergabeliste arbeiten, Elemente zu einer Wiedergabeliste hinzufügen oder Elemente aus einer Wiedergabeliste entfernen.</span><span class="sxs-lookup"><span data-stu-id="a6409-136">By calling the methods on this interface, you can work with the attributes and properties of a playlist, add items to a playlist, or remove items from a playlist.</span></span>

<span data-ttu-id="a6409-137">Informationen zum programmgesteuerten Entfernen eines Elements aus einer Wiedergabeliste finden Sie in der Implementierung von **callowbasedialog <T> :: onremovemediafromplaylist**.</span><span class="sxs-lookup"><span data-stu-id="a6409-137">To learn how to remove an item from a playlist programmatically, see the implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span> <span data-ttu-id="a6409-138">Weitere Informationen zum Arbeiten mit Medien-und Wiedergabelisten Objekten finden Sie unter [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span><span class="sxs-lookup"><span data-stu-id="a6409-138">To learn more about working with media and playlist objects, see [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span></span>

## <a name="code-that-can-be-removed"></a><span data-ttu-id="a6409-139">Code, der entfernt werden kann</span><span class="sxs-lookup"><span data-stu-id="a6409-139">Code That Can Be Removed</span></span>

<span data-ttu-id="a6409-140">Wahrscheinlich möchten Sie den Code entfernen, der die Dialogfelder öffnet, da es unwahrscheinlich ist, dass Benutzer entscheiden, welche Medienelemente wiedergegeben oder kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a6409-140">You will probably want to remove the code that opens dialog boxes because it is unlikely that you will want users deciding which media items can be played or copied.</span></span> <span data-ttu-id="a6409-141">Entfernen Sie den folgenden Code aus yourproject. h:</span><span class="sxs-lookup"><span data-stu-id="a6409-141">From YourProject.h, remove the following code:</span></span>

-   <span data-ttu-id="a6409-142">Die Deklaration von **callowbasedialog**.</span><span class="sxs-lookup"><span data-stu-id="a6409-142">The declaration of **CAllowBaseDialog**.</span></span>
-   <span data-ttu-id="a6409-143">Die Deklaration von **callowburndialog**.</span><span class="sxs-lookup"><span data-stu-id="a6409-143">The declaration of **CAllowBurnDialog**.</span></span>
-   <span data-ttu-id="a6409-144">Die Deklaration von **callowtransferdialog**.</span><span class="sxs-lookup"><span data-stu-id="a6409-144">The declaration of **CAllowTransferDialog**.</span></span>

<span data-ttu-id="a6409-145">Entfernen Sie aus yourproject. cpp den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="a6409-145">From YourProject.cpp, remove the following code:</span></span>

-   <span data-ttu-id="a6409-146">Die Implementierung von **callowbasedialog <T> :: OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="a6409-146">The implementation of **CAllowBaseDialog<T>::OnInitDialog**.</span></span>
-   <span data-ttu-id="a6409-147">Die Implementierung von **callowbasedialog <T> :: onremovemediafromwiedergabe Liste**.</span><span class="sxs-lookup"><span data-stu-id="a6409-147">The implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6409-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6409-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6409-149">**Entwickeln des Plug-Ins für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="a6409-149">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




