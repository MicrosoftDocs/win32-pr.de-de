---
title: Die named_type_to_local-Funktion
description: Die Stubdateien nennen den benannten \_ Typ \_ an die \_ lokale Funktion, um Daten von einem übertragenen Typ in den Typ zu konvertieren, den Sie für die Anwendung enthalten.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036961"
---
# <a name="the-named_type_to_local-function"></a><span data-ttu-id="09a3d-104">Der benannte \_ Typ \_ der \_ lokalen Funktion.</span><span class="sxs-lookup"><span data-stu-id="09a3d-104">The named\_type\_to\_local Function</span></span>

<span data-ttu-id="09a3d-105">Die Stubdateien nennen den **benannten \_ Typ an die \_ \_ lokale** Funktion, um Daten von einem übertragenen Typ in den Typ zu konvertieren, den Sie für die Anwendung enthalten.</span><span class="sxs-lookup"><span data-stu-id="09a3d-105">The stubs call the **named\_type\_to\_local** function to convert data from a transmitted type to the type that they present to the application.</span></span> <span data-ttu-id="09a3d-106">Die-Funktion ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="09a3d-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

<span data-ttu-id="09a3d-107">Der erste Parameter verweist auf die übertragenen Daten.</span><span class="sxs-lookup"><span data-stu-id="09a3d-107">The first parameter points to the transmitted data.</span></span> <span data-ttu-id="09a3d-108">Die-Funktion legt den zweiten Parameter fest, um auf die dargestellten Daten zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="09a3d-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="09a3d-109">Der **benannte \_ Typ \_ der \_ lokalen** Funktion muss den Arbeitsspeicher für den dargestellten Typ verwalten.</span><span class="sxs-lookup"><span data-stu-id="09a3d-109">The **named\_type\_to\_local** function must manage memory for the presented type.</span></span> <span data-ttu-id="09a3d-110">Die-Funktion muss für die gesamte Datenstruktur, die bei der durch den zweiten Parameter angegebenen Adresse beginnt, Arbeitsspeicher zuweisen, mit Ausnahme des-Parameters selbst (der Stub weist Speicher für den Stamm Knoten zu und übergibt ihn an die-Funktion).</span><span class="sxs-lookup"><span data-stu-id="09a3d-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="09a3d-111">Der Wert des zweiten Parameters kann während des Aufrufes nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="09a3d-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="09a3d-112">Die Funktion kann den Inhalt an dieser Adresse ändern.</span><span class="sxs-lookup"><span data-stu-id="09a3d-112">The function can change the contents at that address.</span></span>

 

 




