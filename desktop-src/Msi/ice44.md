---
description: ICE44 überprüft, ob im Dialogfeld "newdialog", "spawndialog" und "spawnwaitdialog" auf gültige Dialogfelder in der Dialogfeld Tabelle verwiesen wird.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362566"
---
# <a name="ice44"></a><span data-ttu-id="3afbc-103">ICE44</span><span class="sxs-lookup"><span data-stu-id="3afbc-103">ICE44</span></span>

<span data-ttu-id="3afbc-104">ICE44 überprüft, ob im Dialogfeld " [newdialog](newdialog-controlevent.md)", " [spawndialog](spawndialog-controlevent.md)" und " [spawnwaitdialog](spawnwaitdialog-controlevent.md) " auf gültige Dialogfelder in der [Dialogfeld Tabelle](dialog-table.md)verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3afbc-104">ICE44 validates that the [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md), and [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents reference valid dialog boxes in the [Dialog table](dialog-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="3afbc-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="3afbc-105">Result</span></span>

<span data-ttu-id="3afbc-106">ICE44 gibt eine Fehlermeldung aus, wenn ein Dialogfeld-Steuerelement vorhanden ist, das nicht auf ein Dialogfeld verweist, das in der Dialogfeld Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="3afbc-106">ICE44 posts an error message if there is a dialog control event that does not reference a dialog box listed in the Dialog table.</span></span>

## <a name="example"></a><span data-ttu-id="3afbc-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3afbc-107">Example</span></span>

<span data-ttu-id="3afbc-108">ICE44 würde die folgenden Fehler für das gezeigte Beispiel melden.</span><span class="sxs-lookup"><span data-stu-id="3afbc-108">ICE44 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="3afbc-109">ICE44-Fehler</span><span class="sxs-lookup"><span data-stu-id="3afbc-109">ICE44 error</span></span>                                                                                                                               | <span data-ttu-id="3afbc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3afbc-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3afbc-111">Steuerungs Ereignis für das Steuerelement "Dialog1". Control1 ' ist vom Typ spawndialog, das Argument Dialog2 ist jedoch kein gültiger Eintrag in der Dialog Feld Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3afbc-111">Control Event for Control 'Dialog1'.'Control1' is of type SpawnDialog, but its argument Dialog2 is not a valid entry in the Dialog Table.</span></span> | <span data-ttu-id="3afbc-112">Es gibt eine spawndialog-, spawnwaitdialog-oder newdialog-Aktion, die ein Argument aufweist, das in der Dialogfeld Tabelle nicht auf ein Dialogfeld verweist.</span><span class="sxs-lookup"><span data-stu-id="3afbc-112">There is a SpawnDialog, SpawnWaitDialog, or NewDialog actions that has an argument that does not refer to a dialog box in the Dialog table.</span></span> <span data-ttu-id="3afbc-113">Fügen Sie ein Argument hinzu, das ein Schlüssel in der Dialog Feld Tabelle ist, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="3afbc-113">To fix this error, add an argument that is a key in the Dialog Table.</span></span><br/> |



 

<span data-ttu-id="3afbc-114">[Dialog Feld Tabelle](dialog-table.md) (teilweise)</span><span class="sxs-lookup"><span data-stu-id="3afbc-114">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="3afbc-115">Dialog</span><span class="sxs-lookup"><span data-stu-id="3afbc-115">Dialog</span></span>  | <span data-ttu-id="3afbc-116">Titel</span><span class="sxs-lookup"><span data-stu-id="3afbc-116">Title</span></span> |
|---------|-------|
| <span data-ttu-id="3afbc-117">Dialog1</span><span class="sxs-lookup"><span data-stu-id="3afbc-117">Dialog1</span></span> |       |



 

<span data-ttu-id="3afbc-118">[ControlEvent-Tabelle](controlevent-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="3afbc-118">[ControlEvent Table](controlevent-table.md) (partial)</span></span>



| <span data-ttu-id="3afbc-119">Dialog\_</span><span class="sxs-lookup"><span data-stu-id="3afbc-119">Dialog\_</span></span> | <span data-ttu-id="3afbc-120">Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="3afbc-120">Control\_</span></span> | <span data-ttu-id="3afbc-121">type</span><span class="sxs-lookup"><span data-stu-id="3afbc-121">Type</span></span>        | <span data-ttu-id="3afbc-122">Argument</span><span class="sxs-lookup"><span data-stu-id="3afbc-122">Argument</span></span> |
|----------|-----------|-------------|----------|
| <span data-ttu-id="3afbc-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="3afbc-123">Dialog1</span></span>  | <span data-ttu-id="3afbc-124">Control1</span><span class="sxs-lookup"><span data-stu-id="3afbc-124">Control1</span></span>  | <span data-ttu-id="3afbc-125">Spawndialog</span><span class="sxs-lookup"><span data-stu-id="3afbc-125">SpawnDialog</span></span> | <span data-ttu-id="3afbc-126">Dialog2</span><span class="sxs-lookup"><span data-stu-id="3afbc-126">Dialog2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="3afbc-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3afbc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3afbc-128">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="3afbc-128">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




