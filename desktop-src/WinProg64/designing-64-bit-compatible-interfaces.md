---
title: Entwerfen von 64-Bit-kompatiblen Schnittstellen
description: Abwärts Kompatibilitätsprobleme treten auf, wenn Sie einer Schnittstelle neue Datentypen oder Methoden hinzufügen, alte Datentypen ändern oder Datentypen nicht ordnungsgemäß verwenden.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- Abwärtskompatibilität 64-Bit-Windows-Programmierung
- 64-Bit-kompatible Schnittstellen 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Kompatibilität
- Kompatibilität 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309947"
---
# <a name="designing-64-bit-compatible-interfaces"></a><span data-ttu-id="3c092-107">Entwerfen von 64-Bit-kompatiblen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3c092-107">Designing 64-bit-Compatible Interfaces</span></span>

<span data-ttu-id="3c092-108">Das Portieren von 32-Bit-Fenstern auf 64-Bit-Windows sollte keinerlei Probleme für verteilte Anwendungen verursachen, egal ob Sie Remote Prozedur Aufrufe (RPC) direkt oder über DCOM verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c092-108">Porting from 32-bit Windows to 64-bit Windows should not, by itself, create any problems for distributed applications, whether they use Remote Procedure Calls (RPC) directly or through DCOM.</span></span> <span data-ttu-id="3c092-109">Das RPC-Programmiermodell gibt wohl definierte Datengrößen und ganzzahlige Typen an, die an jedem Ende der Verbindung dieselbe Größe haben.</span><span class="sxs-lookup"><span data-stu-id="3c092-109">The RPC programming model specifies well-defined data sizes and integer types that are the same size on each end of the connection.</span></span> <span data-ttu-id="3c092-110">Außerdem werden im LLP64 Abstract Data Model, das für 64-Bit-Windows entwickelt wurde, nur die Zeiger auf 64 Bits erweitert – alle anderen ganzzahligen Datentypen bleiben 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="3c092-110">Also, in the LLP64 abstract data model developed for 64-bit Windows, only the pointers expand to 64 bits—all other integer data types remain 32 bits.</span></span> <span data-ttu-id="3c092-111">Da Zeiger für jede Seite der Client/Server-Verbindung lokal sind und normalerweise als **null** -Marker oder nicht-**null** -Marker übertragen werden, kann das marshallingmodul verschiedene Zeiger Größen an jedem Ende einer Verbindung transparent verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3c092-111">Because pointers are local to each side of the client/server connection and are usually transmitted as **NULL** or non-**NULL** markers, the marshaling engine can handle different pointer sizes on either end of a connection transparently.</span></span>

<span data-ttu-id="3c092-112">Es treten jedoch abwärts Kompatibilitätsprobleme auf, wenn Sie einer Schnittstelle neue Datentypen oder Methoden hinzufügen, alte Datentypen ändern oder Datentypen nicht ordnungsgemäß verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c092-112">However, backward compatibility issues arise when you add new data types or methods to an interface, change old data types, or use data types inappropriately.</span></span> <span data-ttu-id="3c092-113">In den folgenden Themen wird erläutert, wie Sie diese Situationen vermeiden können (sofern möglich) und wie Sie robuste Problem Umgehungen entwerfen können, wenn es nicht möglich ist, Sie zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3c092-113">The following topics discuss how to avoid these situations (when possible) and how to design robust workarounds when it is not possible to avoid them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3c092-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3c092-114">In this Section</span></span>

-   [<span data-ttu-id="3c092-115">Ändern einer vorhandenen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3c092-115">Changing an Existing Interface</span></span>](changing-an-existing-interface.md)
-   [<span data-ttu-id="3c092-116">Vermeiden von Informationen ausblenden</span><span class="sxs-lookup"><span data-stu-id="3c092-116">Avoiding Information Hiding</span></span>](avoiding-information-hiding.md)
-   [<span data-ttu-id="3c092-117">Vermeiden von Polymorphie</span><span class="sxs-lookup"><span data-stu-id="3c092-117">Avoiding Polymorphism</span></span>](avoiding-polymorphism.md)
-   [<span data-ttu-id="3c092-118">Verwenden neuer Datentypen in ihrer IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="3c092-118">Using New Data Types in Your IDL File</span></span>](using-new-data-types-in-your-idl-file.md)
-   [<span data-ttu-id="3c092-119">Vorbereiten der Anwendung für 64-Bit-Windows</span><span class="sxs-lookup"><span data-stu-id="3c092-119">Preparing Your Application for 64-bit Windows</span></span>](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a><span data-ttu-id="3c092-120">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="3c092-120">Related Sections</span></span>

<span data-ttu-id="3c092-121">Wenn Sie noch nicht mit den neuen Datentypen, der Arbeitsumgebung und den API-Änderungen für 64-Bit-Windows vertraut sind, finden Sie weitere Informationen unter [vorbereiten für 64-Bit-Windows](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="3c092-121">If you are not already familiar with the new data types, working environment, and API changes for 64-bit Windows, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

 

 




