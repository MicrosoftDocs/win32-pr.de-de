---
title: Verwenden des Windows-Ereignis Protokolls
description: Dieser Abschnitt enthält ausführliche Informationen zur Verwendung der Windows-Ereignisprotokoll-API zum Schreiben eines Instrumentierungs Manifests, zum Schreiben des Anbieters, der die im Manifest definierten Ereignisse bereitstellt, und zum Verarbeiten der protokollierten Ereignisse.
ms.assetid: c2855190-584b-406d-acff-5ffbf10dbb5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8aca9896eabf1f785cef590993a0e6184f70c39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101738"
---
# <a name="using-windows-event-log"></a><span data-ttu-id="c5e03-103">Verwenden des Windows-Ereignis Protokolls</span><span class="sxs-lookup"><span data-stu-id="c5e03-103">Using Windows Event Log</span></span>

<span data-ttu-id="c5e03-104">Dieser Abschnitt enthält ausführliche Informationen zur Verwendung der Windows-Ereignisprotokoll-API zum Schreiben eines Instrumentierungs Manifests, zum Schreiben des Anbieters, der die im Manifest definierten Ereignisse bereitstellt, und zum Verarbeiten der protokollierten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c5e03-104">This section contains the details on how to use the Windows Event Log API to write an instrumentation manifest, write the provider that provides the events defined in the manifest, and consume the events that are logged.</span></span>

<span data-ttu-id="c5e03-105">Einzelheiten dazu finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c5e03-105">For details, see the following topics:</span></span>

-   [<span data-ttu-id="c5e03-106">Schreiben eines Instrumentierungs Manifests</span><span class="sxs-lookup"><span data-stu-id="c5e03-106">Writing an Instrumentation Manifest</span></span>](writing-an-instrumentation-manifest.md)
-   [<span data-ttu-id="c5e03-107">Kompilieren eines Instrumentierungs Manifests</span><span class="sxs-lookup"><span data-stu-id="c5e03-107">Compiling an Instrumentation Manifest</span></span>](compiling-an-instrumentation-manifest.md)
-   [<span data-ttu-id="c5e03-108">Entwickeln eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="c5e03-108">Developing a Provider</span></span>](developing-a-provider.md)
-   [<span data-ttu-id="c5e03-109">Verarbeiten von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="c5e03-109">Consuming Events</span></span>](consuming-events.md)
-   [<span data-ttu-id="c5e03-110">Einrichten und Festlegen der Konfigurations Eigenschaften eines Kanals</span><span class="sxs-lookup"><span data-stu-id="c5e03-110">Getting and Setting a Channel's Configuration Properties</span></span>](getting-and-setting-a-channel-s-configuration-properties.md)
-   [<span data-ttu-id="c5e03-111">Die Metadaten eines Anbieters werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5e03-111">Getting a Provider's Metadata</span></span>](getting-a-provider-s-metadata-.md)
-   [<span data-ttu-id="c5e03-112">Zugreifen auf Remote Computer</span><span class="sxs-lookup"><span data-stu-id="c5e03-112">Accessing Remote Computers</span></span>](accessing-remote-computers.md)
-   [<span data-ttu-id="c5e03-113">Speichern von Ereignissen in einer Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="c5e03-113">Saving Events to a Log File</span></span>](saving-events-to-a-log-file.md)

## <a name="related-topics"></a><span data-ttu-id="c5e03-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5e03-114">Related topics</span></span>

[<span data-ttu-id="c5e03-115">Wie aktiviere ich die WPP-Ablauf Verfolgung über den Windows-Ereignisprotokoll Dienst?</span><span class="sxs-lookup"><span data-stu-id="c5e03-115">How Do I Enable WPP Tracing Through the Windows Event Log Service?</span></span>](/windows-hardware/drivers/devtest/enabling-wpp-tracing-through-windows-event-log)

[<span data-ttu-id="c5e03-116">Referenz zum Windows-Ereignisprotokoll</span><span class="sxs-lookup"><span data-stu-id="c5e03-116">Windows Event Log Reference</span></span>](windows-event-log-reference.md)