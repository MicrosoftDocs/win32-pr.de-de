---
description: Erläutert die kryptoapi-Systemarchitektur.
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: Kryptoapi-System Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d5dcf1756c9b581d75d4e52d57fbce089976a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343139"
---
# <a name="cryptoapi-system-architecture"></a><span data-ttu-id="00cc0-103">Kryptoapi-System Architektur</span><span class="sxs-lookup"><span data-stu-id="00cc0-103">CryptoAPI System Architecture</span></span>

<span data-ttu-id="00cc0-104">Die kryptoapi-Systemarchitektur besteht aus fünf Haupt Funktionsbereichen:</span><span class="sxs-lookup"><span data-stu-id="00cc0-104">The CryptoAPI system architecture is composed of five major functional areas:</span></span>

-   [<span data-ttu-id="00cc0-105">Grundlegende Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-105">Base Cryptographic Functions</span></span>](#base-cryptographic-functions)
-   [<span data-ttu-id="00cc0-106">Zertifikatcodieren/Decodieren von Funktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-106">Certificate Encode/Decode Functions</span></span>](#certificate-encodedecode-functions)
-   [<span data-ttu-id="00cc0-107">Zertifikat Speicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-107">Certificate Store Functions</span></span>](#certificate-store-functions)
-   [<span data-ttu-id="00cc0-108">Vereinfachte Nachrichten Funktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-108">Simplified Message Functions</span></span>](#simplified-message-functions)
-   [<span data-ttu-id="00cc0-109">Nachrichten Funktionen auf niedriger Ebene</span><span class="sxs-lookup"><span data-stu-id="00cc0-109">Low-level Message Functions</span></span>](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a><span data-ttu-id="00cc0-110">Grundlegende Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-110">Base Cryptographic Functions</span></span>

-   <span data-ttu-id="00cc0-111">*Kontextfunktionen* , die zum Herstellen einer Verbindung mit einem CSP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-111">*Context functions* used to connect to a CSP.</span></span> <span data-ttu-id="00cc0-112">Mit diesen Funktionen können Anwendungen einen bestimmten CSP nach Namen auswählen oder einen bestimmten CSP auswählen, der eine erforderliche Funktionsklasse bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="00cc0-112">These functions enable applications to choose a specific CSP by name or to choose a specific CSP that can provide a needed class of functionality.</span></span>
-   <span data-ttu-id="00cc0-113">[*Schlüssel Generierungs Funktionen*](../secgloss/k-gly.md) , die zum Generieren und Speichern von [*kryptografischen Schlüsseln*](../secgloss/c-gly.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-113">[*Key generation functions*](../secgloss/k-gly.md) used to generate and store [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="00cc0-114">Vollständige Unterstützung für das Ändern von [*Verkettungs Modi*](../secgloss/c-gly.md), [*Initialisierungs Vektoren*](../secgloss/i-gly.md)und anderen Verschlüsselungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="00cc0-114">Full support is included for changing [*chaining modes*](../secgloss/c-gly.md), [*initialization vectors*](../secgloss/i-gly.md), and other encryption features.</span></span> <span data-ttu-id="00cc0-115">Weitere Informationen finden Sie unter [Schlüsselgenerierung und Exchange-Funktionen](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-115">For more information, see [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>
-   <span data-ttu-id="00cc0-116">*Schlüsselaustausch Funktionen* , die zum austauschen oder übertragen von Schlüsseln verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-116">*Key exchange functions* used to exchange or transmit keys.</span></span> <span data-ttu-id="00cc0-117">Weitere Informationen finden Sie unter [kryptografieschlüsselspeicher und Exchange](cryptographic-key-storage-and-exchange.md) -und [Schlüssel Generierungs-und Exchange-Funktionen](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-117">For more information, see [Cryptographic Key Storage and Exchange](cryptographic-key-storage-and-exchange.md) and [Key Generation and Exchange Functions](cryptography-functions.md).</span></span>

## <a name="certificate-encodedecode-functions"></a><span data-ttu-id="00cc0-118">Zertifikatcodieren/Decodieren von Funktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-118">Certificate Encode/Decode Functions</span></span>

-   <span data-ttu-id="00cc0-119">Funktionen, die zum Verschlüsseln oder Entschlüsseln von Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-119">Functions used to encrypt or decrypt data.</span></span> <span data-ttu-id="00cc0-120">Die Unterstützung ist auch für das [*hashingdata*](../secgloss/h-gly.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="00cc0-120">Support is also included for [*hashing*](../secgloss/h-gly.md) data.</span></span> <span data-ttu-id="00cc0-121">Weitere Informationen finden Sie unter [Datenverschlüsselungs-und Entschlüsselungs Funktionen](cryptography-functions.md) und [Datenverschlüsselung und Entschlüsselung](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-121">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md) and [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

## <a name="certificate-store-functions"></a><span data-ttu-id="00cc0-122">Zertifikat Speicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-122">Certificate Store Functions</span></span>

-   <span data-ttu-id="00cc0-123">Funktionen, die zum Verwalten von Sammlungen digitaler Zertifikate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-123">Functions used to manage collections of digital certificates.</span></span> <span data-ttu-id="00cc0-124">Weitere Informationen finden Sie unter [digitale Zertifikate](digital-certificates.md) und [Zertifikat Speicherfunktionen](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-124">For more information, see [Digital Certificates](digital-certificates.md) and [Certificate Store Functions](cryptography-functions.md).</span></span>

## <a name="simplified-message-functions"></a><span data-ttu-id="00cc0-125">Vereinfachte Nachrichten Funktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-125">Simplified Message Functions</span></span>

-   <span data-ttu-id="00cc0-126">Funktionen, die zum Verschlüsseln und Entschlüsseln von Nachrichten und Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-126">Functions used to encrypt and decrypt messages and data.</span></span>
-   <span data-ttu-id="00cc0-127">Funktionen zum Signieren von Nachrichten und Daten.</span><span class="sxs-lookup"><span data-stu-id="00cc0-127">Functions used to sign messages and data.</span></span>
-   <span data-ttu-id="00cc0-128">Funktionen, die verwendet werden, um die Authentizität von Signaturen in empfangenen Nachrichten und zugehörigen Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="00cc0-128">Functions used to verify the authenticity of signatures on received messages and related data.</span></span>

<span data-ttu-id="00cc0-129">Weitere Informationen finden Sie unter [vereinfachte Meldungen](simplified-messages.md) und [vereinfachte Nachrichten Funktionen](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-129">For more information, see [Simplified Messages](simplified-messages.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

## <a name="low-level-message-functions"></a><span data-ttu-id="00cc0-130">Nachrichten Funktionen auf niedriger Ebene</span><span class="sxs-lookup"><span data-stu-id="00cc0-130">Low-level Message Functions</span></span>

-   <span data-ttu-id="00cc0-131">Funktionen, die verwendet werden, um alle Aufgaben auszuführen, die von den vereinfachten Nachrichten Funktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-131">Functions used to perform all of the tasks performed by the simplified message functions.</span></span> <span data-ttu-id="00cc0-132">Die Nachrichten Funktionen auf niedriger Ebene bieten mehr Flexibilität als die vereinfachten Nachrichten Funktionen, erfordern jedoch mehr Funktionsaufrufe.</span><span class="sxs-lookup"><span data-stu-id="00cc0-132">The low-level message functions provide more flexibility than the simplified message functions but require more function calls.</span></span> <span data-ttu-id="00cc0-133">Weitere Informationen finden Sie unter [Nachrichten auf niedriger Ebene](low-level-messages.md) und auf [Low-Level-Nachrichten Funktionen](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-133">For more information, see [Low-level Messages](low-level-messages.md) and [Low-level Message Functions](cryptography-functions.md).</span></span>

![kryptoapi-Architektur](images/cryparch.png)

<span data-ttu-id="00cc0-135">Jeder Funktionsbereich verfügt über ein Schlüsselwort im Funktionsnamen, das den Funktionsbereich angibt.</span><span class="sxs-lookup"><span data-stu-id="00cc0-135">Each of the functional areas has a key word in its function name that indicates its functional area.</span></span>



| <span data-ttu-id="00cc0-136">Funktionsbereich</span><span class="sxs-lookup"><span data-stu-id="00cc0-136">Functional area</span></span>              | <span data-ttu-id="00cc0-137">Funktionsnamens Konvention</span><span class="sxs-lookup"><span data-stu-id="00cc0-137">Function name convention</span></span> |
|------------------------------|--------------------------|
| <span data-ttu-id="00cc0-138">Grundlegende Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-138">Base cryptographic functions</span></span> | <span data-ttu-id="00cc0-139">Schlendern</span><span class="sxs-lookup"><span data-stu-id="00cc0-139">Crypt</span></span>                    |
| <span data-ttu-id="00cc0-140">Codierung/Decodierung von Funktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-140">Encoding/decoding functions</span></span>  | <span data-ttu-id="00cc0-141">Schlendern</span><span class="sxs-lookup"><span data-stu-id="00cc0-141">Crypt</span></span>                    |
| <span data-ttu-id="00cc0-142">Zertifikat Speicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-142">Certificate store functions</span></span>  | <span data-ttu-id="00cc0-143">Speicher</span><span class="sxs-lookup"><span data-stu-id="00cc0-143">Store</span></span>                    |
| <span data-ttu-id="00cc0-144">Vereinfachte Nachrichten Funktionen</span><span class="sxs-lookup"><span data-stu-id="00cc0-144">Simplified message functions</span></span> | <span data-ttu-id="00cc0-145">`Message`</span><span class="sxs-lookup"><span data-stu-id="00cc0-145">Message</span></span>                  |
| <span data-ttu-id="00cc0-146">Nachrichten Funktionen auf niedriger Ebene</span><span class="sxs-lookup"><span data-stu-id="00cc0-146">Low-level message functions</span></span>  | <span data-ttu-id="00cc0-147">Meldung</span><span class="sxs-lookup"><span data-stu-id="00cc0-147">Msg</span></span>                      |



 

<span data-ttu-id="00cc0-148">Anwendungen verwenden Funktionen in allen diesen Bereichen.</span><span class="sxs-lookup"><span data-stu-id="00cc0-148">Applications use functions in all of these areas.</span></span> <span data-ttu-id="00cc0-149">Diese Funktionen bilden eine kryptografieapi.</span><span class="sxs-lookup"><span data-stu-id="00cc0-149">These functions, taken together, make up CryptoAPI.</span></span> <span data-ttu-id="00cc0-150">Die [*grundlegenden Kryptografiefunktionen*](../secgloss/b-gly.md) verwenden die CSPs für die erforderlichen Kryptografiealgorithmen und für die Generierung und sichere Speicherung von [Kryptografieschlüsseln](cryptographic-keys.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-150">The [*base cryptographic functions*](../secgloss/b-gly.md) use the CSPs for the necessary cryptographic algorithms and for the generation and secure storage of [cryptographic keys](cryptographic-keys.md).</span></span>

<span data-ttu-id="00cc0-151">Es werden zwei verschiedene Arten von Kryptografieschlüsseln verwendet: [*Sitzungsschlüssel*](../secgloss/s-gly.md), die für einzelne Verschlüsselungs-/Entschlüsselungs-und [*öffentliche/private Schlüsselpaare*](../secgloss/p-gly.md)verwendet werden, die permanent verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00cc0-151">Two different kinds of cryptographic keys are used: [*session keys*](../secgloss/s-gly.md), which are used for a single encryption/decryption, and [*public/private key pairs*](../secgloss/p-gly.md), which are used on a more permanent basis.</span></span>

> [!Note]  
> <span data-ttu-id="00cc0-152">Obwohl eine Anwendung direkt mit jedem der fünf Funktionsbereiche kommunizieren kann, kann Sie nicht direkt mit einem CSP kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="00cc0-152">Although an application can communicate directly with any of the five functional areas, it cannot communicate directly with a CSP.</span></span> <span data-ttu-id="00cc0-153">Die gesamte Kommunikation zwischen Anwendungen und CSP erfolgt über die [*grundlegenden Kryptografiefunktionen*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="00cc0-153">All application-to-CSP communications occur through the [*base cryptographic functions*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="00cc0-154">Grundlegende Kryptografiefunktionen verfügen über einen Parameter, der angibt, welcher CSP verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00cc0-154">Base cryptographic functions have a parameter that specifies which CSP to use.</span></span> <span data-ttu-id="00cc0-155">Dieser Parameter kann auf **null** festgelegt werden, um einen Standard-CSP auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="00cc0-155">This parameter can be set to **NULL** to select a default CSP.</span></span>

 

 

 
