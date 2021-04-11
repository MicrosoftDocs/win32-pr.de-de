---
title: Informationen zu TSB
description: Ein-Systemdienst, der die transparente Freigabe der Trusted Platform Module (TPM)-Ressourcen ermöglicht.
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TPM-Basisdienste-TSB, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104208729"
---
# <a name="about-tbs"></a><span data-ttu-id="ff649-104">Informationen zu TSB</span><span class="sxs-lookup"><span data-stu-id="ff649-104">About TBS</span></span>

<span data-ttu-id="ff649-105">Das TPM-Basis Dienst Feature (TSB) ist ein Systemdienst, der die transparente Freigabe der Trusted Platform Module (TPM)-Ressourcen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ff649-105">The TPM Base Services (TBS) feature is a system service that allows transparent sharing of the Trusted Platform Module (TPM) resources.</span></span> <span data-ttu-id="ff649-106">Die TPM-Ressourcen werden gleichzeitig auf mehrere Anwendungen auf demselben physischen Computer verteilt, auch wenn diese Anwendungen auf unterschiedlichen virtuellen Computern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ff649-106">It simultaneously shares the TPM resources among multiple applications on the same physical machine, even if those applications run on different virtual machines.</span></span> <span data-ttu-id="ff649-107">Ab Windows 8 und Windows Server 2012 ist TSB auf allen Systemen mit einem TPM vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="ff649-107">Starting with Windows 8 and Windows Server 2012, TBS comes pre-installed on all systems with a TPM.</span></span>

<span data-ttu-id="ff649-108">Der Trusted Computing Group (TCG) definiert eine Trusted Platform Module, die Kryptografiefunktionen bereitstellt, die für die Bereitstellung von Vertrauen in der Plattform konzipiert sind</span><span class="sxs-lookup"><span data-stu-id="ff649-108">The Trusted Computing Group (TCG) defines a Trusted Platform Module that provides cryptographic functions designed to provide trust in the platform.</span></span> <span data-ttu-id="ff649-109">Da das TPM in der Hardware implementiert ist, verfügt es über begrenzte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ff649-109">Because the TPM is implemented in hardware, it has finite resources.</span></span> <span data-ttu-id="ff649-110">Das TCG definiert auch einen Software Stapel, der diese Ressourcen verwendet, um vertrauenswürdige Vorgänge für Anwendungssoftware bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ff649-110">The TCG also defines a software stack that makes use of these resources to provide trusted operations for application software.</span></span> <span data-ttu-id="ff649-111">Es wird jedoch keine Bereitstellung für die parallele Ausführung einer TSS-Implementierung mit Betriebssystem Software vorgenommen, die möglicherweise auch TPM-Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff649-111">However, no provision is made for running a TSS implementation side-by-side with operating system software that may also be using TPM resources.</span></span> <span data-ttu-id="ff649-112">Das TSB-Feature löst dieses Problem, indem jeder Software Stapel, der mit TSB kommuniziert, die Überprüfung von TPM-Ressourcen für andere Software Stapel verwendet, die möglicherweise auf dem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ff649-112">The TBS feature solves this problem by enabling each software stack that communicates with TBS to use TPM resources checking for any other software stacks that may be running on the machine.</span></span>

<span data-ttu-id="ff649-113">Die TPM-Spezifikation und die TSS-Spezifikation (TCG Software Stack) finden Sie unter [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .</span><span class="sxs-lookup"><span data-stu-id="ff649-113">The TPM specification and TCG Software Stack (TSS) specification are available at [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/).</span></span>

<span data-ttu-id="ff649-114">TSB wird als Prozess interner Dienst implementiert, der Befehle annimmt, die einen RPC-Dienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff649-114">TBS is implemented as an out-of-process service that accepts commands that use an RPC service.</span></span> <span data-ttu-id="ff649-115">Eine dynamisch verknüpfte Bibliothek stellt die Programmiersprache C dar und kommuniziert mit dem TSB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ff649-115">A dynamically linked library presents the C language interface and communicates with the TBS service.</span></span>

> [!Note]  
> <span data-ttu-id="ff649-116">Der TSB-Dienst akzeptiert nur RPC-Anforderungen vom lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="ff649-116">The TBS service only accepts RPC requests from the local machine.</span></span>

 

<span data-ttu-id="ff649-117">Die wichtigsten Ziele der TSB lauten:</span><span class="sxs-lookup"><span data-stu-id="ff649-117">The primary goals of the TBS are to:</span></span>

-   <span data-ttu-id="ff649-118">Bieten Sie eine effiziente Freigabe von eingeschränkten TPM-Ressourcen, z. b. Schlüssel Slots, Slots von Autorisierungs Sitzungen und Transport Slots.</span><span class="sxs-lookup"><span data-stu-id="ff649-118">Provide efficient sharing of limited TPM resources, such as key slots, authorization sessions slots, and transport slots.</span></span>
-   <span data-ttu-id="ff649-119">Stellen Sie einen priorisierten und synchronisierten Zugriff auf TPM-Ressourcen zwischen mehreren Instanzen von TPM-Software Stapeln bereit.</span><span class="sxs-lookup"><span data-stu-id="ff649-119">Provide prioritized and synchronized access to TPM resources between multiple instances of TPM software stacks.</span></span>
-   <span data-ttu-id="ff649-120">Sorgen Sie für eine angemessene Verwaltung von TPM-Ressourcen in den Energiezuständen.</span><span class="sxs-lookup"><span data-stu-id="ff649-120">Provide appropriate management of TPM resources across power states.</span></span>
-   <span data-ttu-id="ff649-121">Verhindern Sie, dass TPM-Software Stapel auf TPM-Befehle zugreifen, die aufgrund von Platt Form Einschränkungen oder administrativen Anforderungen eingeschränkt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="ff649-121">Prevent TPM software stacks from accessing TPM commands that should be restricted, either because of platform limitations or administrative requirements.</span></span>

<span data-ttu-id="ff649-122">Die folgende Abbildung zeigt die Beziehung zwischen den TSB und dem TPM.</span><span class="sxs-lookup"><span data-stu-id="ff649-122">The following illustration shows the relationship of the TBS to the TPM.</span></span>

![Beziehung der TSB im Benutzermodus mit dem TPM im Kernel Modus](images/tbs-block-diagram-as11601.png)

 

 




