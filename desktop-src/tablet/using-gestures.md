---
description: Übersicht über die Verwendung von Gesten.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Verwenden von Gesten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958899"
---
# <a name="using-gestures"></a><span data-ttu-id="05d20-103">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="05d20-103">Using Gestures</span></span>

<span data-ttu-id="05d20-104">Die Tablet PC-Plattform bietet die Microsoft Gestenerkennung zum unterstützen von Anwendungs Gesten.</span><span class="sxs-lookup"><span data-stu-id="05d20-104">The Tablet PC platform provides the Microsoft gesture recognizer for supporting application gestures.</span></span> <span data-ttu-id="05d20-105">Eine Liste der Gesten, die von der Gestenerkennung von Microsoft unterstützt werden, finden Sie in der Tabelle mit Anwendungs Gesten in der [**applicationgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="05d20-105">For a list of gestures supported by the Microsoft gesture recognizer, see the table of application gestures in the [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration.</span></span> <span data-ttu-id="05d20-106">Der Tablet PC unterstützt auch System Gesten.</span><span class="sxs-lookup"><span data-stu-id="05d20-106">The Tablet PC also supports system gestures.</span></span> <span data-ttu-id="05d20-107">Eine Liste der System Gesten, die vom Tablet PC unterstützt werden, finden Sie in der Tabelle mit System Gesten in der [**systemgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="05d20-107">For a list of system gestures supported by the Tablet PC, see the table of system gestures in the [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration.</span></span>

## <a name="microsoft-gesture-recognizer"></a><span data-ttu-id="05d20-108">Gestenerkennung von Microsoft</span><span class="sxs-lookup"><span data-stu-id="05d20-108">Microsoft Gesture Recognizer</span></span>

<span data-ttu-id="05d20-109">Sie können die Microsoft Gestenerkennung mithilfe der [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) -Eigenschaft des [**InkCollector**](inkcollector-class.md) -Objekts, des [**InkOverlay**](inkoverlay-class.md) -Objekts oder des [InkPicture](inkpicture-control-reference.md) -Steuer Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="05d20-109">You can employ the Microsoft gesture recognizer by using the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property of the [**InkCollector**](inkcollector-class.md) object, the [**InkOverlay**](inkoverlay-class.md) object, or the [InkPicture](inkpicture-control-reference.md) control.</span></span> <span data-ttu-id="05d20-110">Wenn Sie die **CollectionMode** -Eigenschaft auf den gemischten Modus (**inkandgesten**) oder den Modus "nur Gesten" (**GestureOnly**) festlegen, werden frei Hand Eingaben standardmäßig an die Microsoft Gestenerkennung weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="05d20-110">Setting the **CollectionMode** property to mixed mode (**InkAndGesture**) or gesture-only mode (**GestureOnly**) passes ink to the Microsoft gesture recognizer by default.</span></span> <span data-ttu-id="05d20-111">Sie können die Microsoft Gestenerkennung mit dem [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden, indem Sie die Eigenschaft [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) auf **inkandgesten** festlegen.</span><span class="sxs-lookup"><span data-stu-id="05d20-111">You can employ the Microsoft gesture recognizer with the [InkEdit](inkedit-control-reference.md) control by setting the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property to **InkAndGesture**.</span></span> <span data-ttu-id="05d20-112">Sie können auch die Gestenerkennung mit dem [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) -Objekt verwenden, indem Sie einer der zugehörigen Plug-in-Auflistungen ein [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="05d20-112">You can also use gesture recognition with the [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) object by adding a [**GestureRecognizer**](gesturerecognizer-class.md) object to one of its plug-in collections.</span></span>

<span data-ttu-id="05d20-113">Wenn die Gesten, die Sie verwenden möchten, jedoch nicht von der aktuellen Version der Gestenerkennung von Microsoft unterstützt werden, können Sie Ihre eigene Erkennung erstellen und in Verbindung mit der Microsoft-Gestenerkennung verwenden.</span><span class="sxs-lookup"><span data-stu-id="05d20-113">However, if the gestures that you want to use are not supported by the current version of the Microsoft gesture recognizer, you can build your own recognizer and use it in conjunction with the Microsoft gesture recognizer.</span></span> <span data-ttu-id="05d20-114">Dies ermöglicht die vollständige Unterstützung der Gesten in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="05d20-114">This allows full support for the gestures in your application.</span></span>

<span data-ttu-id="05d20-115">Der Tablet PC verwendet einen Stift für einige oder alle Eingaben.</span><span class="sxs-lookup"><span data-stu-id="05d20-115">The Tablet PC uses a pen for some or all input.</span></span> <span data-ttu-id="05d20-116">Dadurch ist es sehr einfach, frei Hand Eingaben zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="05d20-116">This makes it extremely easy to write ink.</span></span> <span data-ttu-id="05d20-117">Die Tablet PC-Plattform bietet eine Architektur für Stift Eingaben, die eine mehrstufige Struktur von Gesten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05d20-117">The Tablet PC platform delivers architecture for pen input that supports a tiered structure of gestures.</span></span> <span data-ttu-id="05d20-118">Gesten und Zuordnung werden definiert, um dem Benutzer das Schreiben und aufrufen erweiterter Gesten auf neuen Oberflächen zu ermöglichen und gleichzeitig Gesten zu reservieren, die herkömmliche Maus Meldungen anderer Windows-basierter Anwendungen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="05d20-118">Gestures and mapping are defined to allow the user to write and invoke advanced gestures on new surfaces, while reserving gestures that invoke traditional mouse messages of other Windows-based applications.</span></span>

<span data-ttu-id="05d20-119">Die Tablet PC-Plattform führt zwei Ebenen von Gesten ein: System Gesten, auch als Systemereignisse bezeichnet und Anwendungs Gesten.</span><span class="sxs-lookup"><span data-stu-id="05d20-119">The Tablet PC platform introduces two levels of gestures: system gestures, also known as system events, and application gestures.</span></span> <span data-ttu-id="05d20-120">Die Pen-Architektur unterstützt sowohl System-als auch Anwendungs Gesten.</span><span class="sxs-lookup"><span data-stu-id="05d20-120">The pen architecture supports both system and application gestures.</span></span> <span data-ttu-id="05d20-121">Anwendungen mit nur einem Strich und mehreren Strichen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05d20-121">Both single-stroke and multiple-stroke application gestures are supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05d20-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05d20-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05d20-123">Anwendungs Gesten</span><span class="sxs-lookup"><span data-stu-id="05d20-123">Application Gestures</span></span>](application-gestures.md)
</dt> <dt>

[<span data-ttu-id="05d20-124">Gesten Flicks</span><span class="sxs-lookup"><span data-stu-id="05d20-124">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

[<span data-ttu-id="05d20-125">System Gesten</span><span class="sxs-lookup"><span data-stu-id="05d20-125">System Gestures</span></span>](system-gestures.md)
</dt> </dl>

 

 



