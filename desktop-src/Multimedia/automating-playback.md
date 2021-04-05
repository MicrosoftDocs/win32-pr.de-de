---
title: Automatisieren der Wiedergabe
description: Automatisieren der Wiedergabe
ms.assetid: 3aa05a54-58d7-4d14-93ee-459aa860b20e
keywords:
- Mciwndcreate-Makro
- Mciwndplay-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6097d38b3d468b6de68ee7e11f98f530aff00d2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714075"
---
# <a name="automating-playback"></a><span data-ttu-id="e62cb-105">Automatisieren der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="e62cb-105">Automating Playback</span></span>

<span data-ttu-id="e62cb-106">Sie können die Wiedergabe in der Anwendung automatisieren, indem Sie [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) und das Makro mciwndplay zusammen mit dem [**mciwnddestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) -Makro oder dem mciwndclose-Makro verwenden. [](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) [](/windows/desktop/api/Vfw/nf-vfw-mciwndclose)</span><span class="sxs-lookup"><span data-stu-id="e62cb-106">You can automate playback in your application by using [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) and the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, along with either the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="e62cb-107">Um die Wiedergabe zu automatisieren, geben Sie die Stile mciwndf \_ noplaybar und mciwndf \_ notifymode im Parameter \**mciwndcreate \* \* \* dwstyle* an.</span><span class="sxs-lookup"><span data-stu-id="e62cb-107">To automate playback, specify the MCIWNDF\_NOPLAYBAR and MCIWNDF\_NOTIFYMODE styles in the \**MCIWndCreate\*\*\*dwStyle* parameter.</span></span> <span data-ttu-id="e62cb-108">Geben Sie den mciwndf \_ -noplaybar-Stil zum Ausblenden der Symbolleiste und den mciwndf- \_ Stil "notifymode" an, um eine entsprechende Benachrichtigungs Meldung auszugeben, wenn das Gerät beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e62cb-108">Specify the MCIWNDF\_NOPLAYBAR style to hide the toolbar, and the MCIWNDF\_NOTIFYMODE style to issue an appropriate notification message when the device stops playing.</span></span>

<span data-ttu-id="e62cb-109">Sie können das in **mciwndcreate** angegebene Gerät oder die Datei mit **mciwndplay** wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="e62cb-109">You can play the device or file specified in **MCIWndCreate** by using **MCIWndPlay**.</span></span> <span data-ttu-id="e62cb-110">Das mciwndplay-Makro beginnt mit der Wiedergabe des Inhalts von der aktuellen Wiedergabe Position bis zum Ende.</span><span class="sxs-lookup"><span data-stu-id="e62cb-110">The MCIWndPlay macro starts playing the content from its current playback position and continues to its end.</span></span>

<span data-ttu-id="e62cb-111">Sie können ein mciwnd-Fenster mit dem [**mciwnddestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) -oder [**mciwndclose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) -Makro zerstören oder schließen.</span><span class="sxs-lookup"><span data-stu-id="e62cb-111">You can destroy or close an MCIWnd window by using the [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy) or [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span> <span data-ttu-id="e62cb-112">Das **mciwnddestroy** -Makro schließt das Gerät oder die Datei und zerstört das mciwnd-Fenster, indem das Handle ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="e62cb-112">The **MCIWndDestroy** macro closes the device or file and destroys the MCIWnd window by invalidating its handle.</span></span> <span data-ttu-id="e62cb-113">Wenn die Anwendung das mciwnd-Fenster wieder verwenden kann, verwenden Sie **mciwndclose** , um das Gerät zu schließen, ohne das Fenster zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="e62cb-113">If your application can reuse the MCIWnd window, use **MCIWndClose** to close the device without destroying the window.</span></span>

<span data-ttu-id="e62cb-114">Die Anwendung kann erkennen, wenn das Gerät beendet wird und das Fenster automatisch schließt.</span><span class="sxs-lookup"><span data-stu-id="e62cb-114">Your application can detect when the device stops playing and automatically close the window.</span></span> <span data-ttu-id="e62cb-115">Geben Sie hierzu den mciwndf- \_ notifymode-Stil für den *dwstyle* -Parameter von [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)an.</span><span class="sxs-lookup"><span data-stu-id="e62cb-115">To do this, specify the MCIWNDF\_NOTIFYMODE style for the *dwStyle* parameter of [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span> <span data-ttu-id="e62cb-116">Dies bewirkt, dass das Gerät immer dann eine [**mciwndm- \_ Benachrichtigung**](mciwndm-notifymode.md) sendet, wenn der Modus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e62cb-116">This causes the device to send a [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message whenever it changes modes.</span></span> <span data-ttu-id="e62cb-117">Ihre Anwendung kann diese Nachricht abfangen, um zu bestimmen, ob das Gerät beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e62cb-117">Your application can trap this message to determine whether the device has stopped playing.</span></span> <span data-ttu-id="e62cb-118">Wenn die Wiedergabe des Geräts beendet wird, schließt die Anwendung das Fenster.</span><span class="sxs-lookup"><span data-stu-id="e62cb-118">When the device stops playing, the application closes the window.</span></span>

 

 




