---
title: SendMessage, PostMessage und verwandte Funktionen
description: In diesem Abschnitt werden Überlegungen zum Weiterleiten von Nachrichten mit SendMessage, PostMessage und verwandten Funktionen mit Berührungs Nachrichten beschrieben.
ms.assetid: 9fba2013-17a3-499c-80dc-627e89c0edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fc42e31f3c971c704d18f04a961fb6bd40eb91d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390638"
---
# <a name="sendmessage-postmessage-and-related-functions"></a><span data-ttu-id="e14ff-103">SendMessage, PostMessage und verwandte Funktionen</span><span class="sxs-lookup"><span data-stu-id="e14ff-103">SendMessage, PostMessage, and Related Functions</span></span>

<span data-ttu-id="e14ff-104">In diesem Abschnitt werden Überlegungen zum Weiterleiten von Nachrichten mit [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)und verwandten Funktionen mit Berührungs Nachrichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e14ff-104">This section describes considerations about forwarding messages using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), and related functions with touch messages.</span></span>

<span data-ttu-id="e14ff-105">Wenn eine Fingereingabe Nachricht mit [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [Post Message](/windows/win32/api/winuser/nf-winuser-postmessagea)oder einer anderen verknüpften Funktion weitergeleitet wird, wird das Fingereingabe Handle geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e14ff-105">If a touch message is forwarded using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some other related function, the touch input handle is closed.</span></span> <span data-ttu-id="e14ff-106">Wenn Sie die Informationen, auf die von einem Fingereingabe handle verwiesen wird, über einen aufgerufenen [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)abgerufen haben, bleiben diese Daten gültig, bis Sie den Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="e14ff-106">If you have retrieved the information contained referenced by a touch input handle through a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo), that data will remain valid until you free the memory.</span></span>

<span data-ttu-id="e14ff-107">Eine Anwendung, die über einen dieser Mechanismen weitergeleitete Berührungs Nachrichten empfängt, besitzt das Fingereingabe handle, das in der Nachricht *LPARAM* empfangen wird und für deren Schließung zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="e14ff-107">An application that receives touch messages forwarded through one of these mechanisms owns the touch input handle it receives in the message *LPARAM* and is responsible for closing it.</span></span> <span data-ttu-id="e14ff-108">Wenn Sie das Handle nicht mit einem Rückruf von [**closetouchinputhandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)schließen, die Nachricht an [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)übergeben oder die Nachricht mit [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea)oder einer zugehörigen Funktion weiterleiten, liegt ein Speicherfehler vor.</span><span class="sxs-lookup"><span data-stu-id="e14ff-108">If you don't close the handle with a call to [**CloseTouchInputHandle**](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle), pass the message to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), or forward the message using [SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage), [PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea), or some related function, you will have a memory leak.</span></span>

> [!Note]  
> <span data-ttu-id="e14ff-109">Berührungs Nachrichten unterliegen den normalen UIPI-Regeln (User Interface Privilege Isolation), wenn Sie weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="e14ff-109">Touch messages are subject to normal User Interface Privilege Isolation (UIPI) rules when they are forwarded.</span></span>

 

## <a name="functions-related-to-sendmessage-and-postmessage"></a><span data-ttu-id="e14ff-110">Funktionen im Zusammenhang mit SendMessage und PostMessage</span><span class="sxs-lookup"><span data-stu-id="e14ff-110">Functions related to SendMessage and PostMessage</span></span>

<span data-ttu-id="e14ff-111">Die folgenden Funktionen, die den Zustand des Berührungs Eingabe Handles beeinflussen können.</span><span class="sxs-lookup"><span data-stu-id="e14ff-111">The following functions that can affect the state of the touch input handle.</span></span>

-   [<span data-ttu-id="e14ff-112">SendMessage</span><span class="sxs-lookup"><span data-stu-id="e14ff-112">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="e14ff-113">PostMessage</span><span class="sxs-lookup"><span data-stu-id="e14ff-113">PostMessage</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
-   <span data-ttu-id="e14ff-114">Sendnotisymess</span><span class="sxs-lookup"><span data-stu-id="e14ff-114">SendNotifyMessage</span></span>
-   <span data-ttu-id="e14ff-115">Sendmessagecallback</span><span class="sxs-lookup"><span data-stu-id="e14ff-115">SendMessageCallback</span></span>
-   <span data-ttu-id="e14ff-116">Von SendMessageTimeout</span><span class="sxs-lookup"><span data-stu-id="e14ff-116">SendMessageTimeout</span></span>
-   <span data-ttu-id="e14ff-117">PostThreadMessage</span><span class="sxs-lookup"><span data-stu-id="e14ff-117">PostThreadMessage</span></span>

## <a name="related-topics"></a><span data-ttu-id="e14ff-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e14ff-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e14ff-119">Funktionen</span><span class="sxs-lookup"><span data-stu-id="e14ff-119">Functions</span></span>](mtfunctions.md)
</dt> <dt>

[<span data-ttu-id="e14ff-120">DefWindowProc</span><span class="sxs-lookup"><span data-stu-id="e14ff-120">DefWindowProc</span></span>](/windows/win32/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

 