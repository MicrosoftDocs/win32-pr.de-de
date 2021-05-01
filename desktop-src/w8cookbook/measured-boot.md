---
title: Kontrollierter Start
description: Kontrollierter Start
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314341"
---
# <a name="measured-boot"></a><span data-ttu-id="3160f-103">Kontrollierter Start</span><span class="sxs-lookup"><span data-stu-id="3160f-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="3160f-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="3160f-104">Platforms</span></span>

 <span data-ttu-id="3160f-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="3160f-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="3160f-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3160f-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="3160f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3160f-107">Description</span></span>

<span data-ttu-id="3160f-108">Da Antischadsoftware (AM) immer besser zur Erkennung von Runtime-Schadsoftware geworden ist, werden Angreifer auch besser darin, Rootkits zu erstellen, die sich vor der Erkennung verbergen können.</span><span class="sxs-lookup"><span data-stu-id="3160f-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="3160f-109">Die Erkennung von Schadsoftware, die früh im Startzyklus gestartet wird, ist eine Herausforderung, die die meisten AM-Anbieter sorgfältig bewältigen müssen.</span><span class="sxs-lookup"><span data-stu-id="3160f-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="3160f-110">In der Regel erstellen sie System-Hacks, die vom Hostbetriebssystem nicht unterstützt werden und tatsächlich dazu führen können, dass der Computer in einem instabilen Zustand platziert wird.</span><span class="sxs-lookup"><span data-stu-id="3160f-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="3160f-111">Bis zu diesem Zeitpunkt bietet Windows keine gute Möglichkeit für AM, diese Bedrohungen für den frühen Start zu erkennen und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="3160f-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="3160f-112">Windows 8 führt ein neues Feature namens Kontrollierter Start ein, das jede Komponente misst , von der Firmware bis hin zu den Starttreibern, speichert diese Messungen im Trusted Platform Module (TPM) auf dem Computer und stellt dann ein Protokoll zur Verfügung, das remote getestet werden kann, um den Startstatus des Clients zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3160f-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="3160f-113">Manifestation</span><span class="sxs-lookup"><span data-stu-id="3160f-113">Manifestation</span></span>

<span data-ttu-id="3160f-114">Das feature Kontrollierter Start stellt AM-Software ein vertrauenswürdiges Protokoll (beständig gegen Spoofing und Manipulation) aller Startkomponenten bereit, die vor am-Software gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="3160f-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="3160f-115">Am-Software kann das Protokoll verwenden, um zu bestimmen, ob Komponenten, die vor der Anwendung ausgeführt wurden, vertrauenswürdig sind oder ob sie mit Schadsoftware infiziert sind.</span><span class="sxs-lookup"><span data-stu-id="3160f-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="3160f-116">Die AM-Software auf dem lokalen Computer kann das Protokoll zur Auswertung an einen Remoteserver senden.</span><span class="sxs-lookup"><span data-stu-id="3160f-116">The AM software on the local machine can send the log to a remote server for evaluation.</span></span> <span data-ttu-id="3160f-117">Der Remoteserver kann Wartungsaktionen initiieren, indem er je nach Bedarf mit Software auf dem Client oder über Out-of-Band-Mechanismen interagiert.</span><span class="sxs-lookup"><span data-stu-id="3160f-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="3160f-118">Minderung</span><span class="sxs-lookup"><span data-stu-id="3160f-118">Mitigation</span></span>

<span data-ttu-id="3160f-119">In Unternehmensszenarien hat der Systemadministrator die Kontrolle darüber, wie Kontrollierter Start Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3160f-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="3160f-120">In Endbenutzerszenarien, z. B. Onlinebanking), muss sich der Kunde dafür entscheiden, Kontrollierter Start für den jeweiligen Dienst zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3160f-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="3160f-121">Lösung</span><span class="sxs-lookup"><span data-stu-id="3160f-121">Solution</span></span>

<span data-ttu-id="3160f-122">Es wird ein Whitepaper vorbereitet, in dem die APIs und Funktionsaufrufe ausführlich beschrieben werden, die für verschiedene Kontrollierter Start Szenarien erfolgen müssen.</span><span class="sxs-lookup"><span data-stu-id="3160f-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




