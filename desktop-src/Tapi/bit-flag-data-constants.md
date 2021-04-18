---
description: Für erweiterbare Bitflag-Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte für angegebene Bits definieren.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Daten Konstanten Bit-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368222"
---
# <a name="bit-flag-data-constants"></a><span data-ttu-id="46aef-103">Daten Konstanten Bit-Flag</span><span class="sxs-lookup"><span data-stu-id="46aef-103">Bit-Flag Data Constants</span></span>

<span data-ttu-id="46aef-104">Für erweiterbare Bitflag-Daten Konstanten kann ein Anbieter von Dienstanbietern neue Werte für angegebene Bits definieren.</span><span class="sxs-lookup"><span data-stu-id="46aef-104">For extensible bit-flag data constants, a service-provider vendor can define new values for specified bits.</span></span> <span data-ttu-id="46aef-105">Da die meisten bitflagkonstanten **DWORD** s sind, ist eine bestimmte Anzahl von niedrigeren Bits in der Regel für allgemeine Erweiterungen reserviert, während die restlichen oberen Bits für herstellerspezifische Erweiterungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="46aef-105">Because most bit-flag constants are **DWORD** s, a specific number of the lower bits are usually reserved for common extensions, while the remaining upper bits are available for vendor-specific extensions.</span></span> <span data-ttu-id="46aef-106">Allgemeine Bitflags werden aus Bit 0 (null) zugewiesen, und herstellerspezifische Erweiterungen sollten von Bit 31 nach unten zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="46aef-106">Common bit flags are assigned from bit zero up, and vendor-specific extensions should be assigned from bit 31 down.</span></span> <span data-ttu-id="46aef-107">Dieses Schema bietet maximale Flexibilität beim Zuweisen von Bitpositionen zu allgemeinen Erweiterungen, im Gegensatz zu herstellerspezifischen Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="46aef-107">This scheme provides maximum flexibility in assigning bit positions to common extensions, as opposed to vendor-specific extensions.</span></span> <span data-ttu-id="46aef-108">Es wird erwartet, dass ein Anbieter neue Werte definiert, bei denen es sich um natürliche Erweiterungen der von der API definierten Bitflags handelt.</span><span class="sxs-lookup"><span data-stu-id="46aef-108">A vendor is expected to define new values that are natural extensions of the bit flags defined by the API.</span></span>

<span data-ttu-id="46aef-109">Erweiterbare Datenstrukturen verfügen über ein Feld mit variabler Größe, das für die gerätespezifische Verwendung reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="46aef-109">Extensible data structures have a variably sized field that is reserved for device-specific use.</span></span> <span data-ttu-id="46aef-110">Da die Größe des Felds variabel ist, entscheidet der Dienstanbieter die Menge an Informationen und die Interpretation des Felds.</span><span class="sxs-lookup"><span data-stu-id="46aef-110">Because the field is variably sized, the service provider decides the field's amount of information and interpretation.</span></span> <span data-ttu-id="46aef-111">Ein Anbieter, der ein Geräte spezifisches Feld definiert, wird davon ausgegangen, dass diese natürlichen Erweiterungen der ursprünglichen Datenstruktur durch die API definiert werden.</span><span class="sxs-lookup"><span data-stu-id="46aef-111">A vendor that defines a device-specific field is expected to make these natural extensions of the original data structure defined by the API.</span></span>

 

 



