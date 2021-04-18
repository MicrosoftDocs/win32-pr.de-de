---
description: Die Ziffern Überwachung überwacht den-Befehl für Ziffern.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Ziffern Überwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341199"
---
# <a name="digit-monitoring"></a><span data-ttu-id="dbc8d-103">Ziffern Überwachung</span><span class="sxs-lookup"><span data-stu-id="dbc8d-103">Digit Monitoring</span></span>

<span data-ttu-id="dbc8d-104">Die Ziffern Überwachung überwacht den-Befehl für Ziffern.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-104">Digit monitoring monitors the call for digits.</span></span> <span data-ttu-id="dbc8d-105">TAPI ermöglicht, dass Ziffern gemäß zwei Methoden (Ziffern Modi) signalisiert werden:</span><span class="sxs-lookup"><span data-stu-id="dbc8d-105">TAPI allows digits to be signaled according to two methods (digit modes):</span></span>

-   <span data-ttu-id="dbc8d-106">Pulsziffern werden als Pulse oder als Dreh Sequenzen signalisiert.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-106">Pulse Digits are signaled as pulse or rotary sequences.</span></span> <span data-ttu-id="dbc8d-107">Zur Erkennung werden diese Pulse selbst als nicht mehr als Sequenzen von hörbaren Klicks angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-107">For detection, these pulses manifest themselves as nothing more than sequences of audible clicks.</span></span> <span data-ttu-id="dbc8d-108">Gültige Pulse-Ziffern sind "0" bis "9".</span><span class="sxs-lookup"><span data-stu-id="dbc8d-108">Valid pulse digits are '0' through '9'.</span></span>
-   <span data-ttu-id="dbc8d-109">DTMF-Ziffern werden als DTMF-Töne (Dual Ton Multiple Frequency) signalisiert.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-109">DTMF Digits are signaled as DTMF (Dual Tone Multiple Frequency) tones.</span></span> <span data-ttu-id="dbc8d-110">Gültige DTMF-Ziffern sind "0" bis "9", "A".</span><span class="sxs-lookup"><span data-stu-id="dbc8d-110">Valid DTMF digits are '0' through '9', 'A'.</span></span> <span data-ttu-id="dbc8d-111">"B", "C", "d", " \* " und " \# ".</span><span class="sxs-lookup"><span data-stu-id="dbc8d-111">'B', 'C', 'D', '\*', and '\#'.</span></span> <span data-ttu-id="dbc8d-112">Sowohl der anfangs-als auch der Down-Rand der DTMF-Ziffern können überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-112">Both the beginning and the down edge of DTMF digits can be monitored.</span></span>

<span data-ttu-id="dbc8d-113">Eine Anwendung kann die Ziffern Überwachung für einen angegebenen-Befehl mit [**linemonitordigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)aktivieren bzw. deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-113">An application can enable or disable digit monitoring on a specified call with [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span></span> <span data-ttu-id="dbc8d-114">Wenn die Ziffern Überwachung aktiviert ist, bewirken erkannte Ziffern, dass die Anwendung mit der [**Zeile " \_ monitordigits**](line-monitordigits.md) " benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-114">When digit monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORDIGITS**](line-monitordigits.md) message.</span></span> <span data-ttu-id="dbc8d-115">Diese Meldung enthält das Telefon handle, für das die Ziffer erkannt wurde, sowie den Ziffern-und Ziffern Modus.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-115">This message provides the call handle on which the digit was detected as well as the digit value and the digit mode.</span></span> <span data-ttu-id="dbc8d-116">Der Bereich der Ziffern Überwachung wird durch die Lebensdauer des Aufrufes gebunden.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-116">The scope of digit monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="dbc8d-117">Die Ziffern Überwachung bei einem-Rückruf wird beendet, sobald der-Rückruf die Verbindung *trennt oder in* den *Leerlauf* wechselt.</span><span class="sxs-lookup"><span data-stu-id="dbc8d-117">Digit monitoring on a call ends as soon as the call *disconnects* or goes *idle*.</span></span>

 

 



