---
title: Grundlagen zu Kompressor und Debug
description: Grundlagen zu Kompressor und Debug
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Videokomprimierungs-Manager (VCM), Öffnen von Kompressoren
- VCM (Videokomprimierungs-Manager), Öffnen von Kompressoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856052"
---
# <a name="compressor-and-decompressor-basics"></a><span data-ttu-id="f4806-105">Grundlagen zu Kompressor und Debug</span><span class="sxs-lookup"><span data-stu-id="f4806-105">Compressor and Decompressor Basics</span></span>

<span data-ttu-id="f4806-106">Zum Öffnen und Suchen eines Kompressors können Sie die [**iclocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) -Funktion und die [**icopen**](/windows/desktop/api/Vfw/nf-vfw-icopen) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4806-106">To open and locate a compressor, you can use the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="f4806-107">Sie können **iclocate** verwenden, um einen Kompressor eines bestimmten Typs zu finden und ein Handle dafür für die Verwendung in anderen VCM-Funktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4806-107">You can use **ICLocate** to find a compressor of a specific type and to obtain a handle of it for use in other VCM functions.</span></span> <span data-ttu-id="f4806-108">Zum Öffnen eines Kompressors können Sie **icopen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4806-108">To open a compressor, you can use **ICOpen**.</span></span> <span data-ttu-id="f4806-109">Die Anwendung verwendet das Handle, das von dieser Funktion zurückgegeben wird, um den geöffneten Kompressor zu identifizieren, wenn er andere VCM-Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4806-109">Your application uses the handle returned by this function to identify the opened compressor when it uses other VCM functions.</span></span>

<span data-ttu-id="f4806-110">Zum Öffnen und Suchen eines-Debug können Anwendungen die [**ICDE compressopen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) -und [**icdrawopen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) -Makros verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4806-110">To open and locate a decompressor, applications can use the [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) and [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macros.</span></span> <span data-ttu-id="f4806-111">Diese Makros verwenden **iclocate** für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f4806-111">These macros use **ICLocate** for operation.</span></span>

<span data-ttu-id="f4806-112">Wenn Ihre Anwendung die Verwendung eines Kompressors oder einer Debug-Debug abgeschlossen hat, muss Sie Sie schließen, um alle Ressourcen freizugeben, die für die Komprimierung oder die Komprimierung</span><span class="sxs-lookup"><span data-stu-id="f4806-112">When your application has finished using a compressor or decompressor, it must close it to free any resources used for compression or decompression.</span></span> <span data-ttu-id="f4806-113">Die Anwendung kann die [**icclose**](/windows/desktop/api/Vfw/nf-vfw-icclose) -Funktion verwenden, um den-Kompressor oder den-Debug zu schließen.</span><span class="sxs-lookup"><span data-stu-id="f4806-113">Your application can use the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function to close the compressor or decompressor.</span></span>

<span data-ttu-id="f4806-114">Außerdem kann die Anwendung die Kompressoren oder die Aufzählung auf einem System mithilfe der [**icinfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) -Funktion auflisten.</span><span class="sxs-lookup"><span data-stu-id="f4806-114">Also, your application can enumerate the compressors or decompressors on a system by using the [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) function.</span></span>

> [!Note]  
> <span data-ttu-id="f4806-115">Der Stream-Header in einer AVI-Datei enthält Informationen über den Streamtyp und den spezifischen Handler für diesen Stream.</span><span class="sxs-lookup"><span data-stu-id="f4806-115">The stream header in an AVI file contains information about the stream type and the specific handler for that stream.</span></span> <span data-ttu-id="f4806-116">Innerhalb des Stream-Headers identifizieren die Member **fcctype** und **fccHandler** den Streamtyp und den für den Stream angegebenen Stream-Handler.</span><span class="sxs-lookup"><span data-stu-id="f4806-116">Within the stream header, the **fccType** and **fccHandler** members identify the stream type and the stream handler specified for the stream.</span></span>

 

 

 




