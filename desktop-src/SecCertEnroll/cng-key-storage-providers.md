---
description: 'Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern (Key Storage Providers, kSPS).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: CNG-Schlüsselspeicher Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393402"
---
# <a name="cng-key-storage-providers"></a><span data-ttu-id="5d290-103">CNG-Schlüsselspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="5d290-103">CNG Key Storage Providers</span></span>

<span data-ttu-id="5d290-104">Im Unterschied zur Cryptography API (CryptoAPI) trennt Cryptography API: Next Generation (CNG) Kryptografieanbieter von Schlüsselspeicher Anbietern (Key Storage Providers, kSPS).</span><span class="sxs-lookup"><span data-stu-id="5d290-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers (KSPs).</span></span> <span data-ttu-id="5d290-105">KSPS können zum Erstellen, löschen, exportieren, importieren, öffnen und Speichern von Schlüsseln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d290-105">KSPs can be used to create, delete, export, import, open and store keys.</span></span> <span data-ttu-id="5d290-106">Abhängig von der Implementierung können Sie auch für die asymmetrische Verschlüsselung, geheime Vereinbarung und Signierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d290-106">Depending on implementation, they can also be used for asymmetric encryption, secret agreement, and signing.</span></span> <span data-ttu-id="5d290-107">Microsoft installiert die folgenden kSPS ab Windows Vista und Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5d290-107">Microsoft installs the following KSPs beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="5d290-108">Anbieter können andere Anbieter erstellen und installieren.</span><span class="sxs-lookup"><span data-stu-id="5d290-108">Vendors can create and install other providers.</span></span>

## <a name="microsoft-software-key-storage-provider"></a><span data-ttu-id="5d290-109">Microsoft-Software Schlüsselspeicher-Anbieter</span><span class="sxs-lookup"><span data-stu-id="5d290-109">Microsoft Software Key Storage Provider</span></span>

<span data-ttu-id="5d290-110">Unterstützt die Erstellung und Speicherung von Software Schlüsseln sowie die folgenden Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="5d290-110">Supports software key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="5d290-111">Algorithmus</span><span class="sxs-lookup"><span data-stu-id="5d290-111">Algorithm</span></span>                                          | <span data-ttu-id="5d290-112">Zweck</span><span class="sxs-lookup"><span data-stu-id="5d290-112">Purpose</span></span>                           | <span data-ttu-id="5d290-113">Schlüssellänge (Bits)</span><span class="sxs-lookup"><span data-stu-id="5d290-113">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="5d290-114">Diffie-Hellman (dh)</span><span class="sxs-lookup"><span data-stu-id="5d290-114">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="5d290-115">Geheimer Vertrag und Schlüsselaustausch</span><span class="sxs-lookup"><span data-stu-id="5d290-115">Secret agreement and key exchange</span></span> | <span data-ttu-id="5d290-116">512 bis 4096 in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="5d290-116">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="5d290-117">Digital Signature-Algorithmus (DSA)</span><span class="sxs-lookup"><span data-stu-id="5d290-117">Digital Signature Algorithm (DSA)</span></span>                  | <span data-ttu-id="5d290-118">Signaturen</span><span class="sxs-lookup"><span data-stu-id="5d290-118">Signatures</span></span>                        | <span data-ttu-id="5d290-119">512 bis 1024 in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="5d290-119">512 to 1024 in 64-bit increments</span></span>  |
| <span data-ttu-id="5d290-120">ECDH (Elliptic Curve Diffie-Hellman)</span><span class="sxs-lookup"><span data-stu-id="5d290-120">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="5d290-121">Geheimer Vertrag und Schlüsselaustausch</span><span class="sxs-lookup"><span data-stu-id="5d290-121">Secret agreement and key exchange</span></span> | <span data-ttu-id="5d290-122">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="5d290-122">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5d290-123">ECDSA (Elliptic Curve Digital Signature-Algorithmus)</span><span class="sxs-lookup"><span data-stu-id="5d290-123">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="5d290-124">Signaturen</span><span class="sxs-lookup"><span data-stu-id="5d290-124">Signatures</span></span>                        | <span data-ttu-id="5d290-125">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="5d290-125">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5d290-126">RSA</span><span class="sxs-lookup"><span data-stu-id="5d290-126">RSA</span></span>                                                | <span data-ttu-id="5d290-127">Asymmetrische Verschlüsselung und Signierung</span><span class="sxs-lookup"><span data-stu-id="5d290-127">Asymmetric encryption and signing</span></span> | <span data-ttu-id="5d290-128">512 bis 16384 in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="5d290-128">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="microsoft-smart-card-key-storage-provider"></a><span data-ttu-id="5d290-129">Microsoft-Smartcard-Schlüsselspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="5d290-129">Microsoft Smart Card Key Storage Provider</span></span>

<span data-ttu-id="5d290-130">Unterstützt die Erstellung und Speicherung von smartcardschlüsseln sowie die folgenden Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="5d290-130">Supports smart card key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="5d290-131">Algorithmus</span><span class="sxs-lookup"><span data-stu-id="5d290-131">Algorithm</span></span>                                          | <span data-ttu-id="5d290-132">Zweck</span><span class="sxs-lookup"><span data-stu-id="5d290-132">Purpose</span></span>                           | <span data-ttu-id="5d290-133">Schlüssellänge (Bits)</span><span class="sxs-lookup"><span data-stu-id="5d290-133">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="5d290-134">Diffie-Hellman (dh)</span><span class="sxs-lookup"><span data-stu-id="5d290-134">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="5d290-135">Geheimer Vertrag und Schlüsselaustausch</span><span class="sxs-lookup"><span data-stu-id="5d290-135">Secret agreement and key exchange</span></span> | <span data-ttu-id="5d290-136">512 bis 4096 in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="5d290-136">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="5d290-137">ECDH (Elliptic Curve Diffie-Hellman)</span><span class="sxs-lookup"><span data-stu-id="5d290-137">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="5d290-138">Geheimer Vertrag und Schlüsselaustausch</span><span class="sxs-lookup"><span data-stu-id="5d290-138">Secret agreement and key exchange</span></span> | <span data-ttu-id="5d290-139">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="5d290-139">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5d290-140">ECDSA (Elliptic Curve Digital Signature-Algorithmus)</span><span class="sxs-lookup"><span data-stu-id="5d290-140">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="5d290-141">Signaturen</span><span class="sxs-lookup"><span data-stu-id="5d290-141">Signatures</span></span>                        | <span data-ttu-id="5d290-142">P256, P384, P521</span><span class="sxs-lookup"><span data-stu-id="5d290-142">P256, P384, P521</span></span>                  |
| <span data-ttu-id="5d290-143">RSA</span><span class="sxs-lookup"><span data-stu-id="5d290-143">RSA</span></span>                                                | <span data-ttu-id="5d290-144">Asymmetrische Verschlüsselung und Signierung</span><span class="sxs-lookup"><span data-stu-id="5d290-144">Asymmetric encryption and signing</span></span> | <span data-ttu-id="5d290-145">512 bis 16384 in 64-Bit-Inkrementen</span><span class="sxs-lookup"><span data-stu-id="5d290-145">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5d290-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d290-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d290-147">**CNG-Algorithmusbezeichner**</span><span class="sxs-lookup"><span data-stu-id="5d290-147">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="5d290-148">CNG-Schlüsselspeicher Funktionen</span><span class="sxs-lookup"><span data-stu-id="5d290-148">CNG Key Storage Functions</span></span>](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[<span data-ttu-id="5d290-149">Grundlegendes zu Kryptografieanbietern</span><span class="sxs-lookup"><span data-stu-id="5d290-149">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
