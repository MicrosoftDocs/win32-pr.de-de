---
description: Ruft die attachproperties-Funktion auf, um die Eigenschaften zuzuordnen, die in einem erkannten Datenobjekt vorhanden sind.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementieren von attachproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350511"
---
# <a name="implementing-attachproperties"></a><span data-ttu-id="e128b-103">Implementieren von attachproperties</span><span class="sxs-lookup"><span data-stu-id="e128b-103">Implementing AttachProperties</span></span>

<span data-ttu-id="e128b-104">Netzwerkmonitor Ruft die [**attachproperties**](attachproperties.md) -Funktion auf, um die Eigenschaften zuzuordnen, die in einem erkannten Datenobjekt vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e128b-104">Network Monitor calls the [**AttachProperties**](attachproperties.md) function to map the properties that exist in a piece of recognized data.</span></span> <span data-ttu-id="e128b-105">Die [**attachproperties**](attachproperties.md) -Funktion ordnet die Eigenschaften einem bestimmten Speicherort zu.</span><span class="sxs-lookup"><span data-stu-id="e128b-105">The [**AttachProperties**](attachproperties.md) function maps the properties to a specific location.</span></span>

<span data-ttu-id="e128b-106">Netzwerkmonitor verwendet den folgenden Prozess, um die Daten in einem Frame zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="e128b-106">Network Monitor uses the following process to parse the data in a frame.</span></span>

-   <span data-ttu-id="e128b-107">Zuerst ruft Netzwerkmonitor [erkenzeframe](recognizeframe.md) auf, um alle Protokolle zu erkennen, die in einem Frame vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e128b-107">First, Network Monitor calls [RecognizeFrame](recognizeframe.md) to recognize all the protocols that exist in a frame.</span></span>
-   <span data-ttu-id="e128b-108">Dann ruft Netzwerkmonitor [**attachproperties**](attachproperties.md) für jeden Parser auf, der ein Datenelement erkennt.</span><span class="sxs-lookup"><span data-stu-id="e128b-108">Then, Network Monitor calls [**AttachProperties**](attachproperties.md) for each parser that recognizes a piece of data.</span></span>

<span data-ttu-id="e128b-109">Wenn Netzwerkmonitor die [attachproperties](attachproperties.md) -Funktion für die erkannten Daten aufruft, muss der aufgerufene Parser die Daten analysieren und dann jede vorhandene Eigenschaft einem Speicherort in den erkannten Daten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="e128b-109">When Network Monitor calls the [AttachProperties](attachproperties.md) function for the recognized data, the parser that is called must parse the data, and then map each existing property to a location in the recognized data.</span></span> <span data-ttu-id="e128b-110">Der Parser bestimmt, welche Eigenschaften vorhanden sind und wo sich jede Eigenschaft in den Daten befindet.</span><span class="sxs-lookup"><span data-stu-id="e128b-110">The parser determines which properties exist, and where each property is located in the data.</span></span> <span data-ttu-id="e128b-111">In der folgenden Abbildung werden vom Parser erkannte Daten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e128b-111">The following figure shows parser-recognized data.</span></span>

![vom Parser erkannte Daten](images/attachproperties1.png)

<span data-ttu-id="e128b-113">Während der Implementierung von [**attachproperties**](attachproperties.md)müssen Sie eine der folgenden Funktionen für jede Eigenschaft, die in einem Datenrahmen vorhanden ist, aufruft.</span><span class="sxs-lookup"><span data-stu-id="e128b-113">During the implementation of [**AttachProperties**](attachproperties.md), you must call one of the following functions for each property that exists in a data frame.</span></span>

-   <span data-ttu-id="e128b-114">Wenn Sie die Eigenschaften Daten in einem Frame ändern möchten, können Sie die [**attachpropertyinstanceex**](attachpropertyinstanceex.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e128b-114">Call the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you want to modify the property data in a frame.</span></span>
-   <span data-ttu-id="e128b-115">Wenn Sie die Eigenschaften Daten in einem Frame nicht ändern möchten, können Sie die [**attachpropertyinstance**](attachpropertyinstance.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e128b-115">Call the [**AttachPropertyInstance**](attachpropertyinstance.md) function when you do not want to modify the property data in a frame.</span></span>

> [!Note]  
> <span data-ttu-id="e128b-116">Es wird empfohlen, die Daten zu verwenden, wie Sie in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e128b-116">It is recommended that you use the data as it exists in the capture.</span></span>

 

<span data-ttu-id="e128b-117">Im folgenden Verfahren werden die erforderlichen Schritte zum Implementieren von [**attachproperties**](attachproperties.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e128b-117">The following procedure identifies the steps necessary to implement [**AttachProperties**](attachproperties.md).</span></span>

<span data-ttu-id="e128b-118">**So implementieren Sie attachproperties**</span><span class="sxs-lookup"><span data-stu-id="e128b-118">**To implement AttachProperties**</span></span>

1.  <span data-ttu-id="e128b-119">Bestimmen Sie, welche Eigenschaften vorhanden sind, und die Eigenschaften Position in den Daten.</span><span class="sxs-lookup"><span data-stu-id="e128b-119">Determine which properties exist, and the property location in the data.</span></span>
2.  <span data-ttu-id="e128b-120">Aufrufen von [**attachpropertyinstanceex**](attachpropertyinstanceex.md) für jede Eigenschaft mit einem Wert, den Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="e128b-120">Call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) for each property with a value that you want to modify.</span></span>
3.  <span data-ttu-id="e128b-121">Aufrufen von [**attachpropertyinstance**](attachpropertyinstance.md) für jede Eigenschaft mit einem Wert, den Sie nicht ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="e128b-121">Call [**AttachPropertyInstance**](attachpropertyinstance.md) for each property with a value that you do not want to modify.</span></span> <span data-ttu-id="e128b-122">In der Regel ist dies die einzige Funktion, die aufgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="e128b-122">Typically, this is the only function that you need to call.</span></span>

<span data-ttu-id="e128b-123">Im folgenden finden Sie eine grundlegende Implementierung von " [**attachproperties**](attachproperties.md)".</span><span class="sxs-lookup"><span data-stu-id="e128b-123">The following is a basic implementation of [**AttachProperties**](attachproperties.md).</span></span> <span data-ttu-id="e128b-124">Beachten Sie, dass das Beispiel weder den Code zum Bestimmen der vorhandenen Eigenschaften noch den Code zum Suchen der Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="e128b-124">Be aware that the example does not include either the code to determine which properties exist, or the code to locate the properties.</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



