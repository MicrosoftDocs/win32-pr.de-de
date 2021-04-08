---
title: Treiberunterstützung für MCI-Befehle
description: Treiberunterstützung für MCI-Befehle
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709587"
---
# <a name="driver-support-for-mci-commands"></a><span data-ttu-id="46328-103">Treiberunterstützung für MCI-Befehle</span><span class="sxs-lookup"><span data-stu-id="46328-103">Driver Support for MCI Commands</span></span>

<span data-ttu-id="46328-104">MCI-Treiber stellen die Funktionalität für MCI-Befehle bereit.</span><span class="sxs-lookup"><span data-stu-id="46328-104">MCI drivers provide the functionality for MCI commands.</span></span> <span data-ttu-id="46328-105">Die Systemsoftware führt einige grundlegende Daten Verwaltungsaufgaben aus, aber die gesamte Multimedia-Wiedergabe,-Präsentation und-Aufzeichnung wird von den einzelnen MCI-Treibern verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="46328-105">The system software performs some basic data-management tasks, but all the multimedia playback, presentation, and recording is handled by the individual MCI drivers.</span></span>

<span data-ttu-id="46328-106">Treiber unterscheiden sich in der Unterstützung von MCI-Befehlen und Befehlsflags.</span><span class="sxs-lookup"><span data-stu-id="46328-106">Drivers vary in their support for MCI commands and command flags.</span></span> <span data-ttu-id="46328-107">Da Multimedia-Geräte vielfältige Funktionen haben können, ist MCI so konzipiert, dass einzelne Treiber die Befehls Sätze erweitern oder reduzieren können, damit Sie den Funktionen des Geräts entsprechen.</span><span class="sxs-lookup"><span data-stu-id="46328-107">Because multimedia devices can have widely different capabilities, MCI is designed to let individual drivers extend or reduce the command sets to match the capabilities of the device.</span></span> <span data-ttu-id="46328-108">Der [**Datensatz**](record.md) -Befehl ([**MCI- \_ Datensatz**](mci-record.md)) ist z. b. Teil des Befehlssatzes für MIDI-Sequencer, aber der in Windows enthaltene mciseq-Treiber unterstützt diesen Befehl nicht.</span><span class="sxs-lookup"><span data-stu-id="46328-108">For example, the [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command is part of the command set for MIDI sequencers, but the MCISEQ driver included with Windows does not support this command.</span></span> <span data-ttu-id="46328-109">Das Referenz Thema für den Datensatz-Befehl erläutert, dass Geräte des **Sequencer** -Gerätetyps den Befehl erkennen. Dies bedeutet nicht, dass alle Geräte dieses Typs den Befehl unterstützen.</span><span class="sxs-lookup"><span data-stu-id="46328-109">The reference topic for the record command explains that devices of the **sequencer** device type recognize the command; this does not mean that all devices of this type support the command.</span></span> <span data-ttu-id="46328-110">Anwendungen [**sollten den Funktionsbefehl**](capability.md) ([**MCI \_ getdevcaps**](mci-getdevcaps.md)) verwenden, um die Funktionen eines bestimmten Geräts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="46328-110">Applications should use the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) command to determine the capabilities of a particular device.</span></span>

 

 




