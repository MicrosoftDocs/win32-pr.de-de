---
title: Unicode-Unterstützung für allgemeine Steuerelemente
description: In diesem Thema wird beschrieben, wie Unicode für allgemeine Steuerelement Benachrichtigungen unterstützt wird.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949238"
---
# <a name="unicode-support-for-common-controls"></a><span data-ttu-id="24d04-103">Unicode-Unterstützung für allgemeine Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="24d04-103">Unicode Support for Common Controls</span></span>

<span data-ttu-id="24d04-104">In diesem Thema wird beschrieben, wie Unicode für allgemeine Steuerelement Benachrichtigungen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="24d04-104">This topic describes how to support Unicode for common control notifications.</span></span>


<span data-ttu-id="24d04-105">Bei den Versionen 5,80 und höher von comctl32.dll unterstützen allgemeine Steuerelement Benachrichtigungen sowohl ANSI-als auch Unicode-Formate auf Windows 95-Systemen oder höher.</span><span class="sxs-lookup"><span data-stu-id="24d04-105">For versions 5.80 and later of comctl32.dll, common controls notifications support both ANSI and Unicode formats on Windows 95 systems or later.</span></span> <span data-ttu-id="24d04-106">Das System bestimmt, welches Format verwendet werden soll, indem das Fenster eine [**WM \_ notifyformat**](wm-notifyformat.md) -Meldung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="24d04-106">The system determines which format to use by sending your window a [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message.</span></span> <span data-ttu-id="24d04-107">Wenn Sie ein Format angeben möchten, geben Sie NFR \_ ANSI für ANSI-Benachrichtigungen oder NFR \_ Unicode für Unicode-Benachrichtigungen zurück.</span><span class="sxs-lookup"><span data-stu-id="24d04-107">To specify a format, return NFR\_ANSI for ANSI notifications or NFR\_UNICODE for Unicode notifications.</span></span> <span data-ttu-id="24d04-108">Wenn Sie diese Meldung nicht verarbeiten, ruft das System [**iswindowunicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) auf, um das Format zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="24d04-108">If you do not handle this message, the system calls [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) to determine the format.</span></span> <span data-ttu-id="24d04-109">Da Windows 95 und Windows 98 bei diesem Funktions aufrufimmer **false** zurückgeben, werden standardmäßig ANSI-Benachrichtigungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="24d04-109">Since Windows 95 and Windows 98 always return **FALSE** to this function call, they use ANSI notifications by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24d04-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24d04-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24d04-111">Informationen zu allgemeinen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="24d04-111">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 