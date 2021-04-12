---
title: Verwalten von Objekt bezeichlern
description: Die WinSNMP-API bietet mehrere WinSNMP-Hilfsprogrammfunktionen, die die Bearbeitung von Objekt Bezeichners für WinSNMP-Anwendungen vereinfachen.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471644"
---
# <a name="managing-object-identifiers"></a><span data-ttu-id="277bf-103">Verwalten von Objekt bezeichlern</span><span class="sxs-lookup"><span data-stu-id="277bf-103">Managing Object Identifiers</span></span>

<span data-ttu-id="277bf-104">Die WinSNMP-API bietet mehrere [WinSNMP-Hilfsprogrammfunktionen](winsnmp-functions.md) , die die Bearbeitung von Objekt Bezeichners für WinSNMP-Anwendungen vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="277bf-104">The WinSNMP API provides several [WinSNMP utility functions](winsnmp-functions.md) that simplify the manipulation of object identifiers for WinSNMP applications.</span></span>

<span data-ttu-id="277bf-105">Die [**snmpoidtostr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) -Funktion konvertiert die interne binäre Darstellung eines Objekt Bezeichners in das gepunktete numerische Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="277bf-105">The [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) function converts the internal binary representation of an object identifier to its dotted numeric string format.</span></span> <span data-ttu-id="277bf-106">Wenn Sie [**snmpoidtostr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)aufzurufen, geben Sie einen Zeichen folgen Puffer mit der Länge maxobjidgersize (1408 Bytes) an, um sicherzustellen, dass der Ausgabepuffer groß genug für die konvertierte Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="277bf-106">When you call [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specify a string buffer of MAXOBJIDSTRSIZE length (1408 bytes) to ensure that the output buffer is large enough to hold the converted string.</span></span> <span data-ttu-id="277bf-107">Um einen Objekt Bezeichner aus dem Format der punktierten numerischen Zeichenfolge in seine interne binäre Darstellung zu konvertieren, müssen Sie die Funktion [**snmpstrautooid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) abrufen.</span><span class="sxs-lookup"><span data-stu-id="277bf-107">To convert an object identifier from the dotted numeric string format to its internal binary representation, call the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) function.</span></span>

<span data-ttu-id="277bf-108">Zum Kopieren eines SNMP-Objekt Bezeichners wird die [**snmpoidcopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="277bf-108">To copy an SNMP object identifier call the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) function.</span></span> <span data-ttu-id="277bf-109">Diese Funktion ordnet den erforderlichen Speicherplatz für den neuen Objekt Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="277bf-109">This function allocates any necessary memory for the new object identifier.</span></span>

<span data-ttu-id="277bf-110">Eine WinSNMP-Anwendung muss die [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) -Funktion aufruft, um Ressourcen freizugeben, die für den **ptr** -Member der [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur reserviert sind, die sowohl durch die [**snmpstrautooid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) -als auch die [**snmpoidcopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) -Funktion angegeben wird</span><span class="sxs-lookup"><span data-stu-id="277bf-110">A WinSNMP application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free resources allocated for the **ptr** member of the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure specified by both the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) and the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) functions.</span></span>

<span data-ttu-id="277bf-111">Die [**snmpoidcompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) -Funktion vergleicht zwei SNMP-Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="277bf-111">The [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) function compares two SNMP object identifiers.</span></span> <span data-ttu-id="277bf-112">Die WinSNMP-Anwendung kann die Anzahl der zu vergleichenden untergeordneten Elemente angeben.</span><span class="sxs-lookup"><span data-stu-id="277bf-112">The WinSNMP application can specify the number of subidentifiers to compare.</span></span> <span data-ttu-id="277bf-113">Rufen Sie **snmpoidcompare** auf, um zu bestimmen, ob zwei Objekt Bezeichner über allgemeine Präfixe verfügen.</span><span class="sxs-lookup"><span data-stu-id="277bf-113">Call **SnmpOidCompare** to determine whether two object identifiers have common prefixes.</span></span>

<span data-ttu-id="277bf-114">Weitere Informationen zum Verwalten des Arbeitsspeichers, der den Objekt Bezeichners zugeordnet ist, finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="277bf-114">For additional information about managing the memory allocated for object identifiers, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




