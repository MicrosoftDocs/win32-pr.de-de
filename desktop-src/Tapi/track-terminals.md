---
description: Zwei Arten von Nachverfolgung-Terminals sind für die Aufzeichnung des Terminal-und Wiedergabe trackterminals definiert, die zu gehören und vom Terminal-und Dateiwiedergabe Terminal der Datei Aufzeichnung verwaltet werden.
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Nachverfolgen von Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362384"
---
# <a name="track-terminals"></a><span data-ttu-id="4b16e-103">Nachverfolgen von Terminals</span><span class="sxs-lookup"><span data-stu-id="4b16e-103">Track Terminals</span></span>

<span data-ttu-id="4b16e-104">Es sind zwei Arten von Nachverfolgung-Terminals definiert: das Aufzeichnen des Terminal-und Wiedergabe Nachverfolgung Terminals, die zu gehören und vom Terminal Datei Aufzeichnungs Terminal und Dateiwiedergabe Terminal verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4b16e-104">Two types of track terminals are defined: Recording Track Terminal and Playback Track Terminal, which, respectively, belong to and are managed by File Recording Terminal and File Playback Terminal.</span></span>

<span data-ttu-id="4b16e-105">Alle Nachverfolgung-Terminals machen die Schnittstellen [**itfiletrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) und [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4b16e-105">All track terminals expose the [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) and [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interfaces.</span></span> <span data-ttu-id="4b16e-106">Die **itterminal** -Schnittstelle ermöglicht die Auswahl von Nachverfolgung von Terminals in Streams oder aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4b16e-106">The **ITTerminal** interface allows the selection of track terminals onto streams or calls.</span></span>

> [!Note]  
> <span data-ttu-id="4b16e-107">Nachverfolgen Terminals machen außerdem eine private Schnittstelle ( [**itmediacontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)) verfügbar, die vom MSP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4b16e-107">Track terminals also expose a private interface, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), which the MSP uses.</span></span> <span data-ttu-id="4b16e-108">Anwendungen sollten nicht versuchen, auf diese Schnittstelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="4b16e-108">Applications should not attempt to access this interface.</span></span>

 

 

 
