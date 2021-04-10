---
title: Automatisches Ändern der Größe von Rich-Edit-Steuerelementen
description: Eine Anwendung kann die Größe eines Rich-Edit-Steuer Elements nach Bedarf ändern, sodass es immer dieselbe Größe wie der Inhalt hat.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039698"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a><span data-ttu-id="f2b04-103">Automatisches Ändern der Größe von Rich-Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="f2b04-103">How to Automatically Resize Rich Edit Controls</span></span>

<span data-ttu-id="f2b04-104">Eine Anwendung kann die Größe eines Rich-Edit-Steuer Elements nach Bedarf ändern, sodass es immer dieselbe Größe wie der Inhalt hat.</span><span class="sxs-lookup"><span data-stu-id="f2b04-104">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="f2b04-105">Ein RichEdit-Steuerelement unterstützt diese so genannte, nicht *aufgerufene Funktion* , indem es das übergeordnete Fenster an den e-How-Wert der Datei " [ \_ RequestResize](en-requestresize.md) " sendet.</span><span class="sxs-lookup"><span data-stu-id="f2b04-105">A rich edit control supports this so-called *bottomless* functionality by sending its parent window an [EN\_REQUESTRESIZE](en-requestresize.md) notification code whenever the size of the control's content changes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f2b04-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="f2b04-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f2b04-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="f2b04-107">Technologies</span></span>

-   [<span data-ttu-id="f2b04-108">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="f2b04-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f2b04-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f2b04-109">Prerequisites</span></span>

-   <span data-ttu-id="f2b04-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="f2b04-110">C/C++</span></span>
-   <span data-ttu-id="f2b04-111">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="f2b04-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f2b04-112">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="f2b04-112">Instructions</span></span>

### <a name="automatically-resize-a-rich-edit-control"></a><span data-ttu-id="f2b04-113">Automatisches Ändern der Größe eines Rich-Edit-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="f2b04-113">Automatically Resize a Rich Edit Control</span></span>

<span data-ttu-id="f2b04-114">Bei der Verarbeitung des Benachrichtigungs Codes " [en \_ RequestResize](en-requestresize.md) " sollte eine Anwendung die Größe des Steuer Elements auf die Dimensionen in der angegebenen [**reqresize**](/windows/desktop/api/Richedit/ns-richedit-reqresize) -Struktur ändern.</span><span class="sxs-lookup"><span data-stu-id="f2b04-114">When processing the [EN\_REQUESTRESIZE](en-requestresize.md) notification code, an application should resize the control to the dimensions in the specified [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure.</span></span> <span data-ttu-id="f2b04-115">Eine Anwendung kann auch alle Informationen verschieben, die sich in der Nähe des Steuer Elements befinden, um die Änderung der Höhe des Steuer Elements zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f2b04-115">An application might also move any information that is near the control to accommodate the control's change in height.</span></span> <span data-ttu-id="f2b04-116">Um die Größe des Steuer Elements zu ändern, können Sie die [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2b04-116">To resize the control, you can use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function.</span></span>

<span data-ttu-id="f2b04-117">Sie können ein nicht gesteuerloses Bearbeitungs Steuerelement erzwingen, um einen [en \_ RequestResize](en-requestresize.md) -Benachrichtigungs Code mithilfe der [**EM \_ RequestResize**](em-requestresize.md) -Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="f2b04-117">You can force a bottomless rich edit control to send an [EN\_REQUESTRESIZE](en-requestresize.md) notification code by using the [**EM\_REQUESTRESIZE**](em-requestresize.md) message.</span></span> <span data-ttu-id="f2b04-118">Diese Meldung kann nützlich sein, wenn die [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f2b04-118">This message can be useful when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2b04-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2b04-119">Remarks</span></span>

<span data-ttu-id="f2b04-120">Zum Empfangen von [en \_ RequestResize](en-requestresize.md) -Benachrichtigungs Codes müssen Sie die Benachrichtigung mithilfe der Nachricht [EM \_ SetEventMask](em-seteventmask.md) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f2b04-120">To receive [EN\_REQUESTRESIZE](en-requestresize.md) notification codes, you must enable the notification by using the [EM\_SETEVENTMASK](em-seteventmask.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2b04-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2b04-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b04-122">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="f2b04-122">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="f2b04-123">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="f2b04-123">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 