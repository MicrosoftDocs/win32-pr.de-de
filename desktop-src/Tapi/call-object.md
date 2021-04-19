---
description: Das Aufruf Objekt stellt eine adressieren-Verbindung zwischen der lokalen Adresse und mindestens einer anderen Adresse dar.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Calltobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363851"
---
# <a name="call-object"></a><span data-ttu-id="64ea5-103">Calltobjekt</span><span class="sxs-lookup"><span data-stu-id="64ea5-103">Call Object</span></span>

<span data-ttu-id="64ea5-104">Das "Callcenter"-Objekt stellt die Verbindung einer Adresse zwischen der lokalen Adresse und einer oder mehreren anderen Adressen dar.</span><span class="sxs-lookup"><span data-stu-id="64ea5-104">The Call object represents an address's connection between the local address and one or more other addresses.</span></span> <span data-ttu-id="64ea5-105">Alle callensteuerelemente werden über das-Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="64ea5-105">All call control is done through the Call object.</span></span> <span data-ttu-id="64ea5-106">[**Itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) und [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) sind die am häufigsten verwendeten Schnittstellen des Aufruf Objekts.</span><span class="sxs-lookup"><span data-stu-id="64ea5-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) are the most frequently used interfaces on the call object.</span></span> <span data-ttu-id="64ea5-107">Diese Schnittstellen implementieren eine Reihe von Vorgängen und Abfragen, z. b. das Abrufen von Schnittstellen Zeigern für Medienströme oder das Abrufen der Aufruferkennung</span><span class="sxs-lookup"><span data-stu-id="64ea5-107">These interfaces implement a variety of operations and queries, such as acquiring interface pointers for media streams or getting the caller ID.</span></span> <span data-ttu-id="64ea5-108">Weitere Informationen zu [Sitzungs Vorgängen](session-operations-ovr.md) und [Sitzungsinformationen](session-information-ovr.md) finden Sie in den Abschnitten Haupt Übersicht über die von TAPI unterstützten Überprüfungen.</span><span class="sxs-lookup"><span data-stu-id="64ea5-108">See the main overview sections on [Session Operations](session-operations-ovr.md) and [Session Information](session-information-ovr.md) for reviews of those supported by TAPI.</span></span>

<span data-ttu-id="64ea5-109">Ein Medien Dienstanbieter kann [anbieterspezifische Schnittstellen](provider-specific-interfaces.md)implementieren, die auf einem calltobjekt von TAPI aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="64ea5-109">A media service provider can implement [provider-specific interfaces](provider-specific-interfaces.md), which are aggregated on a call object by TAPI.</span></span> <span data-ttu-id="64ea5-110">Ausführliche Informationen zu den von einem Anbieter implementierten Informationen finden Sie in der Dokumentation des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="64ea5-110">For detailed information on what a provider has implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="64ea5-111">Die Beispiele zum Ausführen [eines aufrufscodes](make-a-call.md) und zum [empfangen eines Aufrufcodes](receive-a-call.md) veranschaulichen einige Abbildungen der Verwendung eines calltobjekt.</span><span class="sxs-lookup"><span data-stu-id="64ea5-111">The [Make a Call](make-a-call.md) and [Receive a Call](receive-a-call.md) code examples show some illustrations of using a Call object.</span></span>

<span data-ttu-id="64ea5-112">Eine Liste aller dem-Objekt zugeordneten Schnittstellen finden Sie unter [Callcenter-Schnittstellen](call-object-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="64ea5-112">See [Call Object Interfaces](call-object-interfaces.md) for a list of all interfaces associated with the Call object.</span></span>

 

 



