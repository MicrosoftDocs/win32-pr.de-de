---
description: Anbieter implementieren kryptografische Algorithmen, generieren Schlüssel, stellen Schlüsselspeicher bereit und authentifizieren Benutzer. Anbieter können in Hardware, Software oder beidem implementiert werden.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Grundlegendes zu Kryptografieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960310"
---
# <a name="understanding-cryptographic-providers"></a><span data-ttu-id="01555-104">Grundlegendes zu Kryptografieanbietern</span><span class="sxs-lookup"><span data-stu-id="01555-104">Understanding Cryptographic Providers</span></span>

<span data-ttu-id="01555-105">Das kryptografieanbieterkonzept, das in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) eingeführt wurde und etwas in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) entwickelt wurde, ist für die sichere Implementierung von Kryptografiefunktionen auf Microsoft-Betriebssystemen von zentraler Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="01555-105">The cryptographic provider concept that was introduced in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) and which evolved somewhat in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) is central to the secure implementation of cryptographic functionality on Microsoft operating systems.</span></span> <span data-ttu-id="01555-106">Diese beiden sdche wurden verwendet, um viele Anwendungen zu erstellen und werden intern von anderen sdert aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="01555-106">These two SDKs have been used to create many applications and are called internally by other SDKs.</span></span> <span data-ttu-id="01555-107">Beispielsweise basieren Active Directory Zertifikat Dienste und die Zertifikatregistrierungs-API auf CryptoAPI und CNG.</span><span class="sxs-lookup"><span data-stu-id="01555-107">For example, Active Directory Certificate Services and the Certificate Enrollment API rely on CryptoAPI and CNG.</span></span>

<span data-ttu-id="01555-108">Im Allgemeinen implementieren Anbieter Kryptografiealgorithmen, generieren Schlüssel, stellen Schlüsselspeicher bereit und authentifizieren Benutzer.</span><span class="sxs-lookup"><span data-stu-id="01555-108">In general, providers implement cryptographic algorithms, generate keys, provide key storage, and authenticate users.</span></span> <span data-ttu-id="01555-109">Anbieter können in Hardware, Software oder beidem implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="01555-109">Providers can be implemented in hardware, software, or both.</span></span> <span data-ttu-id="01555-110">Anwendungen, die mithilfe von CryptoAPI oder CNG erstellt wurden, können die von Anbietern erstellten Schlüssel nicht ändern, und Sie können die Implementierung von Kryptografiealgorithmen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="01555-110">Applications built by using CryptoAPI or CNG cannot alter the keys created by providers, and they cannot alter cryptographic algorithm implementation.</span></span> <span data-ttu-id="01555-111">Die von Microsoft erstellten verschiedenen Anbieter werden mit den Betriebssystemen verteilt.</span><span class="sxs-lookup"><span data-stu-id="01555-111">The multiple providers created by Microsoft are distributed with the operating systems.</span></span> <span data-ttu-id="01555-112">Andere Anbieter wurden von Drittanbietern erstellt und verteilt.</span><span class="sxs-lookup"><span data-stu-id="01555-112">Other providers have been created and distributed by third parties.</span></span>

<span data-ttu-id="01555-113">In den folgenden Themen werden die Unterschiede zwischen den Anbietern der kryptografieapi und den mit CNG zugeordneten Anbietern hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="01555-113">The following topics highlight the differences between providers associated with CryptoAPI and those associated with CNG.</span></span> <span data-ttu-id="01555-114">In der Regel bezieht sich diese Dokumentation auf Anbieter ohne Verweis auf das SDK, mit dem Sie verknüpft sind. die Zuordnung erfolgt nur, wenn Sie relevant ist.</span><span class="sxs-lookup"><span data-stu-id="01555-114">Typically, this documentation refers to providers without reference to the SDK with which they are associated, noting the association only when it is relevant.</span></span>

-   [<span data-ttu-id="01555-115">Kryptografiedienstanbieter von CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="01555-115">CryptoAPI Cryptographic Service Providers</span></span>](cryptoapi-cryptographic-service-providers.md)
-   [<span data-ttu-id="01555-116">CNG-kryptografiealgorithmusanbieter</span><span class="sxs-lookup"><span data-stu-id="01555-116">CNG Cryptographic Algorithm Providers</span></span>](cng-cryptographic-algorithm-providers.md)
-   [<span data-ttu-id="01555-117">CNG-Schlüsselspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="01555-117">CNG Key Storage Providers</span></span>](cng-key-storage-providers.md)
-   [<span data-ttu-id="01555-118">Auflisten installierter Anbieter</span><span class="sxs-lookup"><span data-stu-id="01555-118">Enumerating Installed Providers</span></span>](enumerating-installed-providers.md)

## <a name="related-topics"></a><span data-ttu-id="01555-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01555-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01555-120">Verwenden der Zertifikatregistrierungs-API</span><span class="sxs-lookup"><span data-stu-id="01555-120">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
