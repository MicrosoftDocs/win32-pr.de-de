---
title: Erstellen einer Variablen Bindungs Liste
description: Die snmpkreatevbl-Funktion erstellt eine neue Variablen Bindungs Liste.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206883"
---
# <a name="creating-a-variable-binding-list"></a><span data-ttu-id="76d16-103">Erstellen einer Variablen Bindungs Liste</span><span class="sxs-lookup"><span data-stu-id="76d16-103">Creating a Variable Binding List</span></span>

<span data-ttu-id="76d16-104">Die [**snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) -Funktion erstellt eine neue Variablen Bindungs Liste.</span><span class="sxs-lookup"><span data-stu-id="76d16-104">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function creates a new variable binding list.</span></span> <span data-ttu-id="76d16-105">Wenn die WinSNMP-Anwendung einen Variablennamen und einen Wert angibt, erstellt die Funktion die Liste und fügt den Namen und den Wert als ersten Eintrag in der Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="76d16-105">If the WinSNMP application specifies a variable name and a value, the function creates the list and adds the name and value as the first entry in the list.</span></span> <span data-ttu-id="76d16-106">Wenn die Anwendung für den Variablennamen **null** angibt, erstellt die Funktion eine leere Liste.</span><span class="sxs-lookup"><span data-stu-id="76d16-106">If the application specifies **NULL** for the variable name, the function creates an empty list.</span></span>

<span data-ttu-id="76d16-107">Um eine Variablen Bindungs Liste zu kopieren, nennen Sie die Funktion [**snmpduplialisievbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) .</span><span class="sxs-lookup"><span data-stu-id="76d16-107">To copy a variable binding list, call the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> <span data-ttu-id="76d16-108">Die-Funktion erstellt eine neue Variablen Bindungs Liste und initialisiert die neue Liste mit einer Kopie der Daten in der Bindungs Liste der Quell Variablen.</span><span class="sxs-lookup"><span data-stu-id="76d16-108">The function creates a new variable binding list and initializes the new list with a copy of the data in the source variable binding list.</span></span>

<span data-ttu-id="76d16-109">Die Funktion [**snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) und die Funktion [**snmpduplimpevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) belegen den erforderlichen Arbeitsspeicher für die neue Variablen Bindungs Liste.</span><span class="sxs-lookup"><span data-stu-id="76d16-109">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function and the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function allocate any necessary memory for the new variable binding list.</span></span> <span data-ttu-id="76d16-110">Die WinSNMP-Anwendung muss die dieser Liste zugeordneten Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="76d16-110">The WinSNMP application must release the resources associated with these lists.</span></span> <span data-ttu-id="76d16-111">Es wird empfohlen, dass die Anwendung dies durchsucht, indem Sie die einzelnen Aufrufe von [**snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) und [**snmpduplicallevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) mit einem entsprechenden Aufrufen der Funktion [**snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) vergleichen, wenn es angebracht ist, den belegten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="76d16-111">It is recommended that the application do this by matching each call to [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) and [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) with a corresponding call to the [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) function when it is appropriate to free the allocated memory.</span></span>

 

 




