---
title: Verwalten einer Variablen Bindungs Liste
description: Die snmpgetvb-Funktion ruft Variablen Bindungs Informationen aus einer Variablen Bindungs Liste ab. Die-Funktion Ruft den Variablennamen und den zugeordneten Wert der Variablen aus dem Variablen Bindungs Eintrag ab, der von der WinSNMP-Anwendung angegeben wird.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036715"
---
# <a name="managing-a-variable-binding-list"></a><span data-ttu-id="14255-104">Verwalten einer Variablen Bindungs Liste</span><span class="sxs-lookup"><span data-stu-id="14255-104">Managing a Variable Binding List</span></span>

<span data-ttu-id="14255-105">Die [**snmpgetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) -Funktion ruft Variablen Bindungs Informationen aus einer Variablen Bindungs Liste ab.</span><span class="sxs-lookup"><span data-stu-id="14255-105">The [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) function retrieves variable binding information from a variable binding list.</span></span> <span data-ttu-id="14255-106">Die-Funktion Ruft den Variablennamen und den zugeordneten Wert der Variablen aus dem Variablen Bindungs Eintrag ab, der von der WinSNMP-Anwendung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="14255-106">The function retrieves the variable name and the variable's associated value from the variable binding entry specified by the WinSNMP application.</span></span>

<span data-ttu-id="14255-107">Um Variablen Bindungs Einträge in einer Variablen Bindungs Liste zu aktualisieren, müssen Sie die [**snmpsetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14255-107">To update variable binding entries in a variable binding list, call the [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) function.</span></span> <span data-ttu-id="14255-108">Die **snmpsetvb** -Funktion fügt auch neue Variablen Bindungs Einträge an eine vorhandene Variablen Bindungs Liste an.</span><span class="sxs-lookup"><span data-stu-id="14255-108">The **SnmpSetVb** function also appends new variable binding entries to an existing variable binding list.</span></span>

<span data-ttu-id="14255-109">Die WinSNMP-Anwendung muss die [**snmpdeletevb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) -Funktion aufrufen, um Einträge aus einer Variablen Bindungs Liste zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="14255-109">The WinSNMP application must call the [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) function to remove entries from a variable binding list.</span></span>

<span data-ttu-id="14255-110">Zum Abrufen, ändern oder Löschen eines Variablen Bindungs Eintrags muss in der WinSNMP-Anwendung die Position des Eintrags in der Variablen Bindungs Liste angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14255-110">To retrieve, modify or delete a variable binding entry, the WinSNMP application must specify the position of the entry in the variable binding list.</span></span>

<span data-ttu-id="14255-111">Ein Aufrufen der [**snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) -Funktion ordnet eine Variablen Bindungs Liste einem PDU zu.</span><span class="sxs-lookup"><span data-stu-id="14255-111">A call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function associates a variable binding list with a PDU.</span></span> <span data-ttu-id="14255-112">Ein Aufrufen der [**snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) -Funktion Ruft eine Variablen Bindungs Liste aus einem PDU ab.</span><span class="sxs-lookup"><span data-stu-id="14255-112">A call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function retrieves a variable binding list from a PDU.</span></span> <span data-ttu-id="14255-113">Eine einzelne Variablen Bindung ist nicht direkt einem PDU zugeordnet, aber Sie ist indirekt durch die Einbindung in eine Variablen Bindungs Liste verknüpft.</span><span class="sxs-lookup"><span data-stu-id="14255-113">An individual variable binding is not directly associated with a PDU, but it is indirectly associated through its inclusion in a variable binding list.</span></span>

 

 




