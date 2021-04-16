---
description: Zeitformate für Such Befehle
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Zeitformate für Such Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530326"
---
# <a name="time-formats-for-seek-commands"></a><span data-ttu-id="24c3f-103">Zeitformate für Such Befehle</span><span class="sxs-lookup"><span data-stu-id="24c3f-103">Time Formats For Seek Commands</span></span>

<span data-ttu-id="24c3f-104">Viele der Methoden in der **imediaseeking** -Schnittstelle verfügen über Parameter, die Positionswerte Ausdrücken, wie z. b. die aktuelle Position oder die Position des Stopps.</span><span class="sxs-lookup"><span data-stu-id="24c3f-104">Many of the methods in the **IMediaSeeking** interface have parameters that express position values, such as current position or stop position.</span></span> <span data-ttu-id="24c3f-105">Standardmäßig werden diese Parameter in Einheiten von 100 Nanosekunden ausgedrückt, auch als Bezugszeit bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="24c3f-105">By default, these parameters are expressed in units of 100 nanoseconds, also called reference time.</span></span> <span data-ttu-id="24c3f-106">Jeder Filter, der suchen kann, muss das Suchen nach Verweis Zeit unterstützen.</span><span class="sxs-lookup"><span data-stu-id="24c3f-106">Any filter that can seek must support seeking by reference time.</span></span> <span data-ttu-id="24c3f-107">Einige Filter können auch andere Zeiteinheiten suchen, wie z. b. das Suchen nach einer bestimmten Frame Nummer oder das Suchen eines bestimmten Byte Offsets innerhalb eines Streams.</span><span class="sxs-lookup"><span data-stu-id="24c3f-107">Some filters can seek using other units of time as well, such as seeking to a particular frame number, or seeking to a given byte offset within a stream.</span></span> <span data-ttu-id="24c3f-108">Jede dieser Zeiteinheiten wird als Zeitformat bezeichnet und durch einen Globally Unique Identifier (GUID) definiert.</span><span class="sxs-lookup"><span data-stu-id="24c3f-108">Each of these time units is called a time format, and is defined by a globally unique identifier (GUID).</span></span> <span data-ttu-id="24c3f-109">Eine Liste der von DirectShow definierten Zeitformaten finden Sie unter [**Zeit Format-GUIDs**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="24c3f-109">For a list of the time formats that are defined by DirectShow, see [**Time Format GUIDs**](time-format-guids.md).</span></span> <span data-ttu-id="24c3f-110">Drittanbieter können auch GUIDs für benutzerdefinierte Zeitformate definieren.</span><span class="sxs-lookup"><span data-stu-id="24c3f-110">Third parties can also define GUIDs for custom time formats.</span></span>

<span data-ttu-id="24c3f-111">Um zu ermitteln, ob die derzeit im Filter Diagramm verfüg enden Filter ein bestimmtes Zeitformat unterstützen, rufen Sie die [**imediaseeking:: isformatsupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="24c3f-111">To determine whether the filters currently in the filter graph support a particular time format, call the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span> <span data-ttu-id="24c3f-112">Die Methode gibt "S OK" zurück, \_ Wenn das Format unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="24c3f-112">The method returns S\_OK if the format is supported.</span></span> <span data-ttu-id="24c3f-113">Andernfalls wird S false zurückgegeben, oder es wird \_ ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24c3f-113">Otherwise, it returns S\_FALSE or an error code.</span></span> <span data-ttu-id="24c3f-114">Wenn ein Format unterstützt wird, können Sie zu diesem Format wechseln, indem Sie die [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="24c3f-114">If a format is supported, you can switch to that format by calling the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span> <span data-ttu-id="24c3f-115">Wenn die **settimeformat** -Methode erfolgreich ist, werden nachfolgende Seek-Befehle mit dem neuen Zeitformat ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="24c3f-115">If the **SetTimeFormat** method succeeds, subsequent seek commands are expressed using the new time format.</span></span>

<span data-ttu-id="24c3f-116">Im folgenden Beispiel wird überprüft, ob das Diagramm das Suchen nach Frame Nummer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24c3f-116">The follow example checks whether the graph supports seeking by frame number.</span></span> <span data-ttu-id="24c3f-117">Wenn dies der Fall ist, wird eine Frame Nummer von 20 gesucht:</span><span class="sxs-lookup"><span data-stu-id="24c3f-117">If so, it seeks to frame number 20:</span></span>


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



<span data-ttu-id="24c3f-118">Beachten Sie, dass Zeitformate nur für Such Befehle gelten.</span><span class="sxs-lookup"><span data-stu-id="24c3f-118">Note that time formats only apply to seek commands.</span></span> <span data-ttu-id="24c3f-119">Sie wirken sich nicht auf die Wiedergabe des Diagramms oder andere Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="24c3f-119">They do not affect graph playback or other actions.</span></span>

 

 



