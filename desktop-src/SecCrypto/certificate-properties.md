---
description: Die Zertifikat Dienste unterstützen die Verwendung von Zertifikaten, wie in der ITU-T-Empfehlung X. 509 (auch ISO/IEC 9594-8) definiert.
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Zertifikateigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864363"
---
# <a name="certificate-properties"></a><span data-ttu-id="0df16-103">Zertifikateigenschaften</span><span class="sxs-lookup"><span data-stu-id="0df16-103">Certificate Properties</span></span>

<span data-ttu-id="0df16-104">Die Zertifikat Dienste unterstützen die Verwendung von Zertifikaten, wie in der ITU-T-Empfehlung [*X. 509*](../secgloss/x-gly.md) (auch ISO/IEC 9594-8) definiert.</span><span class="sxs-lookup"><span data-stu-id="0df16-104">Certificate Services supports the use of certificates as defined in the ITU-T recommendation [*X.509*](../secgloss/x-gly.md) (also, ISO/IEC 9594-8).</span></span> <span data-ttu-id="0df16-105">Die folgenden Eigenschaften sind in einem X. 509-Standard Zertifikat enthalten.</span><span class="sxs-lookup"><span data-stu-id="0df16-105">The following are properties that are contained in a standard X.509 certificate.</span></span>



