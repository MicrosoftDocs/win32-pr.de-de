---
title: Persistente Speicherung auf dem Server
description: Sie können Ihre Anwendung optimieren, damit der Server-Stub beim Abschluss eines Remote Prozedur Aufrufes keinen Arbeitsspeicher auf dem Server freigibt.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947897"
---
# <a name="persistent-storage-on-the-server"></a><span data-ttu-id="7620d-103">Persistente Speicherung auf dem Server</span><span class="sxs-lookup"><span data-stu-id="7620d-103">Persistent Storage on the Server</span></span>

<span data-ttu-id="7620d-104">Sie können Ihre Anwendung optimieren, damit der Server-Stub beim Abschluss eines Remote Prozedur Aufrufes keinen Arbeitsspeicher auf dem Server freigibt.</span><span class="sxs-lookup"><span data-stu-id="7620d-104">You can optimize your application so the server stub does not free memory on the server at the conclusion of a remote procedure call.</span></span> <span data-ttu-id="7620d-105">Wenn ein Kontext Handle z. b. von mehreren Remote Prozeduren bearbeitet wird, können Sie das ACF-Attribut **\[ (nicht \_ frei \] )** verwenden, um den belegten Arbeitsspeicher auf dem Server beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="7620d-105">For example, when a context handle will be manipulated by several remote procedures, you can use the ACF attribute **\[allocate(dont\_free)\]** to retain the allocated memory on the server.</span></span>

<span data-ttu-id="7620d-106">Das Attribut " **\[ zuordnen (nicht \_ frei) \]** " wird der ACF- **typedef** -Deklaration in der ACF hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7620d-106">The **\[allocate(dont\_free)\]** attribute is added to the ACF **typedef** declaration in the ACF.</span></span> <span data-ttu-id="7620d-107">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7620d-107">For example:</span></span>

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

<span data-ttu-id="7620d-108">Wenn das Attribut " **\[ zuordnen (nicht \_ frei) \]** " angegeben ist, wird die Strukturdaten Struktur vom Serverstub zugeordnet, aber nicht freigegeben.</span><span class="sxs-lookup"><span data-stu-id="7620d-108">When the **\[allocate(dont\_free)\]** attribute is specified, the tree data structure is allocated, but not freed, by the server stub.</span></span> <span data-ttu-id="7620d-109">Wenn Sie die Zeiger auf solche permanenten Datenbereiche, die für andere Routinen verfügbar sind, – z. b. durch Kopieren der Zeiger auf globale Variablen –, sind die beibehaltenen Daten für andere Serverfunktionen zugänglich.</span><span class="sxs-lookup"><span data-stu-id="7620d-109">When you make the pointers to such persistent data areas available to other routines—for example, by copying the pointers to global variables—the retained data is accessible to other server functions.</span></span> <span data-ttu-id="7620d-110">Das Attribut " **\[ zuordnen" (nicht \_ frei) \]** ist besonders nützlich für die Beibehaltung von permanenten Zeiger Strukturen als Teil der Server Zustandsinformationen, die einem Kontext Handle-Typ zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7620d-110">The **\[allocate(dont\_free)\]** attribute is particularly useful for maintaining persistent pointer structures as part of the server state information associated with a context-handle type.</span></span>

 

 




