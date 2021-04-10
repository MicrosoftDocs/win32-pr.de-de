---
description: Pktextract.exe ist ein Tool, das das PublicKeyToken-Attribut aus einer Zertifikatsdatei extrahiert.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131301"
---
# <a name="pktextractexe"></a><span data-ttu-id="18d82-103">Pktextract.exe</span><span class="sxs-lookup"><span data-stu-id="18d82-103">Pktextract.exe</span></span>

<span data-ttu-id="18d82-104">Pktextract.exe ist ein Tool, das das **PublicKeyToken** -Attribut aus einer Zertifikatsdatei extrahiert.</span><span class="sxs-lookup"><span data-stu-id="18d82-104">Pktextract.exe is a tool that extracts the **publicKeyToken** attribute from a certificate file.</span></span> <span data-ttu-id="18d82-105">Bei der Ausgabe handelt es sich um das **PublicKeyToken**, bei dem es sich um einen eindeutigen 16-Byte-Bezeichner (8-Byte) des öffentlichen Schlüssels handelt, der im Zertifikat vorhanden ist, in einem Format, das leicht in eine Assembly-Identitäts Anweisung eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="18d82-105">The output is the **publicKeyToken**, which is a unique 16-character (8-byte) identifier of the public key present in the certificate, in a format that can easily be pasted into an assembly identity statement.</span></span> <span data-ttu-id="18d82-106">Die Zertifikatsdatei muss sich im selben Verzeichnis wie Pktextract.exe befinden, um das Hilfsprogramm zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="18d82-106">The certificate file must be present in the same directory as Pktextract.exe to use the utility.</span></span> <span data-ttu-id="18d82-107">Pktextract.exe wird im Microsoft Windows Software Development Kit (SDK) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="18d82-107">Pktextract.exe is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="18d82-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="18d82-108">Syntax</span></span>

<span data-ttu-id="18d82-109">**pktextract.exe** *<filename. CER>* **\[ -quiet \] \[ -nologo \]**</span><span class="sxs-lookup"><span data-stu-id="18d82-109">**pktextract.exe** *<filename.cer>* **\[-quiet\] \[-nologo\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="18d82-110">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="18d82-110">Command Line Options</span></span>

<span data-ttu-id="18d82-111">Pktextract.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="18d82-111">Pktextract.exe uses the following case-insensitive command line options.</span></span>



| <span data-ttu-id="18d82-112">Option</span><span class="sxs-lookup"><span data-stu-id="18d82-112">Option</span></span>  | <span data-ttu-id="18d82-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18d82-113">Description</span></span>                                                          |
|---------|----------------------------------------------------------------------|
| <span data-ttu-id="18d82-114">-quiet</span><span class="sxs-lookup"><span data-stu-id="18d82-114">-quiet</span></span>  | <span data-ttu-id="18d82-115">Unterdrückt die vollständige Anzeige von Zertifikat Informationen.</span><span class="sxs-lookup"><span data-stu-id="18d82-115">Suppresses full display of certificate information.</span></span> <span data-ttu-id="18d82-116">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="18d82-116">Optional.</span></span>        |
| <span data-ttu-id="18d82-117">-nologo</span><span class="sxs-lookup"><span data-stu-id="18d82-117">-nologo</span></span> | <span data-ttu-id="18d82-118">Wird ohne Anzeige der standardmäßigen Microsoft-Copyright Daten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18d82-118">Runs without displaying standard Microsoft copyright data.</span></span> <span data-ttu-id="18d82-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="18d82-119">Optional.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="18d82-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18d82-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18d82-121">Parallele assemblyentwicklungtools</span><span class="sxs-lookup"><span data-stu-id="18d82-121">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



