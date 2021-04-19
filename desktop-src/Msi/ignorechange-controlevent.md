---
description: Das ignorechange ControlEvent wird vom directorylist-Steuerelement veröffentlicht, wenn der ausgewählte Ordner von einem Verzeichnis in ein anderes Verzeichnis im-Steuerelement geändert wird. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: Ignorechange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362422"
---
# <a name="ignorechange-controlevent"></a><span data-ttu-id="f0be9-104">Ignorechange ControlEvent</span><span class="sxs-lookup"><span data-stu-id="f0be9-104">IgnoreChange ControlEvent</span></span>

<span data-ttu-id="f0be9-105">Das ignorechange ControlEvent wird vom [directorylist-Steuer](directorylist-control.md) Element veröffentlicht, wenn der ausgewählte Ordner von einem Verzeichnis in ein anderes Verzeichnis im-Steuerelement geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f0be9-105">The IgnoreChange ControlEvent is published by the [DirectoryList control](directorylist-control.md) when the selected folder is changed from one directory to another directory in the control.</span></span> <span data-ttu-id="f0be9-106">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0be9-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="f0be9-107">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0be9-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f0be9-108">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f0be9-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f0be9-109">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f0be9-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f0be9-110">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="f0be9-110">Published By</span></span>

[<span data-ttu-id="f0be9-111">Directoren auflisten</span><span class="sxs-lookup"><span data-stu-id="f0be9-111">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="f0be9-112">Argument</span><span class="sxs-lookup"><span data-stu-id="f0be9-112">Argument</span></span>

<span data-ttu-id="f0be9-113">Dieses ControlEvent verwendet kein Argument.</span><span class="sxs-lookup"><span data-stu-id="f0be9-113">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f0be9-114">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="f0be9-114">Action on Subscribers</span></span>

<span data-ttu-id="f0be9-115">Diese ControlEvent führt keine Aktion für Abonnenten aus.</span><span class="sxs-lookup"><span data-stu-id="f0be9-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f0be9-116">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="f0be9-116">Typical Use</span></span>

<span data-ttu-id="f0be9-117">Das [directoriycombo-Steuer](directorycombo-control.md) Element verwendet häufig das ignorechange ControlEvent-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="f0be9-117">The [DirectoryCombo control](directorycombo-control.md) commonly employs the IgnoreChange ControlEvent.</span></span>

 

 



