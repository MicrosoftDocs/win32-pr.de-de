---
description: Streamobjekte sind eine Abstraktion des Mediendaten Stroms oder von Streams, die einer-sitzungssitzung zugeordnet sind.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Streamobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363558"
---
# <a name="stream-objects"></a><span data-ttu-id="71179-103">Streamobjekte</span><span class="sxs-lookup"><span data-stu-id="71179-103">Stream Objects</span></span>

<span data-ttu-id="71179-104">Streamobjekte sind eine Abstraktion des Mediendaten Stroms oder von Streams, die einer-sitzungssitzung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="71179-104">Stream objects are an abstraction of the media stream or streams associated with a call session.</span></span> <span data-ttu-id="71179-105">Die Schnittstellen und Methoden, die auf Stream-und substreamobjekten verfügbar gemacht werden, ermöglichen einer Anwendung das Ausführen sehr ausführlicher Steuerelemente, wie z. b. das Anhalten eines Streams, das Hinzufügen neuer Medientypen zu einer Kommunikationssitzung oder das Anpassen des audiovolumens eines bestimmten Konferenzteilnehmer.</span><span class="sxs-lookup"><span data-stu-id="71179-105">The interfaces and methods exposed on stream and substream objects allow an application to exercise very detailed controls such as pausing a stream, adding new media types to a communications session, or adjusting the audio volume of a particular conference participant.</span></span>

<span data-ttu-id="71179-106">Die zwei Haupttypen von Stream sind der Stream und der substream.</span><span class="sxs-lookup"><span data-stu-id="71179-106">The two main types of stream are the stream and the substream.</span></span> <span data-ttu-id="71179-107">Die Schnittstellen und Methoden einer Standard Implementierung sind sowohl für als auch für substreaming ähnlich, das eine niedrigere Steuerungsebene zulässt.</span><span class="sxs-lookup"><span data-stu-id="71179-107">The interfaces and methods of a standard implementation are similar for both, but substreaming allowing a lower level of control.</span></span> <span data-ttu-id="71179-108">Alle Medien Dienstanbieter (MSPs) müssen die grundlegenden Stream-Steuerungs Schnittstellen implementieren, aber die Unterstützung für untergeordnete Datenströme ist optional.</span><span class="sxs-lookup"><span data-stu-id="71179-108">All media service providers (MSPs) must implement the basic stream control interfaces, but support for substreams is optional.</span></span>

<span data-ttu-id="71179-109">Außerdem implementieren einige Dienstanbieter [anbieterspezifische Schnittstellen](provider-specific-interfaces.md) für Datenströme.</span><span class="sxs-lookup"><span data-stu-id="71179-109">In addition, some service providers implement [provider-specific interfaces](provider-specific-interfaces.md) for streams.</span></span> <span data-ttu-id="71179-110">Der ipconf-MSP stellt z. b. Steuerelemente auf Teilnehmerebene bereit.</span><span class="sxs-lookup"><span data-stu-id="71179-110">For example, the IPConf MSP provides participant level controls.</span></span> <span data-ttu-id="71179-111">Eine Zusammenfassung finden Sie unter [ipconf-MSP-Schnittstellen](ipconf-msp-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="71179-111">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a summary.</span></span> <span data-ttu-id="71179-112">Weitere Schnittstellen, die implementiert werden können, finden Sie in der Dokumentation des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="71179-112">For other interfaces that might be implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="71179-113">MSP und TAPI erstellen Stream-Objekte für einen-Befehl während der anfänglichen Einrichtung einer ausgehenden oder eingehenden Sitzung.</span><span class="sxs-lookup"><span data-stu-id="71179-113">The MSP and TAPI create stream objects for a call during initial setup of an outgoing or incoming session.</span></span> <span data-ttu-id="71179-114">Die Anwendung ist dafür verantwortlich, die entsprechenden Terminals für diese Streams zu identifizieren und die Terminals auf den Streams auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="71179-114">The application is responsible for identifying appropriate terminals for these streams, and selecting the terminals onto the streams.</span></span>

<span data-ttu-id="71179-115">Beachten Sie, dass in einigen Fällen ein MSP erfordert, dass die Anwendung Datenströme vor bestimmten Sitzungs Sitzungs Vorgängen beendet oder anhält.</span><span class="sxs-lookup"><span data-stu-id="71179-115">Note that in some cases an MSP may require that the application stop or pause streams prior to certain call session operations.</span></span>

<span data-ttu-id="71179-116">Die Stream-Schnittstellen sind in der [MSPi-Referenz (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="71179-116">The stream interfaces are documented in the [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md).</span></span>

<span data-ttu-id="71179-117">Das Beispiel zum [Auswählen eines Terminal](select-a-terminal.md) Codes zeigt ein Beispiel für das Auflisten von Streams und das Auswählen von Terminals auf diesen.</span><span class="sxs-lookup"><span data-stu-id="71179-117">The [Select a Terminal](select-a-terminal.md) code example shows an example of enumerating streams and selecting terminals onto them.</span></span>

 

 



