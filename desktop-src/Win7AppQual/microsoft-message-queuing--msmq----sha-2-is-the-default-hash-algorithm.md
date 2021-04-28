---
description: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.'
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2b73e347f5d5a768780afc5d2153909c6f5a9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088098"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="cce20-103">Microsoft Message Queuing (MSMQ): SHA 2 ist der Standardhashalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="cce20-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="cce20-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="cce20-104">Affected Platforms</span></span>

 <span data-ttu-id="cce20-105">**Clients:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="cce20-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="cce20-106">**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cce20-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="cce20-107">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="cce20-107">Feature Impact</span></span>

 <span data-ttu-id="cce20-108">**Schweregrad –** Niedrig</span><span class="sxs-lookup"><span data-stu-id="cce20-108">**Severity** - Low</span></span>  
<span data-ttu-id="cce20-109">**Häufigkeit** : Niedrig</span><span class="sxs-lookup"><span data-stu-id="cce20-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="cce20-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cce20-110">Description</span></span>

<span data-ttu-id="cce20-111">In Windows 7 verwendet MSMQ SHA-2 als Standard beim Signieren einer ausgehenden Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cce20-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="cce20-112">Darüber hinaus müssen alle eingehenden Nachrichten mit SHA-2 signiert werden.</span><span class="sxs-lookup"><span data-stu-id="cce20-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="cce20-113">Sie können die Unterstützung für einen niedrigeren Verschlüsselungsalgorithmus über einen vom Administrator zugänglichen Registrierungsschlüssel aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cce20-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="cce20-114">Wirkungserz weiter</span><span class="sxs-lookup"><span data-stu-id="cce20-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="cce20-115">MSMQ unter Windows 2003 oder darunter akzeptiert keine signierten Nachrichten, die von MSMQ in Windows 7 stammen.</span><span class="sxs-lookup"><span data-stu-id="cce20-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="cce20-116">MSMQ in Windows 7 akzeptiert keine signierten Nachrichten, die von Windows 2008 oder darunter stammen.</span><span class="sxs-lookup"><span data-stu-id="cce20-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="cce20-117">Minderung</span><span class="sxs-lookup"><span data-stu-id="cce20-117">Mitigation</span></span>

<span data-ttu-id="cce20-118">Benutzer sollten ein Upgrade auf Windows 7 in Betracht ziehen, um den verstärkten Signaturalgorithmus zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="cce20-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="cce20-119">Um den nahtlosen Austausch signierter Nachrichten zwischen Windows 7 und einem beliebigen Downlevelbetriebssystem zu ermöglichen, muss der Administrator auf den MSMQ-Computern entsprechende Ausnahmen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cce20-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



