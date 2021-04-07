---
description: Die directxmath-Bibliothek bietet eine Reihe von Strukturen und definierten Typen zum Kapseln von Daten, um die Benutzerfreundlichkeit, Optimierung und Portabilität zu unterstützen.
ms.assetid: 4b9ffc17-3917-551c-7cb5-19de505dfd21
title: Directxmath-Bibliothekstypen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ac888e451fe1e1ba5cfc66184bf2eb7b6feffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863484"
---
# <a name="directxmath-library-types"></a><span data-ttu-id="a0d9d-103">Directxmath-Bibliothekstypen</span><span class="sxs-lookup"><span data-stu-id="a0d9d-103">DirectXMath Library types</span></span>

<span data-ttu-id="a0d9d-104">Die directxmath-Bibliothek bietet eine Reihe von Strukturen und definierten Typen zum Kapseln von Daten, um die Benutzerfreundlichkeit, Optimierung und Portabilität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-104">The DirectXMath Library provides a number of structures and defined types to encapsulate data to support ease of use, optimization, and portability.</span></span>

<span data-ttu-id="a0d9d-105">Die nachstehende Liste enthält Strukturen, die zurzeit Teil der directxmath-Bibliothek sind und über den directxmath. h-Header verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-105">The list below includes structures currently part of the DirectXMath Library, and available through the DirectXMath.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a0d9d-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a0d9d-106">In this section</span></span>



| <span data-ttu-id="a0d9d-107">Thema</span><span class="sxs-lookup"><span data-stu-id="a0d9d-107">Topic</span></span>                                                             | <span data-ttu-id="a0d9d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0d9d-108">Description</span></span>                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0d9d-109">**Halbdatentyp**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-109">**HALF Data Type**</span></span>](half-data-type.md)<br/>               | <span data-ttu-id="a0d9d-110">Ein Alias für **UInt16 \_ t** mit einer 16-Bit-Gleit Komma Zahl, die aus einem Vorzeichen-Bit, einem 5-Bit-Exponenten und einer 10-Bit-Mantisse besteht.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-110">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span><br/>                         |
| [<span data-ttu-id="a0d9d-111">**Xmvector-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-111">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)<br/>       | <span data-ttu-id="a0d9d-112">Ein portabler Typ, der zum Darstellen eines Vektors von Gleit Komma-oder ganzzahligen 4 32-Bit-Komponenten verwendet wird, die jeweils optimal ausgerichtet und einem Hardware Vektor Register zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-112">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span><br/>       |
| [<span data-ttu-id="a0d9d-113">**XMVECTORF32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-113">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)<br/> | <span data-ttu-id="a0d9d-114">Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Gleit Komma Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-114">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/> |
| [<span data-ttu-id="a0d9d-115">**XMVECTORI32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-115">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)<br/> | <span data-ttu-id="a0d9d-116">Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von ganzzahligen Werten in eine Instanz des [**xmvector**](xmvector-data-type.md) -Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-116">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/>        |
| [<span data-ttu-id="a0d9d-117">**XMVECTORU32-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-117">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)<br/> | <span data-ttu-id="a0d9d-118">Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von UInt32 \_ t-Werten in eine Instanz des xmvector-Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-118">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of XMVECTOR type.</span></span><br/>                                    |
| [<span data-ttu-id="a0d9d-119">**XMVECTORU8-Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-119">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)<br/>   | <span data-ttu-id="a0d9d-120">Ein undurchsichtiger, portabler Typ, der die Verwendung der C/C++-initialisierersyntax zum Laden von Uint8 \_ t-Werten in eine Instanz des xmvector-Typs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-120">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of XMVECTOR type.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="a0d9d-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0d9d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d9d-122">Directxmath-Programmier Referenz</span><span class="sxs-lookup"><span data-stu-id="a0d9d-122">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)
</dt> </dl>

 

 




