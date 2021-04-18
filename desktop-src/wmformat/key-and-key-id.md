---
title: Schlüssel und Schlüssel-ID
description: Schlüssel und Schlüssel-ID
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), Schlüssel
- DRM (Digital Rights Management), Schlüssel
- Digital Rights Management (DRM), Kid
- DRM (Digital Rights Management), Kid
- Schlüssel-ID (Kid)
- Kid (Schlüssel-ID)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341445"
---
# <a name="key-and-key-id"></a><span data-ttu-id="84f1b-110">Schlüssel und Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="84f1b-110">Key and Key ID</span></span>

<span data-ttu-id="84f1b-111">Wenn Sie eine Datei packen, verwenden Sie einen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="84f1b-111">When you package a file, you use a key.</span></span> <span data-ttu-id="84f1b-112">Ein Schlüssel ist ein Datenelement, das in den Verschlüsselungsalgorithmen verwendet wird, mit denen der Inhalt geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="84f1b-112">A key is a piece of data used in the encryption algorithms that protect the content.</span></span> <span data-ttu-id="84f1b-113">Jeder Schlüssel besteht aus zwei Teilen: einem Ausgangswert für den Lizenzschlüssel und einer Schlüssel-ID (häufig als "Kid" abgekürzt).</span><span class="sxs-lookup"><span data-stu-id="84f1b-113">There are two parts to each key: a license key seed and a key ID (often abbreviated as KID).</span></span> <span data-ttu-id="84f1b-114">Die Schlüssel-ID ist öffentlich und wird im Dateiheader gespeichert, um den Schlüssel zu identifizieren, der zum Entschlüsseln der Datei erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="84f1b-114">The key ID is public, and is stored in the file header as a way to identify the key required to decrypt the file.</span></span> <span data-ttu-id="84f1b-115">Der Ausgangswert für den Lizenzschlüssel ist ein geheimer Wert, der vom Content Packager und vom Lizenz Aussteller gemeinsam genutzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="84f1b-115">The license key seed is a secret value that must be shared by the content packager and the license issuer.</span></span>

<span data-ttu-id="84f1b-116">Eine Schlüssel-ID identifiziert geschützte Inhalte aus der Perspektive der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="84f1b-116">A key ID identifies protected content from the perspective of the license.</span></span> <span data-ttu-id="84f1b-117">Sie können zwar dieselbe Schlüssel-ID für mehrere Dateien verwenden, es wird jedoch empfohlen, für jeden geschützten Inhalt stets eine eindeutige Schlüssel-ID zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="84f1b-117">Although you can use the same key ID for multiple files, it is recommended that you always use a unique key ID for each piece of protected content.</span></span>

<span data-ttu-id="84f1b-118">Viele der in dieser Dokumentation beschriebenen Methoden verwenden Schlüssel-ID-Zeichen folgen, um Lizenzen auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="84f1b-118">Many of the methods described in this documentation use key ID strings to select licenses.</span></span> <span data-ttu-id="84f1b-119">Diese Zeichen folgen enthalten die in Base64 codierte Schlüssel-ID.</span><span class="sxs-lookup"><span data-stu-id="84f1b-119">These strings contain the key ID encoded in base64.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84f1b-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84f1b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84f1b-121">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="84f1b-121">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




