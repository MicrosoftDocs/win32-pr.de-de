---
description: Das Anwenden einer Codierungs Regel auf die Datenstrukturen, die durch eine abstrakte Syntax beschrieben werden, bietet eine Übertragungs Syntax, die festlegt, wie Bytes in einem Stream beim Senden zwischen Computern organisiert werden.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: DER-Übertragungs Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569479"
---
# <a name="der-transfer-syntax"></a><span data-ttu-id="c2697-103">DER-Übertragungs Syntax</span><span class="sxs-lookup"><span data-stu-id="c2697-103">DER Transfer Syntax</span></span>

<span data-ttu-id="c2697-104">Das Anwenden einer Codierungs Regel auf die Datenstrukturen, die durch eine abstrakte Syntax beschrieben werden, bietet eine Übertragungs Syntax, die festlegt, wie Bytes in einem Stream beim Senden zwischen Computern organisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c2697-104">Applying an encoding rule to the data structures described by an abstract syntax provides a transfer syntax that governs how bytes in a stream are organized when sent between computers.</span></span> <span data-ttu-id="c2697-105">Die von Distinguished Encoding Rules verwendete Übertragungs Syntax folgt immer einem *Tag, einer Länge und einem Wert* Format.</span><span class="sxs-lookup"><span data-stu-id="c2697-105">The transfer syntax used by Distinguished Encoding Rules always follows a *Tag, Length, Value* format.</span></span> <span data-ttu-id="c2697-106">Das Format wird in der Regel als TLV-dreier bezeichnet, in dem jedes Feld (T, L oder V) mindestens ein Byte enthält.</span><span class="sxs-lookup"><span data-stu-id="c2697-106">The format is usually referred to as a TLV triplet in which each field (T, L, or V) contains one or more bytes.</span></span>

![der Typ, Länge und Wert (TLV)-dreier](images/der-tlv-basic.png)

<span data-ttu-id="c2697-108">Das *Tagfeld* gibt den Typ der zu sendenden Datenstruktur an, das *Längen* Feld gibt die Anzahl der Bytes an Inhalt an, die übertragen werden, und das *Wertfeld* enthält den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="c2697-108">The *Tag* field specifies the type of the data structure being sent, the *Length* field specifies the number of bytes of content being transferred, and the *Value* field contains the content.</span></span> <span data-ttu-id="c2697-109">Beachten Sie, dass das *Wertfeld* ein Dreier sein kann, wenn es einen konstruierten Datentyp enthält, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c2697-109">Note that the *Value* field can be a triplet if it contains a constructed data type as shown by the following illustration.</span></span>

![der-TLV-replerekursion](images/der-tlv-recursive.png)

<span data-ttu-id="c2697-111">In den folgenden Themen finden Sie ausführliche Informationen zu den Komponenten eines TLV-Dreiecks.</span><span class="sxs-lookup"><span data-stu-id="c2697-111">See the following topics for detailed information about the components of a TLV triplet.</span></span>

-   [<span data-ttu-id="c2697-112">Codierte tagbytes</span><span class="sxs-lookup"><span data-stu-id="c2697-112">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
-   [<span data-ttu-id="c2697-113">Codierte Länge und Wert Bytes</span><span class="sxs-lookup"><span data-stu-id="c2697-113">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a><span data-ttu-id="c2697-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2697-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2697-115">Konstruierte Typen</span><span class="sxs-lookup"><span data-stu-id="c2697-115">Constructed Types</span></span>](about-constructed-types.md)
</dt> <dt>

[<span data-ttu-id="c2697-116">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="c2697-116">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 



