---
description: Das folgende Material ist nur gültig, wenn Digest als SASL-Mechanismus verwendet wird. Chiffren und Verschlüsselung sind nicht für die HTTP-Authentifizierung mit Microsoft Digest verfügbar.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215359"
---
# <a name="ciphers"></a><span data-ttu-id="01f5b-104">Ciphers</span><span class="sxs-lookup"><span data-stu-id="01f5b-104">Ciphers</span></span>

<span data-ttu-id="01f5b-105">Das folgende Material ist nur gültig, wenn Digest als SASL-Mechanismus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01f5b-105">The following material is valid only when Digest is used as a SASL mechanism.</span></span> <span data-ttu-id="01f5b-106">Chiffren und Verschlüsselung sind nicht für die HTTP-Authentifizierung mit Microsoft Digest verfügbar.</span><span class="sxs-lookup"><span data-stu-id="01f5b-106">Ciphers and encryption are not available for HTTP authentication using Microsoft Digest.</span></span>

<span data-ttu-id="01f5b-107">Die Chiffre Direktive der Digest SASL Challenge enthält eine Liste der Chiffren, die von einem Server unterstützt werden, für den vertrauliche Kommunikation erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="01f5b-107">A Digest SASL challenge's cipher directive contains a list of the ciphers supported by a server that requires confidential communications.</span></span> <span data-ttu-id="01f5b-108">Die Chiffre Direktive kann nur eingeschlossen werden, wenn die QoP-Direktive auf "auth-conf" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="01f5b-108">The cipher directive can only be included if the qop directive is set to "auth-conf".</span></span> <span data-ttu-id="01f5b-109">Die Chiffren, die von Microsoft Digest erkannt werden, sind in der folgenden Tabelle aufgeführt, von der stärksten zum schwächsten.</span><span class="sxs-lookup"><span data-stu-id="01f5b-109">The ciphers recognized by Microsoft Digest are listed in the following table, in order from strongest to weakest.</span></span>



| <span data-ttu-id="01f5b-110">Chiffre Wert</span><span class="sxs-lookup"><span data-stu-id="01f5b-110">Cipher value</span></span> | <span data-ttu-id="01f5b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01f5b-111">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f5b-112">RC4</span><span class="sxs-lookup"><span data-stu-id="01f5b-112">"rc4"</span></span>        | <span data-ttu-id="01f5b-113">Die RC4-Chiffre mit einem 128-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="01f5b-113">The RC4 cipher with a 128-bit key.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="01f5b-114">3DES</span><span class="sxs-lookup"><span data-stu-id="01f5b-114">"3des"</span></span>       | <span data-ttu-id="01f5b-115">Das [*dreifache*](/windows/desktop/SecGloss/t-gly) der-Verschlüsselung im [*CBC*](/windows/desktop/SecGloss/c-gly) -Modus mit "Ede" mit dem gleichen Schlüssel für jede E-Phase (zwei Schlüssel Modus).</span><span class="sxs-lookup"><span data-stu-id="01f5b-115">The [*triple DES*](/windows/desktop/SecGloss/t-gly) cipher in [*CBC*](/windows/desktop/SecGloss/c-gly) mode with EDE with the same key for each E stage (two keys mode).</span></span> <span data-ttu-id="01f5b-116">Die Gesamtlänge des Schlüssels beträgt 112 Bits.</span><span class="sxs-lookup"><span data-stu-id="01f5b-116">Total key length is 112 bits.</span></span> |
| <span data-ttu-id="01f5b-117">"RC4-56"</span><span class="sxs-lookup"><span data-stu-id="01f5b-117">"rc4-56"</span></span>     | <span data-ttu-id="01f5b-118">Die RC4-Chiffre mit einem 56-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="01f5b-118">The RC4 cipher with a 56-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="01f5b-119">"RC4-40"</span><span class="sxs-lookup"><span data-stu-id="01f5b-119">"rc4-40"</span></span>     | <span data-ttu-id="01f5b-120">Die RC4-Chiffre mit einem 40-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="01f5b-120">The RC4 cipher with a 40-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="01f5b-121">des</span><span class="sxs-lookup"><span data-stu-id="01f5b-121">"des"</span></span>        | <span data-ttu-id="01f5b-122">Der [*Verschlüsselungs Standard (Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) , des) in [*Verschlüsselungs Block Verkettung*](/windows/desktop/SecGloss/c-gly) (CBC)-Modus mit einem 56-Bit-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="01f5b-122">The [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) (DES) cipher in [*cipher block chaining*](/windows/desktop/SecGloss/c-gly) (CBC) mode with a 56-bit key.</span></span> |



 

<span data-ttu-id="01f5b-123">Wenn eine Serveranwendung Vertraulichkeit (QoP = "auth-conf") anfordert Microsoft Digest generiert eine Herausforderung, die dem Client alle auf dem Server installierten Chiffren bietet und von Digest unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="01f5b-123">When a server application requests confidentiality (qop="auth-conf") Microsoft Digest will generate a challenge that offers the client all of the ciphers installed on the server and supported by Digest.</span></span> <span data-ttu-id="01f5b-124">Der digestclient wählt die stärkste verfügbare Chiffre aus.</span><span class="sxs-lookup"><span data-stu-id="01f5b-124">The Digest client will select the strongest available cipher.</span></span> <span data-ttu-id="01f5b-125">Ausführliche Informationen zum Angeben der Vertraulichkeit finden Sie unter [Erstellen der Digest-Challenge](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="01f5b-125">For details on specifying confidentiality, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 
