---
title: WinSNMP-Deskriptoren
description: In der WinSNMP-Programmierumgebung handelt es sich bei einem Deskriptor um eine der beiden folgenden Strukturen.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309443"
---
# <a name="winsnmp-descriptors"></a><span data-ttu-id="a5374-103">WinSNMP-Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="a5374-103">WinSNMP Descriptors</span></span>

<span data-ttu-id="a5374-104">In der WinSNMP-Programmierumgebung handelt es sich bei einem *Deskriptor* um eine der folgenden beiden Strukturen:</span><span class="sxs-lookup"><span data-stu-id="a5374-104">In the WinSNMP programming environment a *descriptor* is one of the following two structures:</span></span>

-   <span data-ttu-id="a5374-105">Eine [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Struktur, die eine Oktett-Zeichen folgen Variable beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a5374-105">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure which describes an octet string variable</span></span>
-   <span data-ttu-id="a5374-106">Eine [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur, die eine SNMP-objektbezeichnervariable beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a5374-106">An [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure which describes an SNMP object identifier variable</span></span>

<span data-ttu-id="a5374-107">Ein WinSNMP-Deskriptor ist eine Struktur mit zwei Membern: einem Längen Element, **len** und einem Zeigermember ( **ptr**).</span><span class="sxs-lookup"><span data-stu-id="a5374-107">A WinSNMP descriptor is a structure that has two members: a length member, **len**, and a pointer member, **ptr**.</span></span> <span data-ttu-id="a5374-108">Das **ptr** -Element verweist auf die Oktett-Zeichenfolge oder den Objekt Bezeichner von Interesse.</span><span class="sxs-lookup"><span data-stu-id="a5374-108">The **ptr** member points to the octet string or object identifier of interest.</span></span> <span data-ttu-id="a5374-109">Der **ptr** -Member kann entweder der Datentyp " **smilpbyte** " oder " **smiLPUINT32** " sein.</span><span class="sxs-lookup"><span data-stu-id="a5374-109">The **ptr** member can be either the **smiLPBYTE** or **smiLPUINT32** data type.</span></span>

<span data-ttu-id="a5374-110">Ein [**smioctets**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) -Deskriptor oder ein [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Deskriptor kann der **Wertmember** einer **smivalue** -Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="a5374-110">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor or an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) descriptor can be the **value** member of an **smiVALUE** structure.</span></span> <span data-ttu-id="a5374-111">Die [**smivalue**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) -Struktur beschreibt den Wert, der einem Variablennamen in einem Variablen Bindungs Eintrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5374-111">The [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure describes the value associated with a variable name in a variable binding entry.</span></span>

<span data-ttu-id="a5374-112">Die Microsoft WinSNMP-Implementierung ordnet Speicher für alle **ausgabesmioctets** und **smioid** -Strukturen zu und hebt deren Zuordnung auf.</span><span class="sxs-lookup"><span data-stu-id="a5374-112">The Microsoft WinSNMP implementation allocates and deallocates memory for all output **smiOCTETS** and **smiOID** structures.</span></span> <span data-ttu-id="a5374-113">Daher muss die Anwendung die [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) -Funktion aufruft, um den Arbeitsspeicher für den **ptr** -Member dieser Strukturen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a5374-113">Therefore, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free the memory for the **ptr** member of these structures.</span></span>

<span data-ttu-id="a5374-114">Zeichen folgen Elemente in Deskriptoren benötigen kein **null** -terminierendes Byte.</span><span class="sxs-lookup"><span data-stu-id="a5374-114">String members in descriptors do not require a **NULL** terminating byte.</span></span> <span data-ttu-id="a5374-115">Weitere Informationen zum Verwalten des Arbeitsspeichers, der Deskriptoren zugeordnet ist, finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a5374-115">For additional information about managing the memory allocated for descriptors, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




