---
description: Raten Steuerung
ms.assetid: 6529859f-cfb6-4983-a489-bcc2f04e721f
title: Raten Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f484a0469d96578ca1bb7e1d661d7e2319bd8bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348485"
---
# <a name="rate-control"></a><span data-ttu-id="ff4a9-103">Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="ff4a9-103">Rate Control</span></span>

<span data-ttu-id="ff4a9-104">Die [Medien Sitzung](media-session.md) unterstützt das Ändern der Wiedergabe Rate, mit der eine Anwendung Wiedergabe Funktionen wie "schnell Forward" und "rewind" implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="ff4a9-104">The [Media Session](media-session.md) supports changing the playback rate, which an application can use to implement playback features such as fast-forward and rewind.</span></span> <span data-ttu-id="ff4a9-105">In diesem Abschnitt wird beschrieben, wie Anwendungen die Wiedergabe Rate bei der Verwendung der Medien Sitzung ändern können.</span><span class="sxs-lookup"><span data-stu-id="ff4a9-105">This section describes how applications can change the playback rate while using the Media Session.</span></span>

<span data-ttu-id="ff4a9-106">Informationen zur Unterstützung der Raten Steuerung in ihren eigenen Pipeline Komponenten finden Sie unter [Implementieren der Raten Kontrolle](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="ff4a9-106">For information about supporting rate control in your own pipeline components, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="ff4a9-107">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="ff4a9-107">This section contains the following topics.</span></span>



| <span data-ttu-id="ff4a9-108">Thema</span><span class="sxs-lookup"><span data-stu-id="ff4a9-108">Topic</span></span>                                                                                                      | <span data-ttu-id="ff4a9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff4a9-109">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="ff4a9-110">Informationen zur Raten Kontrolle</span><span class="sxs-lookup"><span data-stu-id="ff4a9-110">About Rate Control</span></span>](about-rate-control.md)                                                               | <span data-ttu-id="ff4a9-111">Bietet eine allgemeine Übersicht über die Raten Steuerung.</span><span class="sxs-lookup"><span data-stu-id="ff4a9-111">Gives a general overview of rate control.</span></span>                              |
| [<span data-ttu-id="ff4a9-112">Bestimmen der unterstützten Tarife</span><span class="sxs-lookup"><span data-stu-id="ff4a9-112">How to Determine Supported Rates</span></span>](how-to-determine-supported-rates.md)                                   | <span data-ttu-id="ff4a9-113">Hier finden Sie die schnellsten und langsamsten unterstützten Wiedergabe Raten.</span><span class="sxs-lookup"><span data-stu-id="ff4a9-113">How to find the fastest and slowest supported playback rates.</span></span>          |
| [<span data-ttu-id="ff4a9-114">Festlegen der Wiedergabe Rate für die Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="ff4a9-114">How to Set the Playback Rate on the Media Session</span></span>](how-to-set-the-playback-rate-on-the-media-session.md) | <span data-ttu-id="ff4a9-115">Ändern der Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="ff4a9-115">How to change the playback rate.</span></span>                                       |
| [<span data-ttu-id="ff4a9-116">Vorgehensweise beim Ausführen von Scrubbing</span><span class="sxs-lookup"><span data-stu-id="ff4a9-116">How to Perform Scrubbing</span></span>](how-to-perform-scrubbing.md)                                                   | <span data-ttu-id="ff4a9-117">Schrittweises Ausführen eines Video Frames.</span><span class="sxs-lookup"><span data-stu-id="ff4a9-117">How to step one video frame at a time.</span></span>                                 |
| [<span data-ttu-id="ff4a9-118">Implementieren der Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="ff4a9-118">Implementing Rate Control</span></span>](implementing-rate-control.md)                                                 | <span data-ttu-id="ff4a9-119">Unterstützung von Variablen Wiedergabe Raten in einer benutzerdefinierten Pipeline Komponente.</span><span class="sxs-lookup"><span data-stu-id="ff4a9-119">How to support variable playback rates in a custom pipeline component.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ff4a9-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff4a9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff4a9-121">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="ff4a9-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="ff4a9-122">Suchen, schnelles vorwärts und umgekehrtes spielen</span><span class="sxs-lookup"><span data-stu-id="ff4a9-122">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