| <span data-ttu-id="0df16-106">Feld</span><span class="sxs-lookup"><span data-stu-id="0df16-106">Field</span></span>                                       | <span data-ttu-id="0df16-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0df16-107">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df16-108">Version</span><span class="sxs-lookup"><span data-stu-id="0df16-108">Version</span></span>                                     | <span data-ttu-id="0df16-109">Die Versionsnummer des Zertifikats Formats.</span><span class="sxs-lookup"><span data-stu-id="0df16-109">Version number of the certificate format.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="0df16-110">Seriennummer</span><span class="sxs-lookup"><span data-stu-id="0df16-110">Serial Number</span></span>                               | <span data-ttu-id="0df16-111">Seriennummer des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="0df16-111">Serial number of the certificate.</span></span> <span data-ttu-id="0df16-112">Diese Nummer wird vom Aussteller zugewiesen und ist innerhalb der Liste der ausgestellten Zertifikate des Ausstellers eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0df16-112">This number is assigned by the issuer and is unique within the issuer's list of issued certificates.</span></span>                                                                          |
| <span data-ttu-id="0df16-113">Algorithmusbezeichner und-Parameter</span><span class="sxs-lookup"><span data-stu-id="0df16-113">Algorithm Identifier and Parameters</span></span>         | <span data-ttu-id="0df16-114">Der Signatur Algorithmus und alle Parameter, die vom Aussteller verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0df16-114">Signature algorithm and any parameters used by the issuer.</span></span>                                                                                                                                                      |
| <span data-ttu-id="0df16-115">Issuer (Aussteller)</span><span class="sxs-lookup"><span data-stu-id="0df16-115">Issuer</span></span>                                      | <span data-ttu-id="0df16-116">Der Name der [*Zertifizierungs*](../secgloss/c-gly.md) Stelle, die das Zertifikat ausgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="0df16-116">Name of the [*certification authority*](../secgloss/c-gly.md) which issued the certificate.</span></span>                                               |
| <span data-ttu-id="0df16-117">Nicht vor (Datum)</span><span class="sxs-lookup"><span data-stu-id="0df16-117">Not Before (Date)</span></span>                           | <span data-ttu-id="0df16-118">Das Zertifikat ist vor diesem Datum ungültig.</span><span class="sxs-lookup"><span data-stu-id="0df16-118">Certificate not valid before this date.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="0df16-119">Nicht nach (Datum)</span><span class="sxs-lookup"><span data-stu-id="0df16-119">Not After (Date)</span></span>                            | <span data-ttu-id="0df16-120">Das Zertifikat ist nach diesem Datum ungültig.</span><span class="sxs-lookup"><span data-stu-id="0df16-120">Certificate not valid after this date.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="0df16-121">Antragstellername</span><span class="sxs-lookup"><span data-stu-id="0df16-121">Subject Name</span></span>                                | <span data-ttu-id="0df16-122">Der Name der Person oder Entität, für die das Zertifikat ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0df16-122">Name of the person or entity to whom the certificate is being issued.</span></span> <span data-ttu-id="0df16-123">Dieses Feld kann auch die Organisation, Organisationseinheit, Ort, Bundesstaat, Kanton und Land/Region des Zertifikats Empfängers enthalten.</span><span class="sxs-lookup"><span data-stu-id="0df16-123">This field can also include the certificate recipient's organization, organization unit, locality, state or province, and country/region.</span></span> |
| <span data-ttu-id="0df16-124">Algorithmus und Parameter für den öffentlichen Schlüssel des Antragstellers</span><span class="sxs-lookup"><span data-stu-id="0df16-124">Subject Public Key Algorithm and Parameters</span></span> | <span data-ttu-id="0df16-125">Der Algorithmus und alle Parameter, die für den [*öffentlichen Schlüssel*](../secgloss/p-gly.md)des Antragstellers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0df16-125">The algorithm and any parameters used for the subject's [*public key*](../secgloss/p-gly.md).</span></span>                                                                       |
| <span data-ttu-id="0df16-126">Öffentlicher Schlüssel des Antragstellers</span><span class="sxs-lookup"><span data-stu-id="0df16-126">Subject Public Key</span></span>                          | <span data-ttu-id="0df16-127">Der tatsächliche öffentliche Schlüssel (eine Bitzeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="0df16-127">The actual public key (a bit string).</span></span>                                                                                                                                                                           |
| <span data-ttu-id="0df16-128">Signatur</span><span class="sxs-lookup"><span data-stu-id="0df16-128">Signature</span></span>                                   | <span data-ttu-id="0df16-129">Die vom Aussteller bereitgestellte Signatur.</span><span class="sxs-lookup"><span data-stu-id="0df16-129">Signature as provided by the issuer.</span></span>                                                                                                                                                                            |



 

<span data-ttu-id="0df16-130">Abhängig von der [*X. 509*](../secgloss/x-gly.md) -Version des Zertifikats kann ein Zertifikat die folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="0df16-130">A certificate can contain the following items, depending on the [*X.509*](../secgloss/x-gly.md) version of the certificate.</span></span>



| <span data-ttu-id="0df16-131">Optionales Feld</span><span class="sxs-lookup"><span data-stu-id="0df16-131">Optional field</span></span>    | <span data-ttu-id="0df16-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0df16-132">Description</span></span>                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0df16-133">Eindeutige Aussteller-ID</span><span class="sxs-lookup"><span data-stu-id="0df16-133">Issuer Unique ID</span></span>  | <span data-ttu-id="0df16-134">Wird verwendet, um den Aussteller Namen eindeutig zu machen, wenn er von mehr als einer Entität verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0df16-134">Used to make the issuer name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="0df16-135">Nur in den Versionen [*X. 509*](../secgloss/x-gly.md) 2,0 oder höher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0df16-135">Present only in versions [*X.509*](../secgloss/x-gly.md) 2.0 or later.</span></span><br/> |
| <span data-ttu-id="0df16-136">Eindeutige Subjekt-ID</span><span class="sxs-lookup"><span data-stu-id="0df16-136">Subject unique ID</span></span> | <span data-ttu-id="0df16-137">Wird verwendet, um den Antragsteller Namen eindeutig zu machen, wenn er von mehr als einer Entität verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0df16-137">Used to make the subject name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="0df16-138">Nur in X. 509 2,0 oder höher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0df16-138">Present only in X.509 2.0 or later.</span></span><br/>                                                                     |
| <span data-ttu-id="0df16-139">Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="0df16-139">Extensions</span></span>        | <span data-ttu-id="0df16-140">Zum angeben gewünschter benutzerdefinierter Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0df16-140">For specifying any desired custom properties.</span></span> <span data-ttu-id="0df16-141">Im Zertifikat können beliebig viele Erweiterungs Felder eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0df16-141">Any number of extension fields can be included in the certificate.</span></span> <span data-ttu-id="0df16-142">Nur in Version X. 509 3,0 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0df16-142">Present only in version X.509 3.0.</span></span><br/>                                            |



 

> [!Note]  
> <span data-ttu-id="0df16-143">Die Microsoft Certificate Services gibt X. 509 Version 3-Zertifikate aus.</span><span class="sxs-lookup"><span data-stu-id="0df16-143">Microsoft Certificate Services issues X.509 version 3 certificates.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0df16-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0df16-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df16-145">Namens Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0df16-145">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
