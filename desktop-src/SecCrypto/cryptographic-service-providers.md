---
description: Wichtig diese API ist veraltet.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Kryptografiedienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393509"
---
# <a name="cryptographic-service-providers"></a><span data-ttu-id="8a7c0-103">Kryptografiedienstanbieter</span><span class="sxs-lookup"><span data-stu-id="8a7c0-103">Cryptographic Service Providers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a7c0-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-104">This API is deprecated.</span></span> <span data-ttu-id="8a7c0-105">Neue und vorhandene Software sollten mit der Verwendung von [Cryptography Next Generation-APIs beginnen.](/windows/desktop/SecCNG/cng-portal)</span><span class="sxs-lookup"><span data-stu-id="8a7c0-105">New and existing software should start using [Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal)</span></span> <span data-ttu-id="8a7c0-106">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-106">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="8a7c0-107">Ein [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) enthält Implementierungen kryptografischer Standards und Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-107">A [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) contains implementations of cryptographic standards and algorithms.</span></span> <span data-ttu-id="8a7c0-108">Ein CSP besteht mindestens aus einer DLL ( [*Dynamic Link Library*](../secgloss/d-gly.md) ), die die Funktionen in [*cryptospi*](../secgloss/c-gly.md) (einer [*Systemprogramm Schnittstelle*](../secgloss/s-gly.md)) implementiert.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-108">At a minimum, a CSP consists of a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements the functions in [*CryptoSPI*](../secgloss/c-gly.md) (a [*system program interface*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="8a7c0-109">Die meisten CSPs enthalten die Implementierung aller ihrer eigenen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-109">Most CSPs contain the implementation of all of their own functions.</span></span> <span data-ttu-id="8a7c0-110">Einige CSPs implementieren ihre Funktionen jedoch hauptsächlich in einem Windows-basierten Dienstprogramm, das vom Windows-Dienststeuerungs-Manager verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-110">Some CSPs, however, implement their functions mainly in a Windows-based service program managed by the Windows service control manager.</span></span> <span data-ttu-id="8a7c0-111">Andere implementieren Funktionen in Hardware, z. b. eine [*Smartcard*](../secgloss/s-gly.md) oder einen sicheren Coprozessor.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-111">Others implement functions in hardware, such as a [*smart card*](../secgloss/s-gly.md) or secure coprocessor.</span></span> <span data-ttu-id="8a7c0-112">Wenn ein CSP seine eigenen Funktionen nicht implementiert, fungiert die dll als Pass-Through-Schicht und ermöglicht die Kommunikation zwischen dem Betriebssystem und der eigentlichen CSP-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-112">If a CSP does not implement its own functions, the DLL acts as a pass-through layer, facilitating the communication between the operating system and the actual CSP implementation.</span></span>

<span data-ttu-id="8a7c0-113">In diesem Abschnitt werden folgende Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-113">This section includes the following topics.</span></span>



| <span data-ttu-id="8a7c0-114">Thema</span><span class="sxs-lookup"><span data-stu-id="8a7c0-114">Topic</span></span>                                                                                      | <span data-ttu-id="8a7c0-115">Inhalte</span><span class="sxs-lookup"><span data-stu-id="8a7c0-115">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a7c0-116">Typen von Kryptografieanbietern</span><span class="sxs-lookup"><span data-stu-id="8a7c0-116">Cryptographic Provider Types</span></span>](cryptographic-provider-types.md)                           | <span data-ttu-id="8a7c0-117">Kryptografieanbiettypen sind Familien von Kryptografiedienstanbietern, die Datenformate und Kryptografieprotokolle gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-117">Cryptographic provider types are families of cryptographic services providers that share data formats and cryptographic protocols.</span></span> <span data-ttu-id="8a7c0-118">Zu den Datenformaten gehören Algorithmen zum [*Auffüllen*](../secgloss/p-gly.md) von Auffüll Schemata, [*Schlüssellängen*](../secgloss/k-gly.md)und Standard Modi.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-118">Data formats include algorithms [*padding*](../secgloss/p-gly.md) schemes, [*key lengths*](../secgloss/k-gly.md), and default modes.</span></span> |
| [<span data-ttu-id="8a7c0-119">Kryptografiedienstanbieter von Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a7c0-119">Microsoft Cryptographic Service Providers</span></span>](microsoft-cryptographic-service-providers.md) | <span data-ttu-id="8a7c0-120">Ausführliche Informationen zu den derzeit von Microsoft verfügbaren CSPs.</span><span class="sxs-lookup"><span data-stu-id="8a7c0-120">Detailed information about CSPs currently available from Microsoft.</span></span>                                                                                                                                                                                                                                                                                       |



 

 

 
