---
title: Arrays von gezählten Zeichen
description: Das \ size \_ is \-Attribut gibt die obere Grenze des Arrays an, während das \ length \_ ist \-Attribut die Anzahl der zu übermittelten Array Elemente angibt.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473645"
---
# <a name="counted-character-arrays"></a><span data-ttu-id="4c788-103">Arrays von gezählten Zeichen</span><span class="sxs-lookup"><span data-stu-id="4c788-103">Counted Character Arrays</span></span>

<span data-ttu-id="4c788-104">Die \[ [Größe \_ ist](/windows/desktop/Midl/size-is) " \] Attribute" gibt die obere Grenze des Arrays an, während die \[ [ \_ Länge](/windows/desktop/Midl/length-is) " \] Attribute" die Anzahl der zu übermittelten Array Elemente angibt.</span><span class="sxs-lookup"><span data-stu-id="4c788-104">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute indicates the upper bound of the array while the \[ [length\_is](/windows/desktop/Midl/length-is)\] attribute indicates the number of array elements to transmit.</span></span> <span data-ttu-id="4c788-105">Zusätzlich zum-Array muss der Remote Prozedur Prototyp alle Variablen enthalten, die die Länge oder Größe darstellen, die die übertragenen Array Elemente bestimmen (Sie können separate Parameter sein oder mit der Zeichenfolge in einer Struktur gebündelt werden).</span><span class="sxs-lookup"><span data-stu-id="4c788-105">In addition to the array, the remote procedure prototype must include any variables representing length or size that determine the transmitted array elements (they can be separate parameters or bundled with the string in a structure).</span></span> <span data-ttu-id="4c788-106">Diese Attribute können mit breit Zeichen-oder Einzel Byte-Zeichen Arrays genauso wie mit Arrays anderer Typen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c788-106">These attributes can be used with wide-character or single-byte character arrays just as they would be with arrays of other types.</span></span>

<span data-ttu-id="4c788-107">Die Informationen in diesem Abschnitt beschreiben Parameter Prototypen für Remote Prozeduren für Zeichen Arrays.</span><span class="sxs-lookup"><span data-stu-id="4c788-107">The information in this section describes remote procedure parameter prototypes for character arrays.</span></span> <span data-ttu-id="4c788-108">Es ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="4c788-108">It is divided into the following topics:</span></span>

-   <span data-ttu-id="4c788-109">[\[in, out, size \_ ist \] Prototype](-in-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="4c788-109">[\[in, out, size\_is\] Prototype](-in-out-size-is-prototype.md)</span></span>
-   <span data-ttu-id="4c788-110">[\[in, Größe \_ ist und ausgehend, Größe \_ ist \] Prototyp](-in-size-is-and-out-size-is-prototype.md)</span><span class="sxs-lookup"><span data-stu-id="4c788-110">[\[in, size\_is and out, size\_is\] Prototype](-in-size-is-and-out-size-is-prototype.md)</span></span>

 

 