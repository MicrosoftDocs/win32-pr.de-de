---
description: Das Installationsprogramm verwendet das setProgress-Ereignis, um Informationen über den Fortschritt der Installation zu veröffentlichen.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960152"
---
# <a name="setprogress-controlevent"></a><span data-ttu-id="d2cd9-103">SetProgress ControlEvent</span><span class="sxs-lookup"><span data-stu-id="d2cd9-103">SetProgress ControlEvent</span></span>

<span data-ttu-id="d2cd9-104">Das Installationsprogramm verwendet das setProgress-Ereignis, um Informationen über den Fortschritt der Installation zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-104">The installer uses the SetProgress event to publish information on the installation's progress.</span></span> <span data-ttu-id="d2cd9-105">Ein [ProgressBar-Steuer](progressbar-control.md) Element oder ein [Billboard-Steuer](billboard-control.md) Element sollte das Ereignis über die [EventMapping-Tabelle](eventmapping-table.md) abonnieren, indem er die Aktion benennt, deren Status angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-105">A [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) should subscribe to the event via the [EventMapping table](eventmapping-table.md) by naming the Action whose progress is being indicated.</span></span> <span data-ttu-id="d2cd9-106">Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="d2cd9-107">Diese ControlEvent kann von einer Benutzeroberfläche verarbeitet werden, die auf der [*grundlegenden*](b-gly.md)Benutzeroberfläche, der [*reduzierten*](r-gly.md)Benutzeroberfläche oder der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="d2cd9-108">Weitere Informationen zu UI-Ebenen finden Sie unter [Benutzeroberflächen](user-interface-levels.md)Ebenen.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="d2cd9-109">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="d2cd9-109">Published By</span></span>

<span data-ttu-id="d2cd9-110">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d2cd9-111">Argument</span><span class="sxs-lookup"><span data-stu-id="d2cd9-111">Argument</span></span>

<span data-ttu-id="d2cd9-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d2cd9-113">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="d2cd9-113">Action on Subscribers</span></span>

<span data-ttu-id="d2cd9-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d2cd9-115">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="d2cd9-115">Typical Use</span></span>

<span data-ttu-id="d2cd9-116">Ein [ProgressBar](progressbar-control.md) -Steuerelement in einem nicht modaldialog Feld abonniert dieses Ereignis mithilfe des [Progress](progress-control-attribute.md) -Attributs, um die Statusinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2cd9-116">A [ProgressBar](progressbar-control.md) control on a modeless dialog box subscribes to this event using the [Progress](progress-control-attribute.md) attribute to receive the progress information.</span></span>

 

 



