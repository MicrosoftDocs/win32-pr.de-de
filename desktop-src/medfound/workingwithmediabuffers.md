---
description: Arbeiten mit DMO-Medien Puffern
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Arbeiten mit DMO-Medien Puffern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353254"
---
# <a name="working-with-dmo-media-buffers"></a><span data-ttu-id="6218d-103">Arbeiten mit DMO-Medien Puffern</span><span class="sxs-lookup"><span data-stu-id="6218d-103">Working with DMO Media Buffers</span></span>

<span data-ttu-id="6218d-104">Eingabedaten werden mithilfe von Medien Puffern an die Codec-DMOS übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6218d-104">Input data is passed to the codec DMOs using media buffers.</span></span> <span data-ttu-id="6218d-105">Ein Medien Puffer ist ein Objekt, das die [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="6218d-105">A media buffer is an object that implements the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="6218d-106">Zu diesem Zweck können Sie eine Klasse implementieren, oder Sie können die Puffer Objekte verwenden, die in diesem SDK definiert sind, wenn Sie das Windows Media-Format-SDK in der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="6218d-106">You can implement a class for this purpose or, if you are using the Windows Media Format SDK in your application, you can use the buffer objects that are defined in that SDK.</span></span>

<span data-ttu-id="6218d-107">Wenn Sie Ihre eigene Puffer Klasse implementieren, achten Sie darauf, wie der Puffer Arbeitsspeicher verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6218d-107">If you implement your own buffer class, be careful about how the buffer memory is handled.</span></span> <span data-ttu-id="6218d-108">Wenn Sie ein Eingabe Beispiel übergeben, behält der DMO einen Verweis auf den Puffer bei, bis das Beispiel abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6218d-108">When you pass an input sample, the DMO keeps a reference to the buffer until it is finished with the sample.</span></span> <span data-ttu-id="6218d-109">Sie können den Verweis auf die [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle sofort freigeben, aber Sie können nicht wissen, wann der Codec seinen Verweis nicht mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="6218d-109">You can immediately release your reference to the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface, but you have no way of knowing when the codec no longer needs its reference.</span></span> <span data-ttu-id="6218d-110">Um sicherzustellen, dass der Arbeitsspeicher freigegeben wird, wenn das Objekt sich selbst löscht, sollten Sie die Klasse implementieren, damit Sie den Speicher für den Puffer intern zuordnet und freigibt.</span><span class="sxs-lookup"><span data-stu-id="6218d-110">To be certain that the memory is freed when the object deletes itself, you should implement your class so that it allocates and frees the memory for the buffer internally.</span></span>

<span data-ttu-id="6218d-111">Da der DMOS für einen unbekannten Zeitraum Verweise auf Puffer aufbewahrt, ist es nicht sehr wichtig, einen begrenzten Pufferpool zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6218d-111">Because the DMOs keep references to buffers for an unknown period of time, it is not a trivial matter to use a limited pool of buffers.</span></span> <span data-ttu-id="6218d-112">Die einfachste Lösung besteht darin, für jedes Beispiel einen neuen Puffer zuzuweisen, obwohl dies ineffizient ist.</span><span class="sxs-lookup"><span data-stu-id="6218d-112">The simplest solution is to allocate a new buffer for each sample, although doing so is inefficient.</span></span>

<span data-ttu-id="6218d-113">Eine bessere Lösung ist die Implementierung eines Objekts zum Verwalten eines Pufferpools.</span><span class="sxs-lookup"><span data-stu-id="6218d-113">A better solution is to implement an object to manage a pool of buffers.</span></span> <span data-ttu-id="6218d-114">Schreiben Sie hierzu Code in der **releasemethode** Ihrer [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Implementierung, die eine Methode Ihres Puffer-Managers aufruft (anstatt sich selbst zu löschen), wenn der Verweis Zähler auf 0 (null) sinkt.</span><span class="sxs-lookup"><span data-stu-id="6218d-114">To do this, write code in the **Release** method of your [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementation that calls a method of your buffer manager (instead of deleting itself) when the reference count drops to zero.</span></span> <span data-ttu-id="6218d-115">Der Puffer-Manager kann dann eine Liste von Zeigern auf zugewiesene Puffer Objekte warten.</span><span class="sxs-lookup"><span data-stu-id="6218d-115">The buffer manager can then maintain a list of pointers to allocated buffer objects.</span></span> <span data-ttu-id="6218d-116">Erstellen Sie im Puffer-Manager eine Methode, um die Liste der freien Puffer zu überprüfen und einen Zeiger zurückzugeben, damit Ihre Anwendung bei Bedarf auf Puffer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6218d-116">Create a method in your buffer manager to check the list of free buffers and return a pointer so that your application can access buffers when needed.</span></span> <span data-ttu-id="6218d-117">Diese Methode sollte bei Bedarf neue Puffer erstellen und Sie der Liste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6218d-117">This method should create new buffers as needed and add them to the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6218d-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6218d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6218d-119">Arbeiten mit Codec-DMOS</span><span class="sxs-lookup"><span data-stu-id="6218d-119">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
