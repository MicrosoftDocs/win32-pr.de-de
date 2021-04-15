---
title: Erstellen temporärer Streams
description: Erstellen temporärer Streams
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Avistreamcreate-Funktion
- Avistreamrelease-Funktion
- Avimakecompressedstream-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471196"
---
# <a name="creating-temporary-streams"></a><span data-ttu-id="c0c83-106">Erstellen temporärer Streams</span><span class="sxs-lookup"><span data-stu-id="c0c83-106">Creating Temporary Streams</span></span>

<span data-ttu-id="c0c83-107">Temporäre Datenströme können auf verschiedene Arten von Vorteil sein.</span><span class="sxs-lookup"><span data-stu-id="c0c83-107">Temporary streams can be beneficial in several ways.</span></span> <span data-ttu-id="c0c83-108">Sie können einen temporären Stream als einen Arbeitsdaten Strom verwenden, z. b. Wenn Sie das Streamformat ändern.</span><span class="sxs-lookup"><span data-stu-id="c0c83-108">You can use a temporary stream as a work stream, for example, when changing the stream format.</span></span> <span data-ttu-id="c0c83-109">Oder Sie können einen temporären Stream erstellen, um Teile anderer Streams zu speichern, die kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c0c83-109">Or you can create a temporary stream to hold portions of other streams that have been copied.</span></span>

<span data-ttu-id="c0c83-110">Sie können einen Stream im Speicher erstellen, der keiner Datei zugeordnet ist, indem Sie die [**avistreamcreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0c83-110">You can create a stream in memory that is not associated with any file by using the [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) function.</span></span> <span data-ttu-id="c0c83-111">Diese Funktion gibt die Adresse der Schnittstelle an den neuen Stream an einem angegebenen Speicherort zurück und wird intern von anderen Funktionen verwendet, die temporäre Datenströme erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0c83-111">This function returns the address of the interface to the new stream in a specified location and is used internally by other functions that create temporary streams.</span></span>

<span data-ttu-id="c0c83-112">Mithilfe der [**avimakecompressedstream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) -Funktion können Sie einen komprimierten Stream aus einem unkomprimierten Datenstrom erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0c83-112">You can create a compressed stream from an uncompressed stream by using the [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) function.</span></span> <span data-ttu-id="c0c83-113">Sie identifizieren den zu Komprimier erenden Stream, die Komprimierungs Methode und Komprimierungs Optionen sowie den Handler für den neuen Stream.</span><span class="sxs-lookup"><span data-stu-id="c0c83-113">You identify the stream to compress, the compression method and compression options, and the handler for the new stream.</span></span>

<span data-ttu-id="c0c83-114">Wenn Sie einen Stream, der mit **avistreamcreate** oder **avimakecompressedstream** erstellt wurde, nicht mehr verwenden, schließen Sie den Datenstrom mithilfe der [**avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c0c83-114">When you finish using a stream created with **AVIStreamCreate** or **AVIMakeCompressedStream**, close the stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="c0c83-115">**Avistreamrelease** gibt die Ressourcen frei, die für den temporären Stream verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0c83-115">**AVIStreamRelease** frees the resources the temporary stream used.</span></span>

 

 




