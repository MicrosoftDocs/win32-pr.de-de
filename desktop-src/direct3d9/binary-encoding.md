---
description: In diesem Abschnitt wird die binäre Version des DirectX-Datei Formats (. x) ausführlich erläutert, das mit der Veröffentlichung von DirectX 3,0 eingeführt wurde.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Binärcodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344942"
---
# <a name="binary-encoding"></a><span data-ttu-id="7ac61-103">Binärcodierung</span><span class="sxs-lookup"><span data-stu-id="7ac61-103">Binary Encoding</span></span>

<span data-ttu-id="7ac61-104">In diesem Abschnitt wird die binäre Version des DirectX-Datei Formats (. x) ausführlich erläutert, das mit der Veröffentlichung von DirectX 3,0 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ac61-104">This section details the binary version of the DirectX (.x) file format as introduced with the release of DirectX 3.0.</span></span>

<span data-ttu-id="7ac61-105">Das Binärformat ist eine Tokendarstellung des Text Formats.</span><span class="sxs-lookup"><span data-stu-id="7ac61-105">The binary format is a tokenized representation of the text format.</span></span> <span data-ttu-id="7ac61-106">Token können eigenständig oder von primitiven Datensätzen begleitet werden.</span><span class="sxs-lookup"><span data-stu-id="7ac61-106">Tokens can be stand-alone or accompanied by primitive data records.</span></span> <span data-ttu-id="7ac61-107">Eigenständige Token verfügen über eine grammatikalische Struktur, und die erforderlichen Daten werden von Daten Satz basierten Token bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7ac61-107">Stand-alone tokens give grammatical structure, and record-bearing tokens supply the necessary data.</span></span>

<span data-ttu-id="7ac61-108">Beachten Sie, dass alle Daten im Little-Endian-Format gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7ac61-108">Note that all data is stored in little-endian format.</span></span> <span data-ttu-id="7ac61-109">Ein gültiger binärer Datenstrom besteht aus einem Header, gefolgt von Vorlagen und/oder Datenobjekten.</span><span class="sxs-lookup"><span data-stu-id="7ac61-109">A valid binary data stream consists of a header followed by templates and/or data objects.</span></span>

<span data-ttu-id="7ac61-110">In diesem Abschnitt werden die folgenden Komponenten des Binärdatei Formats erläutert und eine Beispiel Vorlage und ein binäres Datenobjekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7ac61-110">This section discusses the following components of the binary file format and provides an example template and binary data object.</span></span>

-   [<span data-ttu-id="7ac61-111">Header</span><span class="sxs-lookup"><span data-stu-id="7ac61-111">Header</span></span>](header.md)
-   [<span data-ttu-id="7ac61-112">Token</span><span class="sxs-lookup"><span data-stu-id="7ac61-112">Tokens</span></span>](tokens.md)
-   [<span data-ttu-id="7ac61-113">Tokendatensätze</span><span class="sxs-lookup"><span data-stu-id="7ac61-113">Token Records</span></span>](token-records.md)
-   [<span data-ttu-id="7ac61-114">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="7ac61-114">Templates</span></span>](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [<span data-ttu-id="7ac61-115">Daten</span><span class="sxs-lookup"><span data-stu-id="7ac61-115">Data</span></span>](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [<span data-ttu-id="7ac61-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ac61-116">Examples</span></span>](examples.md)

## <a name="related-topics"></a><span data-ttu-id="7ac61-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ac61-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac61-118">X-Datei Format Referenz</span><span class="sxs-lookup"><span data-stu-id="7ac61-118">X File Format Reference</span></span>](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



