---
description: Stellt Funktionen für die Generierung von Zufallszahlen, Konvertierungen und Codierung und Decodierung von Base64 bereit.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Utilities-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368677"
---
# <a name="utilities-object"></a><span data-ttu-id="af122-103">Utilities-Objekt</span><span class="sxs-lookup"><span data-stu-id="af122-103">Utilities object</span></span>

<span data-ttu-id="af122-104">\[Das Hilfsprogrammobjekt ist für die Verwendung in den Betriebssystemen verfügbar **, die im** Abschnitt "Anforderungen" angegeben sind.\]</span><span class="sxs-lookup"><span data-stu-id="af122-104">\[The **Utilities** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="af122-105">Das **Utilities** -Objekt stellt Funktionen für die Zufallszahlengenerierung, Konvertierungen und Codierung und Decodierung von Base64 bereit.</span><span class="sxs-lookup"><span data-stu-id="af122-105">The **Utilities** object provides functionality for random number generation, conversions, and encoding and decoding from base64.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="af122-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="af122-106">When to use</span></span>

<span data-ttu-id="af122-107">Das **Utilities** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="af122-107">The **Utilities** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="af122-108">Codieren Sie eine Zeichenfolge als Base64, oder Decodieren Sie eine Zeichenfolge aus base64.</span><span class="sxs-lookup"><span data-stu-id="af122-108">Encode a string as base64 or decode a string from base64.</span></span>
-   <span data-ttu-id="af122-109">Konvertiert eine Binär gepackte Zeichenfolge in ein Bytearray und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="af122-109">Convert a binary-packed string to a byte array and vice versa.</span></span>
-   <span data-ttu-id="af122-110">Konvertiert eine Binär gepackte Zeichenfolge in eine hexadezimale Zeichenfolge und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="af122-110">Convert a binary-packed string to a hexadecimal string and vice versa.</span></span>
-   <span data-ttu-id="af122-111">Generieren Sie eine sichere Zufallszahl.</span><span class="sxs-lookup"><span data-stu-id="af122-111">Generate a secure random number.</span></span>
-   <span data-ttu-id="af122-112">Konvertieren der Ortszeit in die koordinierte Weltzeit (Greenwich Mean Time) und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="af122-112">Convert local time to Coordinated Universal Time (Greenwich Mean Time) and vice versa.</span></span>

## <a name="members"></a><span data-ttu-id="af122-113">Member</span><span class="sxs-lookup"><span data-stu-id="af122-113">Members</span></span>

<span data-ttu-id="af122-114">Das **Hilfsprogrammobjekt verfügt** über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="af122-114">The **Utilities** object has these types of members:</span></span>

-   [<span data-ttu-id="af122-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="af122-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="af122-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="af122-116">Methods</span></span>

<span data-ttu-id="af122-117">Das **Utilities** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="af122-117">The **Utilities** object has these methods.</span></span>



| <span data-ttu-id="af122-118">Methode</span><span class="sxs-lookup"><span data-stu-id="af122-118">Method</span></span>                                                               | <span data-ttu-id="af122-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af122-119">Description</span></span>                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="af122-120">**Base64Decode**</span><span class="sxs-lookup"><span data-stu-id="af122-120">**Base64Decode**</span></span>](utilities-base64decode.md)                       | <span data-ttu-id="af122-121">Decodiert eine Zeichenfolge aus base64.</span><span class="sxs-lookup"><span data-stu-id="af122-121">Decodes a string from base64.</span></span><br/>                                     |
| [<span data-ttu-id="af122-122">**Einem base64encode**</span><span class="sxs-lookup"><span data-stu-id="af122-122">**Base64Encode**</span></span>](utilities-base64encode.md)                       | <span data-ttu-id="af122-123">Codiert eine Zeichenfolge als Base64.</span><span class="sxs-lookup"><span data-stu-id="af122-123">Encodes a string as base64.</span></span><br/>                                       |
| [<span data-ttu-id="af122-124">**Binarystringdebytearray**</span><span class="sxs-lookup"><span data-stu-id="af122-124">**BinaryStringToByteArray**</span></span>](utilities-binarystringtobytearray.md) | <span data-ttu-id="af122-125">Konvertiert eine Binär Zeichen-Zeichenfolge in ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="af122-125">Converts a binary-packed string to an array of bytes.</span></span><br/>             |
| [<span data-ttu-id="af122-126">**Binarydehex**</span><span class="sxs-lookup"><span data-stu-id="af122-126">**BinaryToHex**</span></span>](utilities-binarytohex.md)                         | <span data-ttu-id="af122-127">Konvertiert eine Binär Zeichen-Zeichenfolge in eine hexadezimale Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="af122-127">Converts a binary-packed string to a hexadecimal string.</span></span><br/>          |
| [<span data-ttu-id="af122-128">**Bytearraydebinarystring**</span><span class="sxs-lookup"><span data-stu-id="af122-128">**ByteArrayToBinaryString**</span></span>](utilities-bytearraytobinarystring.md) | <span data-ttu-id="af122-129">Konvertiert ein Bytearray in eine Zeichenfolge mit Binär Zeichen.</span><span class="sxs-lookup"><span data-stu-id="af122-129">Converts an array of bytes to a binary-packed string.</span></span><br/>             |
| [<span data-ttu-id="af122-130">**Getrandom**</span><span class="sxs-lookup"><span data-stu-id="af122-130">**GetRandom**</span></span>](utilities-getrandom.md)                             | <span data-ttu-id="af122-131">Generiert eine sichere Zufallszahl.</span><span class="sxs-lookup"><span data-stu-id="af122-131">Generates a secure random number.</span></span><br/>                                 |
| [<span data-ttu-id="af122-132">**Hexin Binärdatei**</span><span class="sxs-lookup"><span data-stu-id="af122-132">**HexToBinary**</span></span>](utilities-hextobinary.md)                         | <span data-ttu-id="af122-133">Konvertiert eine hexadezimale Zeichenfolge in eine Zeichenfolge mit Binär Zeichen.</span><span class="sxs-lookup"><span data-stu-id="af122-133">Converts a hexadecimal string to a binary-packed string.</span></span><br/>          |
| [<span data-ttu-id="af122-134">**Localtimetoutctime**</span><span class="sxs-lookup"><span data-stu-id="af122-134">**LocalTimeToUTCTime**</span></span>](utilities-localtimetoutctime.md)           | <span data-ttu-id="af122-135">Konvertiert die lokale Zeit des Computers in die koordinierte Weltzeit.</span><span class="sxs-lookup"><span data-stu-id="af122-135">Converts the computer's local time to Coordinated Universal Time.</span></span><br/> |
| [<span data-ttu-id="af122-136">**Utctimetolocaltime**</span><span class="sxs-lookup"><span data-stu-id="af122-136">**UTCTimeToLocalTime**</span></span>](utilities-utctimetolocaltime.md)           | <span data-ttu-id="af122-137">Konvertiert die koordinierte Weltzeit in die Ortszeit des Computers.</span><span class="sxs-lookup"><span data-stu-id="af122-137">Converts Coordinated Universal Time to the computer's local time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af122-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af122-138">Remarks</span></span>

<span data-ttu-id="af122-139">Das **Hilfsprogrammobjekt kann** erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="af122-139">The **Utilities** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="af122-140">Die ProgID für das **Hilfsprogrammobjekt ist** CAPICOM. Hilfsprogramme. 1.</span><span class="sxs-lookup"><span data-stu-id="af122-140">The ProgID for the **Utilities** object is CAPICOM.Utilities.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="af122-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af122-141">Requirements</span></span>



| <span data-ttu-id="af122-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af122-142">Requirement</span></span> | <span data-ttu-id="af122-143">Wert</span><span class="sxs-lookup"><span data-stu-id="af122-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af122-144">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="af122-144">Redistributable</span></span><br/> | <span data-ttu-id="af122-145">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="af122-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="af122-146">DLL</span><span class="sxs-lookup"><span data-stu-id="af122-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="af122-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af122-147"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




