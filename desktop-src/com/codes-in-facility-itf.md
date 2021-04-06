---
title: Codes in FACILITY_ITF
description: Codes in der \_ Einrichtung der Einrichtung
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947551"
---
# <a name="codes-in-facility_itf"></a><span data-ttu-id="b3a3d-103">Codes in der \_ Einrichtung der Einrichtung</span><span class="sxs-lookup"><span data-stu-id="b3a3d-103">Codes in FACILITY\_ITF</span></span>

<span data-ttu-id="b3a3d-104">**HRESULT** s mit Einrichtungen wie z. b. dem Werk \_ null und dem Werk- \_ RPC haben universelle Bedeutung, da Sie an einer einzigen Quelle definiert sind: Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-104">**HRESULT** s with facilities such as FACILITY\_NULL and FACILITY\_RPC have universal meaning because they are defined at a single source: Microsoft.</span></span> <span data-ttu-id="b3a3d-105">**HRESULT** s in der Anlage " \_ ITF" werden jedoch durch die Funktion oder Schnittstellen Methode bestimmt, von der Sie zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-105">However, **HRESULT** s in FACILITY\_ITF are determined by the function or interface method from which they are returned.</span></span> <span data-ttu-id="b3a3d-106">Dies bedeutet, dass derselbe 32-Bit-Wert in Einrichtung, der \_ von zwei verschiedenen Schnittstellen Methoden zurückgegeben wurde, möglicherweise eine andere Bedeutung hat.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-106">This means that the same 32-bit value in FACILITY\_ITF returned from two different interface methods might have different meanings.</span></span>

<span data-ttu-id="b3a3d-107">Der Grund für **HRESULT** s in der Einrichtung \_ von "ITF" kann in verschiedenen Schnittstellen unterschiedliche Bedeutungen haben, da **HRESULT** s in einer effizienten Datentyp Größe von 32 Bits aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-107">The reason **HRESULT** s in FACILITY\_ITF can have different meanings in different interfaces is that **HRESULT** s are kept to an efficient data type size of 32 bits.</span></span> <span data-ttu-id="b3a3d-108">Leider ist 32 Bits nicht groß genug für die Entwicklung eines Fehlercode-Zuordnungs Systems, das in Konflikt stehende Codes vermeidet, die von verschiedenen Programmierern zu unterschiedlichen Zeiten an unterschiedlichen Stellen zugeordnet werden (im Gegensatz zur Handhabung von Schnittstellen bezeichmern und CLSIDs).</span><span class="sxs-lookup"><span data-stu-id="b3a3d-108">Unfortunately, 32 bits is not large enough for the development of an error code allocation system that avoids conflicting codes allocated by different programmers at different times in different places (unlike the handling of interface identifiers and CLSIDs).</span></span> <span data-ttu-id="b3a3d-109">Demzufolge ist das 32-Bit- **HRESULT** so strukturiert, dass Microsoft mehrere universelle Fehlercodes definieren und anderen Programmierern das Definieren neuer Fehlercodes ohne Angst vor Konflikten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-109">As a result, the 32-bit **HRESULT** is structured such that Microsoft can define several universal error codes, while allowing other programmers to define new error codes without fear of conflict.</span></span> <span data-ttu-id="b3a3d-110">Die Statuscode Konvention lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b3a3d-110">The status code convention is as follows:</span></span>

-   <span data-ttu-id="b3a3d-111">Status Codes in anderen Einrichtungen als Einrichtung- \_ ITF können nur von Microsoft definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-111">Status codes in facilities other than FACILITY\_ITF can be defined only by Microsoft.</span></span>
-   <span data-ttu-id="b3a3d-112">Statuscodes in der Einrichtung der Einrichtung \_ werden ausschließlich vom Entwickler der-Schnittstelle oder der-Funktion definiert, die den Statuscode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-112">Status codes in facility FACILITY\_ITF are defined solely by the developer of the interface or function that returns the status code.</span></span> <span data-ttu-id="b3a3d-113">Um widersprüchliche Fehlercodes zu vermeiden, ist der Benutzer, der die Schnittstelle definiert, verantwortlich für die Koordination und Veröffentlichung der \_ mit dieser Schnittstelle verknüpften Statuscodes der Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-113">To avoid conflicting error codes, whoever defines the interface is responsible for coordinating and publishing the FACILITY\_ITF status codes associated with that interface.</span></span>

<span data-ttu-id="b3a3d-114">Alle com-definierten Einrichtung- \_ Codes der Einrichtung haben einen Codewert im Bereich von 0x0000-0x01ff.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-114">All the COM-defined FACILITY\_ITF codes have a code value in the range of 0x0000-0x01FF.</span></span> <span data-ttu-id="b3a3d-115">Es ist zwar zulässig, beliebige Codes in der Einrichtung von "" zu verwenden \_ , es wird jedoch empfohlen, dass nur Codewerte im Bereich von 0x0200-0xFFFF verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-115">While it is legal to use any codes in FACILITY\_ITF, it is recommended that only code values in the range of 0x0200-0xFFFF be used.</span></span> <span data-ttu-id="b3a3d-116">Diese Empfehlung dient als Mittel zum Reduzieren von Verwirrung durch com-definierte Fehler.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-116">This recommendation is made as a means of reducing confusion with any COM-defined errors.</span></span>

<span data-ttu-id="b3a3d-117">Außerdem wird empfohlen, dass Entwickler neue Funktionen und Schnittstellen definieren, um Fehlercodes gemäß der Definition durch com und in anderen Einrichtungen als in der Einrichtung von "Einrichtung" zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="b3a3d-117">It is also recommended that developers define new functions and interfaces to return error codes as defined by COM and in facilities other than FACILITY\_ITF.</span></span> <span data-ttu-id="b3a3d-118">Insbesondere sollten Schnittstellen, die die Möglichkeit haben, in Zukunft Remote über RPC zu sein, die Standort- \_ RPC-Codes als legal definieren.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-118">In particular, interfaces that have any chance of being remoted using RPC in the future should define the FACILITY\_RPC codes as legal.</span></span> <span data-ttu-id="b3a3d-119">E \_ unerwartet ist ein bestimmter Fehlercode, der von den meisten Entwicklern universell legal gemacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3a3d-119">E\_UNEXPECTED is a specific error code that most developers will want to make universally legal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3a3d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3a3d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3a3d-121">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="b3a3d-121">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




