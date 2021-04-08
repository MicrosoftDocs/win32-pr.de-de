---
title: Kontrollierter Start
description: Kontrollierter Start
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730737"
---
# <a name="measured-boot"></a><span data-ttu-id="93aa9-103">Kontrollierter Start</span><span class="sxs-lookup"><span data-stu-id="93aa9-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="93aa9-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="93aa9-104">Platforms</span></span>

 <span data-ttu-id="93aa9-105">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="93aa9-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="93aa9-106">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93aa9-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="93aa9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93aa9-107">Description</span></span>

<span data-ttu-id="93aa9-108">Da Antischadsoftware (am) bei der Erkennung von Lauf Zeit Schadsoftware besser und besser geeignet ist, sind Angreifer auch besser in der Erstellung von Rootkits, die von der Erkennung ausblenden können.</span><span class="sxs-lookup"><span data-stu-id="93aa9-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="93aa9-109">Das Erkennen von Schadsoftware, die früh im Start Zyklen gestartet wird, ist eine Herausforderung, die die meisten Anbieter sorgfältig beantworten.</span><span class="sxs-lookup"><span data-stu-id="93aa9-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="93aa9-110">In der Regel erstellen Sie System-Hacks, die vom Host Betriebssystem nicht unterstützt werden, und können dazu führen, dass der Computer in einen instabilen Zustand versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="93aa9-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="93aa9-111">Bis zu diesem Punkt hat Windows keine gute Möglichkeit bereitgestellt, diese frühen Start Bedrohungen zu erkennen und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="93aa9-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="93aa9-112">Windows 8 führt ein neues Feature mit dem Namen "gemessene Start" ein, das jede Komponente misst, von der Firmwareversion bis zu den Start Start Treibern, speichert diese Messungen im Trusted Platform Module (TPM) auf dem Computer und stellt dann ein Protokoll zur Verfügung, das Remote getestet werden kann, um den Startstatus des Clients zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="93aa9-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="93aa9-113">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="93aa9-113">Manifestation</span></span>

<span data-ttu-id="93aa9-114">Das gemessene Start Feature bietet Software mit einem vertrauenswürdigen Protokoll (gegen das Spoofing und Manipulationen) aller Start Komponenten, die vor der Software gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="93aa9-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="93aa9-115">Die Software kann das Protokoll verwenden, um zu bestimmen, ob es sich um vertrauenswürdige Komponenten handelt oder ob Sie mit Schadsoftware infiziert sind.</span><span class="sxs-lookup"><span data-stu-id="93aa9-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="93aa9-116">Die am-Software auf dem lokalen Computer kann das Protokoll zur Evaluierung an einen Remote Server senden.</span><span class="sxs-lookup"><span data-stu-id="93aa9-116">The AM software on the local machine can send the log to a remote sever for evaluation.</span></span> <span data-ttu-id="93aa9-117">Der Remote Server kann Wiederherstellungs Aktionen initiieren, indem er die Interaktion mit der Software auf dem Client oder über Out-of-Band-Mechanismen durchsetzt.</span><span class="sxs-lookup"><span data-stu-id="93aa9-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="93aa9-118">Minderung</span><span class="sxs-lookup"><span data-stu-id="93aa9-118">Mitigation</span></span>

<span data-ttu-id="93aa9-119">In Unternehmens Szenarios kann der Systemadministrator steuern, wie gemessene Startinformationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93aa9-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="93aa9-120">In Endbenutzer Szenarien (z. b. Online Banking) muss der Consumer die Verwendung des gemessenen Starts für den jeweiligen Dienst abonnieren.</span><span class="sxs-lookup"><span data-stu-id="93aa9-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="93aa9-121">Lösung</span><span class="sxs-lookup"><span data-stu-id="93aa9-121">Solution</span></span>

<span data-ttu-id="93aa9-122">Es wird ein Whitepaper vorbereitet, in dem die APIs und Funktionsaufrufe ausführlich erläutert werden, die für verschiedene gemessene Start Szenarios erfolgen müssen.</span><span class="sxs-lookup"><span data-stu-id="93aa9-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




