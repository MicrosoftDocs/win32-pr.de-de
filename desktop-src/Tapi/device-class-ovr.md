---
description: Geräteklassen vereinfachen die Entwicklung, da Programmierer Geräte, die ähnliche Eigenschaften haben, auf ähnliche Weise behandeln können.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Geräteklasse (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959719"
---
# <a name="device-class"></a><span data-ttu-id="9ee71-103">Geräteklasse</span><span class="sxs-lookup"><span data-stu-id="9ee71-103">Device Class</span></span>

<span data-ttu-id="9ee71-104">Geräteklassen vereinfachen die Entwicklung, da Programmierer Geräte, die ähnliche Eigenschaften haben, auf ähnliche Weise behandeln können.</span><span class="sxs-lookup"><span data-stu-id="9ee71-104">Device classes simplify development by letting programmers treat devices that have similar properties in a similar manner.</span></span> <span data-ttu-id="9ee71-105">Beispielsweise verfügt ein digitales Telefon in einem Büro in der Regel über mehr Funktionen als ein Standard-Mobiltelefon in einem Zuhause, beide reagieren aber auf die gleiche Weise auf einen grundlegenden Satz von Funktionen, und beide gehören zu einer Mobiltelefon-Geräteklasse.</span><span class="sxs-lookup"><span data-stu-id="9ee71-105">For example, a digital phone in an office typically has more capabilities than a standard handset in a home, but both respond in much the same way to a basic set of functions, and both belong to a phone device class.</span></span> <span data-ttu-id="9ee71-106">Geräteklassen helfen, TAPI erweiterbar zu machen, indem Sie ein Framework bereitstellen, von dem neue Geräte klassifiziert und unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9ee71-106">Device classes help make TAPI extensible by providing a framework from which to classify and support new equipment.</span></span>

<span data-ttu-id="9ee71-107">Siehe [TAPI-Geräteklassen](./tapi-device-classes.md) für Klassen, die TAPI vordefiniert haben.</span><span class="sxs-lookup"><span data-stu-id="9ee71-107">See [TAPI Device Classes](./tapi-device-classes.md) for classes that TAPI has predefined.</span></span> <span data-ttu-id="9ee71-108">Ein Dienstanbieter kann zusätzliche Geräteklassen für die von ihm unterstützten Geräte implementieren und definieren.</span><span class="sxs-lookup"><span data-stu-id="9ee71-108">A service provider may implement and define additional device classes for the equipment it supports.</span></span> <span data-ttu-id="9ee71-109">Eine Anwendung muss nie wissen, welcher Dienstanbieter das Gerät steuert, aber möglicherweise Informationen zur Steuerung neuer Geräteklassen benötigt.</span><span class="sxs-lookup"><span data-stu-id="9ee71-109">An application never needs to know which service provider controls which device, but may require information on the control of new device classes.</span></span>

<span data-ttu-id="9ee71-110">Ein Dienstanbieter implementiert eine Geräteklasse durch Zuordnung von Anforderungen zu tatsächlichen Geräte Befehlen.</span><span class="sxs-lookup"><span data-stu-id="9ee71-110">A service provider implements a device class by mapping requests into actual device commands.</span></span> <span data-ttu-id="9ee71-111">Wenn z. b. der Dienstanbieter für ein Hayes-kompatibles Modem einen Befehl empfängt, der durch TAPISVR an einen-Befehl übermittelt wird, sendet er klassische at-Befehle an das Modem.</span><span class="sxs-lookup"><span data-stu-id="9ee71-111">For example, when the service provider for a Hayes-compatible modem receives a command passed through TAPISVR to make a call, it sends classic AT commands to the modem.</span></span>

<span data-ttu-id="9ee71-112">Die Dienstanbieter Schnittstelle kann einer Vielzahl von Umgebungen zugeordnet werden, einschließlich derjenigen, die nicht üblicherweise als zu Telefonie gehörend betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="9ee71-112">The service provider interface can be mapped to a wide range of environments, including those not traditionally thought of as belonging to telephony.</span></span> <span data-ttu-id="9ee71-113">Ein Beispiel hierfür sind multimediakkonferenzen über ein IP-basiertes Netzwerk, z. b. das Internet.</span><span class="sxs-lookup"><span data-stu-id="9ee71-113">An example is multimedia conferencing over an IP-based network such as the Internet.</span></span>

<span data-ttu-id="9ee71-114">Anwendungsentwickler sollten das vorhanden sein anderer Anwendungen berücksichtigen, die möglicherweise Telefoniedienste gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="9ee71-114">Application developers should keep in mind the existence of other applications that may share telephony services.</span></span>

 

 
