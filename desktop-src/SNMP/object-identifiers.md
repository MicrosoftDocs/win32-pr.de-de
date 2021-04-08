---
title: Objekt Bezeichner (SNMP)
description: Ein SNMP-Objekt Bezeichner benennt ein Objekt eindeutig und identifiziert seinen Speicherort innerhalb einer MIB-Struktur (Management Information Base).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739329"
---
# <a name="object-identifiers-snmp"></a><span data-ttu-id="57b9b-103">Objekt Bezeichner (SNMP)</span><span class="sxs-lookup"><span data-stu-id="57b9b-103">Object Identifiers (SNMP)</span></span>

<span data-ttu-id="57b9b-104">Ein SNMP-Objekt Bezeichner benennt ein Objekt eindeutig und identifiziert seinen Speicherort innerhalb einer MIB-Struktur (Management Information Base).</span><span class="sxs-lookup"><span data-stu-id="57b9b-104">An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.</span></span> <span data-ttu-id="57b9b-105">Objekt Bezeichner sind Anwendungs unabhängige abstrakte Syntax Notation One (ASN. 1)-Datentypen, die aus einer Sequenz von nicht negativen ganzen Zahlen oder unter Elementen bestehen.</span><span class="sxs-lookup"><span data-stu-id="57b9b-105">Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers.</span></span> <span data-ttu-id="57b9b-106">Objekt Bezeichner müssen mindestens zwei untergeordnete IDs aufweisen, und Sie dürfen 128 subIdentifier nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="57b9b-106">Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.</span></span>

<span data-ttu-id="57b9b-107">Die WinSNMP-Programmierumgebung verwendet die [**smioid**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) -Struktur zum Verwalten von Objekt Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="57b9b-107">The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers.</span></span> <span data-ttu-id="57b9b-108">Das Format des objektbezeichnerarrays in einer **smioid** -Struktur ist ein subIdentifier pro Array-Element.</span><span class="sxs-lookup"><span data-stu-id="57b9b-108">The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.</span></span>

<span data-ttu-id="57b9b-109">Die Darstellung eines Objekt Bezeichners mit punktierter numerischer Zeichenfolge trennt seine unter Elemente in Zeiträume. Beispiel: "1.2.3.4.5.6".</span><span class="sxs-lookup"><span data-stu-id="57b9b-109">The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".</span></span>

<span data-ttu-id="57b9b-110">Weitere Informationen finden Sie in [der SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) und in den entsprechenden RFCs.</span><span class="sxs-lookup"><span data-stu-id="57b9b-110">For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.</span></span>

 

 




