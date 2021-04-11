---
description: .
ms.assetid: 43cca5bc-6675-4f29-925e-19d3fb19ef0f
title: 'Microsoft Message Queuing (MSMQ): SHA 2 ist der Standard Hash Algorithmus.'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f0d2476133ca7939bc90effa3842c0b90482ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217413"
---
# <a name="microsoft-message-queuing-msmq---sha-2-is-the-default-hash-algorithm"></a><span data-ttu-id="caa46-103">Microsoft Message Queuing (MSMQ): SHA 2 ist der Standard Hash Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="caa46-103">Microsoft Message Queuing (MSMQ) - SHA 2 Is the Default Hash Algorithm</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="caa46-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="caa46-104">Affected Platforms</span></span>

 <span data-ttu-id="caa46-105">**Clients** -Windows XP \| Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="caa46-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="caa46-106">**Server** -Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="caa46-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="caa46-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="caa46-107">Feature Impact</span></span>

 <span data-ttu-id="caa46-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="caa46-108">**Severity** - Low</span></span>  
<span data-ttu-id="caa46-109">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="caa46-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="caa46-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="caa46-110">Description</span></span>

<span data-ttu-id="caa46-111">In Windows 7 verwendet MSMQ SHA-2 als Standard beim Signieren einer ausgehenden Nachricht.</span><span class="sxs-lookup"><span data-stu-id="caa46-111">In Windows 7, MSMQ uses SHA-2 as the default when signing an outgoing message.</span></span> <span data-ttu-id="caa46-112">Außerdem müssen alle eingehenden Nachrichten mit SHA-2 signiert werden.</span><span class="sxs-lookup"><span data-stu-id="caa46-112">Additionally, all incoming messages must be signed with SHA-2.</span></span> <span data-ttu-id="caa46-113">Sie können die Unterstützung für einen niedrigeren Verschlüsselungsalgorithmus über einen vom Administrator zugänglichen Registrierungsschlüssel aktivieren.</span><span class="sxs-lookup"><span data-stu-id="caa46-113">You can enable support for a lower encryption algorithm through an administrator-accessible registry key.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="caa46-114">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="caa46-114">Manifestation of Impact</span></span>

-   <span data-ttu-id="caa46-115">MSMQ in Windows 2003 oder unten akzeptiert keine signierten Nachrichten, die von MSMQ in Windows 7 stammen</span><span class="sxs-lookup"><span data-stu-id="caa46-115">MSMQ in Windows 2003 or below will not accept signed messages originating from MSMQ in Windows 7</span></span>
-   <span data-ttu-id="caa46-116">MSMQ in Windows 7 akzeptiert keine signierten Nachrichten, die von Windows 2008 oder niedriger stammen</span><span class="sxs-lookup"><span data-stu-id="caa46-116">MSMQ in Windows 7 will not accept signed messages originating from Windows 2008 or below</span></span>

## <a name="mitigation"></a><span data-ttu-id="caa46-117">Minderung</span><span class="sxs-lookup"><span data-stu-id="caa46-117">Mitigation</span></span>

<span data-ttu-id="caa46-118">Benutzer sollten ein Upgrade auf Windows 7 in Erwägung nehmen, um den stärkeren Signatur Algorithmus zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="caa46-118">Users should consider upgrading to Windows 7 to leverage the stronger signing algorithm.</span></span> <span data-ttu-id="caa46-119">Um einen nahtlosen signierten Nachrichtenaustausch zwischen Windows 7 und einem Betriebssystem auf Betriebssystemebene zu aktivieren, muss der Administrator auf den MSMQ-Computern entsprechende Ausnahmen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="caa46-119">To enable seamless signed message exchange between Windows 7 and any down-level operating system, the Administrator must add appropriate exceptions on the MSMQ machines.</span></span>

 

 



