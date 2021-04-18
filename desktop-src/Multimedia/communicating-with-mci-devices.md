---
title: Kommunikation mit MCI-Geräten
description: Kommunikation mit MCI-Geräten
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- Mciwndsendstring-Makro
- mciSendString-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341296"
---
# <a name="communicating-with-mci-devices"></a><span data-ttu-id="503b9-105">Kommunikation mit MCI-Geräten</span><span class="sxs-lookup"><span data-stu-id="503b9-105">Communicating with MCI Devices</span></span>

<span data-ttu-id="503b9-106">Der Treiber der einzelnen MCI-Geräte verwaltet eine Liste der aktuellen Einstellungen und Funktionen, sodass eine genaue Antwort ausgegeben werden kann, wenn nach Informationen abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="503b9-106">The driver of each MCI device maintains a list of its current settings and capabilities, so it can issue an accurate response when it is queried for information.</span></span>

<span data-ttu-id="503b9-107">Wenn Sie mit einem MCI-Gerät kommunizieren möchten, können Sie mciwnd-Makros und-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="503b9-107">When you want to communicate with an MCI device, you can use MCIWnd macros and functions.</span></span> <span data-ttu-id="503b9-108">Viele der gängigsten MCI-Befehle und-Abfragen werden als Makros definiert.</span><span class="sxs-lookup"><span data-stu-id="503b9-108">Many of the most common MCI commands and queries are defined as macros.</span></span> <span data-ttu-id="503b9-109">Wenn der Task, den Sie ausführen möchten, jedoch nicht als Funktion oder Makro verfügbar ist, können Sie MCI-Befehle direkt an den Gerätetreiber senden, indem Sie das [**mciwndsendstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) -Makro oder entweder das Nachrichten Formular oder die Zeichen folgen Form der MCI-Befehle verwenden.</span><span class="sxs-lookup"><span data-stu-id="503b9-109">However, if the task you want to perform is unavailable as a function or macro, you can send MCI commands directly to the device driver by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro or by using either the message form or string form of the MCI commands.</span></span> <span data-ttu-id="503b9-110">Die Verwendung des **mciwndsendstring** -Makros entspricht der Verwendung der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion wie folgt:</span><span class="sxs-lookup"><span data-stu-id="503b9-110">Using the **MCIWndSendString** macro is equivalent to using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function as follows:</span></span>


```C++
mciSendString(sz, Null, 0, Null) 
```



<span data-ttu-id="503b9-111">Die Parameter von [**mciwndsendstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) schließen nur das Fenster Handle und die Zeichen folgen Form des Befehls ein.</span><span class="sxs-lookup"><span data-stu-id="503b9-111">The parameters of [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) include only the window handle and the string form of the command.</span></span> <span data-ttu-id="503b9-112">Verwenden Sie zum Abrufen der Informationen, die von einem Zeichen folgen Befehl zurückgegeben werden, das [**mciwndreturnstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) -Makro.</span><span class="sxs-lookup"><span data-stu-id="503b9-112">To retrieve the information returned by a string command, use the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>

<span data-ttu-id="503b9-113">Weitere Informationen zu MCI finden Sie unter [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="503b9-113">For more information about MCI, see [MCI](mci.md).</span></span>

> [!Note]  
> <span data-ttu-id="503b9-114">Sie müssen den Gerätealias aus dem MCI-Befehl ausschließen, wenn Sie **mciwndsendstring** verwenden.</span><span class="sxs-lookup"><span data-stu-id="503b9-114">You must exclude the device alias from the MCI command when you use **MCIWndSendString**.</span></span> <span data-ttu-id="503b9-115">Die mciwnd-Bibliothek fügt diesen Alias hinzu, wenn der Befehl an das MCI-Gerät gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="503b9-115">The MCIWnd library adds this alias when it sends the command to the MCI device.</span></span>

 

 

 