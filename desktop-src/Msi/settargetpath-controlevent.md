---
description: Das Ereignis settargetpath benachrichtigt den Installer, den ausgewählten Pfad zu überprüfen und festzulegen. Wenn der Pfad für den Schreibzugriff nicht gültig ist, blockiert der Installer weitere ControlEvents, die dem Steuerelement zugeordnet sind.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: Settargetpath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216933"
---
# <a name="settargetpath-controlevent"></a><span data-ttu-id="1ecaf-104">Settargetpath ControlEvent</span><span class="sxs-lookup"><span data-stu-id="1ecaf-104">SetTargetPath ControlEvent</span></span>

<span data-ttu-id="1ecaf-105">Das Ereignis settargetpath benachrichtigt den Installer, den ausgewählten Pfad zu überprüfen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-105">The SetTargetPath event notifies the installer to check and set the selected path.</span></span> <span data-ttu-id="1ecaf-106">Wenn der Pfad für den Schreibzugriff nicht gültig ist, blockiert der Installer weitere ControlEvents, die dem Steuerelement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-106">If the path is not valid to be written to, then the installer blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="1ecaf-107">Dieses Ereignis kann von einem [PUSHBUTTON-Steuer](pushbutton-control.md)Element oder einem [SelectionTree-Steuer](selectiontree-control.md)Element veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="1ecaf-108">Dieses Ereignis sollte in der [Tabelle ControlEvent](controlevent-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="1ecaf-109">Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="1ecaf-110">Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1ecaf-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="1ecaf-111">Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1ecaf-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="1ecaf-112">Veröffentlicht von</span><span class="sxs-lookup"><span data-stu-id="1ecaf-112">Published By</span></span>

<span data-ttu-id="1ecaf-113">Diese ControlEvent wird vom Installationsprogramm veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1ecaf-114">Argument</span><span class="sxs-lookup"><span data-stu-id="1ecaf-114">Argument</span></span>

<span data-ttu-id="1ecaf-115">Der Name der Eigenschaft, die den Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-115">The name of the property containing the path.</span></span> <span data-ttu-id="1ecaf-116">Wenn die Eigenschaft deretendiert ist, wird der Eigenschaftsname in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1ecaf-117">Aktion auf Abonnenten</span><span class="sxs-lookup"><span data-stu-id="1ecaf-117">Action on Subscribers</span></span>

<span data-ttu-id="1ecaf-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1ecaf-119">Typische Verwendung</span><span class="sxs-lookup"><span data-stu-id="1ecaf-119">Typical Use</span></span>

<span data-ttu-id="1ecaf-120">Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld zum Durchsuchen ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um den ausgewählten Pfad vor der Rückgabe zum Auswahl Dialogfeld zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ecaf-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ecaf-121">Remarks</span></span>

<span data-ttu-id="1ecaf-122">Versuchen Sie nicht, den Zielpfad zu konfigurieren, wenn die Komponenten, die diese Pfade verwenden, für den aktuellen Benutzer oder für einen anderen Benutzer bereits installiert sind.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-122">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="1ecaf-123">Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) vor dem Veröffentlichen von settargetpath ControlEvent, um zu bestimmen, ob das Produkt, das die Komponente enthält, installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ecaf-123">Check the [**ProductState**](productstate.md) property before publishing the SetTargetPath ControlEvent to determine if the product containing the component is installed.</span></span>

 

 



