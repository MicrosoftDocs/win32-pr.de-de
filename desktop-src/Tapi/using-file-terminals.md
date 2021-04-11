---
description: Die Datei Terminals können auf zwei Arten verwendet werden.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Verwenden von Datei Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131925"
---
# <a name="using-file-terminals"></a><span data-ttu-id="33529-103">Verwenden von Datei Terminals</span><span class="sxs-lookup"><span data-stu-id="33529-103">Using File Terminals</span></span>

<span data-ttu-id="33529-104">Die Datei Terminals können auf zwei Arten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33529-104">The file terminals can be used in two ways.</span></span> <span data-ttu-id="33529-105">Die einfachste Methode ist die Verwendung von [**ITBasicCallControl2:: selectterminaloncallzum**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) auswählen eines Datei Terminals (Wiedergabe oder Datensatz) für ein TAPI-calltobjekt.</span><span class="sxs-lookup"><span data-stu-id="33529-105">The simplest method is to use [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) to select a file terminal (playback or record) onto a TAPI call object.</span></span> <span data-ttu-id="33529-106">In diesem Fall übernimmt TAPI das Verbinden der Audiodatenströme mit den Track-Terminals.</span><span class="sxs-lookup"><span data-stu-id="33529-106">In this case TAPI takes care of connecting the audio streams to the track terminals.</span></span>

<span data-ttu-id="33529-107">Die zweite Methode ermöglicht einer Anwendung eine präzisere Kontrolle über die Zuordnung von Audiostreams zu den nach Titeln.</span><span class="sxs-lookup"><span data-stu-id="33529-107">The second method allows an application to have finer control over the mapping of audio streams to tracks.</span></span> <span data-ttu-id="33529-108">In diesem Szenario listet die Anwendung die für den-Befehl verfügbaren Streams auf, wählt diejenigen aus, die Sie aufzeichnen möchten (oder für die Wiedergabe zu verwenden), erstellt (oder sucht nach der Wiedergabe) die entsprechenden Spuren im dateiterminal und wählt die Spuren in callstreams aus.</span><span class="sxs-lookup"><span data-stu-id="33529-108">In this scenario, the application enumerates the streams available on the call, picks the ones it wants to record (or use for playback), creates (or finds for playback) the corresponding tracks on the file terminal, and selects the tracks on call streams.</span></span>

<span data-ttu-id="33529-109">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="33529-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="33529-110">Einfache Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="33529-110">Simple Playback</span></span>](simple-playback.md)
-   [<span data-ttu-id="33529-111">Nachverfolgung gesteuerte Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="33529-111">Track-Controlled Playback</span></span>](track-controlled-playback.md)
-   [<span data-ttu-id="33529-112">Einfacher Datensatz</span><span class="sxs-lookup"><span data-stu-id="33529-112">Simple Record</span></span>](simple-record.md)
-   [<span data-ttu-id="33529-113">Nachverfolgung gesteuerter Datensatz</span><span class="sxs-lookup"><span data-stu-id="33529-113">Track-Controlled Record</span></span>](track-controlled-record.md)

 

 



