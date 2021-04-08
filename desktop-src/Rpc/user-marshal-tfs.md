---
title: Benutzer Mars Hallen
description: Benutzer Mars Hall im Remote Prozedur Aufruf (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856140"
---
# <a name="user-marshal"></a><span data-ttu-id="ffcf3-103">Benutzer Mars Hallen</span><span class="sxs-lookup"><span data-stu-id="ffcf3-103">User-marshal</span></span>

<span data-ttu-id="ffcf3-104">Der Benutzer Mars Hall hat eine Format Zeichenfolge, die der folgenden ähnelt \_ :</span><span class="sxs-lookup"><span data-stu-id="ffcf3-104">User marshal has a format string that is similar to transmit\_as:</span></span>

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

<span data-ttu-id="ffcf3-105">Die Flags<1> Byte bestehen aus dem oberen Flag-Halbbyte und dem unteren Ausrichtungs-Halbbyte.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-105">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="ffcf3-106">Die oberen 2 Bits des Flag-Halbbyte werden verwendet, um zu beschreiben, ob der Wire-Typ als eindeutiger Zeiger, Verweis Zeiger oder kein Zeiger definiert ist (er kann kein PTR sein).</span><span class="sxs-lookup"><span data-stu-id="ffcf3-106">The upper 2 bits of the flag nibble are used to describe whether the wire type is defined as a unique pointer, reference pointer or no pointer (it cannot be a ptr).</span></span> <span data-ttu-id="ffcf3-107">Die folgenden Manifeste wurden definiert, um die Flags festzulegen/zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ffcf3-107">The following manifests have been defined to set/get the flags:</span></span>

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

<span data-ttu-id="ffcf3-108">Der Ausrichtungs Halbbyte des flagworts behält die Netzwerk Ausrichtung des übertragenen Typs bei.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-108">The alignment nibble of the flag word keeps the wire alignment of the transmitted type.</span></span>

<span data-ttu-id="ffcf3-109">Der vierfache \_ Index<2> ist ein Index der Rückruf Routine, vervierfachen der Benutzer Mars Hall Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-109">The quadruple\_index<2> is an index of the callback routine quadruple of the user marshal functions.</span></span> <span data-ttu-id="ffcf3-110">Die Routine Positionen lauten wie folgt: Größenanpassung, Marshalling, Marshalling und Freigeben von Routinen.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-110">The routine positions are as follow: sizing, marshaling, unmarshaling, and freeing routine.</span></span>

<span data-ttu-id="ffcf3-111">Die Arbeits \_ Speichergröße des Benutzer Typs \_ \_<2> bietet eine Größe für den benutzerspezifischen Typ, einschließlich unbekannter Typen.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-111">The user\_type\_memory\_size<2> provides a size for the user specific type, including unknown types.</span></span>

<span data-ttu-id="ffcf3-112">Die übertragene \_ \_ typpuffer \_ Größe<2> ist entweder 0 (null), wenn die Größe variiert, oder die tatsächliche Größe.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-112">The transmitted\_type\_buffer\_size<2> is either zero when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="ffcf3-113">Dies ist eine Optimierung, die es mittlerer l ermöglicht, Rückrufe bei der Größenanpassung des Puffers und auch bei der Freigabe zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-113">This is an optimization that enables MIDL to skip callbacks when sizing the buffer, and also when freeing.</span></span>

## <a name="range"></a><span data-ttu-id="ffcf3-114">Range</span><span class="sxs-lookup"><span data-stu-id="ffcf3-114">Range</span></span>

<span data-ttu-id="ffcf3-115">Die \[ Bereichs \] Überprüfung bietet zusätzliche Mittel für die Argument Validierung auf der NDR-Ebene.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-115">The \[range\] checking provides additional means for argument validation at the NDR layer.</span></span> <span data-ttu-id="ffcf3-116">Der \[ Bereichs \] Deskriptor weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="ffcf3-116">The \[range\] descriptor has the following format:</span></span>

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

<span data-ttu-id="ffcf3-117">Die Flags nehmen den oberen Halbbyte und den Typ den unteren Halbbyte des zweiten bytes.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-117">The flags take the upper nibble and the type the lower nibble of the second byte.</span></span> <span data-ttu-id="ffcf3-118">Der niedrige und hohe Wert hängen vom Typ der Variablen ab, die geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-118">The low and high values depend on the type of the variable to be checked.</span></span>

<span data-ttu-id="ffcf3-119">Die Flags sind als Erweiterungs Fahrzeuge gedacht. der Compiler hat das Halbbyte auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ffcf3-119">The flags are meant as an expansion vehicle; the compiler has been setting the nibble to zero.</span></span>

 

 




