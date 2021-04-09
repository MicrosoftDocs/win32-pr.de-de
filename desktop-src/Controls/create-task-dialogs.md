---
title: Erstellen von Aufgaben Dialogfeldern
description: Ein Aufgaben Dialogfeld wird erstellt und entweder mithilfe der taskdialog-Funktion oder der TaskDialogIndirect-Funktion angezeigt.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036536"
---
# <a name="how-to-create-task-dialogs"></a><span data-ttu-id="5572e-103">Erstellen von Aufgaben Dialogfeldern</span><span class="sxs-lookup"><span data-stu-id="5572e-103">How to Create Task Dialogs</span></span>

<span data-ttu-id="5572e-104">Ein Aufgaben Dialogfeld wird erstellt und entweder mithilfe der [**taskdialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) -Funktion oder der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5572e-104">A task dialog is created and shown by using either the [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) function or the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5572e-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="5572e-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5572e-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="5572e-106">Technologies</span></span>

-   [<span data-ttu-id="5572e-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="5572e-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5572e-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5572e-108">Prerequisites</span></span>

-   <span data-ttu-id="5572e-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="5572e-109">C/C++</span></span>
-   <span data-ttu-id="5572e-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="5572e-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5572e-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="5572e-111">Instructions</span></span>

### <a name="taskdialog"></a><span data-ttu-id="5572e-112">Nenne</span><span class="sxs-lookup"><span data-stu-id="5572e-112">TaskDialog</span></span>

<span data-ttu-id="5572e-113">Die **taskdialog** -Funktion eignet sich für einfache Dialogfelder, die Textinformationen darstellen und eine Standardauswahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="5572e-113">The **TaskDialog** function is suitable for simple dialog boxes that present textual information and ask for a standard choice.</span></span> <span data-ttu-id="5572e-114">Diese Erstellungs Funktion unterstützt keine Status leisten, Kontrollkästchen, Fußzeilen, Schaltflächen zum erweitern/reduzieren, benutzerdefinierte Schaltflächen oder Options Felder.</span><span class="sxs-lookup"><span data-stu-id="5572e-114">This creation function does not support progress bars, check boxes, footers, expand/collapse buttons, custom buttons, or radio buttons.</span></span>

### <a name="taskdialogindirect"></a><span data-ttu-id="5572e-115">TaskDialogIndirect</span><span class="sxs-lookup"><span data-stu-id="5572e-115">TaskDialogIndirect</span></span>

<span data-ttu-id="5572e-116">Die **TaskDialogIndirect** -Funktion ist leistungsfähiger und unterstützt alle verfügbaren Schnittstellen Elemente und ermöglicht es Ihnen, Ereignisse in einer Rückruf Prozedur zu erfassen, damit die Anwendung eine Statusanzeige aktualisieren oder auf einen Link oder eine Schaltfläche klicken kann.</span><span class="sxs-lookup"><span data-stu-id="5572e-116">The **TaskDialogIndirect** function is more powerful, supporting all available interface elements and also enabling you to capture events in a callback procedure so that your application can update a progress bar or respond to a click of a hyperlink or button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5572e-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5572e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5572e-118">Verwenden von Aufgaben Dialog</span><span class="sxs-lookup"><span data-stu-id="5572e-118">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 




