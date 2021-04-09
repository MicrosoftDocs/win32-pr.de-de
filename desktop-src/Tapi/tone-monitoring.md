---
description: Die Tone-Überwachung überwacht den Mediendaten Strom eines Aufrufes für bestimmte Töne.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Tone-Überwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042372"
---
# <a name="tone-monitoring"></a><span data-ttu-id="c56c3-103">Tone-Überwachung</span><span class="sxs-lookup"><span data-stu-id="c56c3-103">Tone Monitoring</span></span>

<span data-ttu-id="c56c3-104">Die Tone-Überwachung überwacht den Mediendaten Strom eines Aufrufes für bestimmte Töne.</span><span class="sxs-lookup"><span data-stu-id="c56c3-104">Tone monitoring monitors the media stream of a call for specified tones.</span></span> <span data-ttu-id="c56c3-105">Ein Ton wird durch seine Komponenten Frequenzen und den Rhythmus beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c56c3-105">A tone is described by its component frequencies and cadence.</span></span> <span data-ttu-id="c56c3-106">Durch eine Implementierung der API können mehrere verschiedene Töne gleichzeitig überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="c56c3-106">An implementation of the API may allow several different tones to be monitored simultaneously.</span></span> <span data-ttu-id="c56c3-107">Eine Anwendung kann jeden Ton markieren, um die verschiedenen Töne zu unterscheiden, für die er eine Erkennung anfordert.</span><span class="sxs-lookup"><span data-stu-id="c56c3-107">An application can tag each tone to be able to distinguish the different tones for which it requests detection.</span></span>

<span data-ttu-id="c56c3-108">Eine Anwendung kann die Überwachung von Tone für einen angegebenen-Befehl mit [**linemonitortones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)aktivieren bzw. deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c56c3-108">An application can enable or disable tone monitoring on a specified call with [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span></span> <span data-ttu-id="c56c3-109">Mit dieser Funktion gibt die Anwendung an, welche Töne bei einem angegebenen-Befehl erkannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c56c3-109">With this function, the application indicates which tones to detect on a specified call.</span></span> <span data-ttu-id="c56c3-110">Wenn die Tone-Überwachung aktiviert ist, bewirken erkannte Ziffern, dass die Anwendung mit der [**Zeile \_ monitortone**](line-monitortone.md) -Nachricht benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="c56c3-110">When tone monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORTONE**](line-monitortone.md) message.</span></span> <span data-ttu-id="c56c3-111">Diese Meldung enthält das Telefon handle, für das der Ton erkannt wurde, sowie das Tag der Anwendung für den Ton.</span><span class="sxs-lookup"><span data-stu-id="c56c3-111">This message provides the call handle on which the tone was detected as well as the application's tag for the tone.</span></span>

<span data-ttu-id="c56c3-112">Der Bereich der Tabellen Überwachung wird durch die Lebensdauer des Aufrufes gebunden.</span><span class="sxs-lookup"><span data-stu-id="c56c3-112">The scope of tone monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="c56c3-113">Die Tone-Überwachung bei einem-Rückruf endet, sobald der-Rückruf die Verbindung *trennt oder in* den *Leerlauf* wechselt.</span><span class="sxs-lookup"><span data-stu-id="c56c3-113">Tone monitoring on a call ends as soon the call *disconnects* or goes *idle*.</span></span>

> [!Note]  
> <span data-ttu-id="c56c3-114">Für die Überwachung von Tönen, Ziffern oder Medientypen ist häufig die Verwendung von Ressourcen erforderlich, von denen der Dienstanbieter nur einen begrenzten Betrag aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="c56c3-114">The monitoring of tones, digits, or media types often requires the use of resources of which the service provider can only have a finite amount.</span></span> <span data-ttu-id="c56c3-115">Eine Anforderung für die Überwachung kann zurückgewiesen werden, wenn keine Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c56c3-115">A request for monitoring can be rejected if resources are not available.</span></span> <span data-ttu-id="c56c3-116">Aus demselben Grund sollte eine Anwendung jede unnötige Überwachung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c56c3-116">For the same reason, an application should disable any unnecessary monitoring.</span></span>

 

 

 



