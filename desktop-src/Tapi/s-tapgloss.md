---
description: Die folgenden Begriffe sind nützlich, um die TAPI-Technologie zu verstehen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: S (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357114"
---
# <a name="s-telephony-api"></a><span data-ttu-id="042a4-103">S (telefonieapi)</span><span class="sxs-lookup"><span data-stu-id="042a4-103">S (Telephony API)</span></span>

<span data-ttu-id="042a4-104">[a](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="042a4-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="042a4-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="042a4-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**service provider**</span></span>
</dt> <dd>

<span data-ttu-id="042a4-106">Eine Dynamic Link Library, die die Kommunikation über ein Telefon Netzwerk über einen Satz exportierter Dienstfunktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="042a4-106">A dynamic-link library that supports communications over a telephone network through a set of exported service functions.</span></span> <span data-ttu-id="042a4-107">Der Dienstanbieter antwortet auf Telefonieanforderungen, die von der TAPI-Dynamic-Link-Bibliothek an ihn gesendet werden, indem er die Aufgaben auf niedriger Ebene ausführt, die für die Kommunikation über das Telefon Netzwerk erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="042a4-107">The service provider responds to telephony requests, sent to it by the TAPI dynamic-link library, by carrying out the low-level tasks necessary to communicate over the telephone network.</span></span> <span data-ttu-id="042a4-108">Auf diese Weise schützt der Dienstanbieter in Verbindung mit TAPI Anwendungen von den Dienst-und Technologie abhängigen Details der Telefon Netzwerkkommunikation.</span><span class="sxs-lookup"><span data-stu-id="042a4-108">In this way, the service provider, in conjunction with TAPI, shields applications from the service- and technology-dependent details of the telephone network communication.</span></span>

</dd> <dt>

<span data-ttu-id="042a4-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**unter Adressierung**</span><span class="sxs-lookup"><span data-stu-id="042a4-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span></span>
</dt> <dd>

<span data-ttu-id="042a4-110">Eine Funktion, die in ISDN-Linien zur Verfügung gestellt wird, die mehr Informationen als nur eine einzige Telefonnummer für die Wahl zulässt.</span><span class="sxs-lookup"><span data-stu-id="042a4-110">A capability provided on ISDN lines that allows more information than just a single telephone number to be used when dialing.</span></span>

</dd> <dt>

<span data-ttu-id="042a4-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Ergänzende Telefonie**</span><span class="sxs-lookup"><span data-stu-id="042a4-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Supplementary Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="042a4-112">Dienst Ebene, die erweiterte Switchfeatures wie z. b. "Hold", "Transfer" usw. bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="042a4-112">Level of service that provides advanced switch features such as hold, transfer, and so on.</span></span> <span data-ttu-id="042a4-113">Alle ergänzenden Dienste sind optional. Das heißt, der Dienstanbieter muss diese nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="042a4-113">All supplementary services are optional; that is, the service provider is not required to support them.</span></span> <span data-ttu-id="042a4-114">Weitere Informationen finden Sie [*unter unter*](b-tapgloss.md) [*stützte telefonietelefonietelefonietelefonie*](a-tapgloss.md) [](e-tapgloss.md#tapi2.extended_telephony_tapgloss)</span><span class="sxs-lookup"><span data-stu-id="042a4-114">See [*Assisted Telephony*](a-tapgloss.md), [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span></span>

</dd> <dt>

<span data-ttu-id="042a4-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**56 gewechselt**</span><span class="sxs-lookup"><span data-stu-id="042a4-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span></span>
</dt> <dd>

<span data-ttu-id="042a4-116">Ein umgeschalteter Datendienst, mit dem der Benutzer eine andere Person wählen und bei vollständigem Duplex, Digital synchronen 56 Kbit/s für den Preis eines Telefonanrufs übertragen kann.</span><span class="sxs-lookup"><span data-stu-id="042a4-116">A switched data service that lets the user dial someone else and transmit at full duplex, digital synchronous 56 Kbps for the price of a phone call.</span></span>

</dd> <dt>

<span data-ttu-id="042a4-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchrone**</span><span class="sxs-lookup"><span data-stu-id="042a4-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronous**</span></span>
</dt> <dd>

<span data-ttu-id="042a4-118">Daten Übertragungsmethode, bei der eine Konstante Zeit zwischen aufeinander folgenden Bits, Zeichen oder Ereignissen vorliegt.</span><span class="sxs-lookup"><span data-stu-id="042a4-118">Data transmission method in which there is constant time between successive bits, characters, or events.</span></span> <span data-ttu-id="042a4-119">Die zeitliche Steuerung wird durch die gemeinsame Nutzung einer einzelnen Uhr erreicht.</span><span class="sxs-lookup"><span data-stu-id="042a4-119">The timing is achieved by the sharing of a single clock.</span></span> <span data-ttu-id="042a4-120">Jedes Ende der Übertragung synchronisiert sich selbst mit der Verwendung von Uhren und Informationen, die zusammen mit den übertragenen Daten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="042a4-120">Each end of the transmission synchronizes itself with the use of clocks and information sent along with the transmitted data.</span></span> <span data-ttu-id="042a4-121">Zeichen werden nach Zeit und nicht nach Start-und Stoppbits verteilt.</span><span class="sxs-lookup"><span data-stu-id="042a4-121">Characters are spaced by time, not by start and stop bits.</span></span> <span data-ttu-id="042a4-122">Siehe [*asynchron*](a-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="042a4-122">See [*asynchronous*](a-tapgloss.md).</span></span>

</dd> </dl>

 

 



