---
title: Unterstützung für Abfragen
description: Durch Implementieren der idirector ysearch-Schnittstelle erhalten ADSI-Anbieter Zugriff auf eine Teilmenge OLE DB schreibgeschützten Features.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Unterstützung für Abfragen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337751"
---
# <a name="support-for-queries"></a><span data-ttu-id="e2bb7-104">Unterstützung für Abfragen</span><span class="sxs-lookup"><span data-stu-id="e2bb7-104">Support for Queries</span></span>

<span data-ttu-id="e2bb7-105">Durch Implementieren der [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle erhalten ADSI-Anbieter Zugriff auf eine Teilmenge OLE DB schreibgeschützten Features.</span><span class="sxs-lookup"><span data-stu-id="e2bb7-105">By implementing the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, ADSI providers gain access to a subset of OLE DB read-only features.</span></span>

<span data-ttu-id="e2bb7-106">Die ADSI-Implementierung der Methoden von [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) selbst verwendet die in ADSI Version 1,0 beschriebenen OLE DB Schnittstellen, einschließlich der folgenden COM-Objekte:</span><span class="sxs-lookup"><span data-stu-id="e2bb7-106">The ADSI implementation of the methods of [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) itself uses the OLE DB interfaces described in ADSI Version 1.0, including the following list of COM objects:</span></span>

-   <span data-ttu-id="e2bb7-107">Datenquellen Objekt (Verzeichnisdienst), Unterstützung für **IDBInitialize**, **idbkreatesession**, **IDBProperties** und **ipersistent**.</span><span class="sxs-lookup"><span data-stu-id="e2bb7-107">Data Source Object (the directory service), supporting **IDBInitialize**, **IDBCreateSession**, **IDBProperties**, and **IPersist**.</span></span>
-   <span data-ttu-id="e2bb7-108">Dbsessions-Objekt, Unterstützung für **IOpenRowset**, **ISessionProperties** und **ikreatecommand**.</span><span class="sxs-lookup"><span data-stu-id="e2bb7-108">DBSessions Object, supporting **IOpenRowSet**, **ISessionProperties**, and **ICreateCommand**.</span></span>
-   <span data-ttu-id="e2bb7-109">Command-Objekt, Unterstützung für **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** und **IConvertType**.</span><span class="sxs-lookup"><span data-stu-id="e2bb7-109">Command Object, supporting **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText**, and **IConvertType**.</span></span>
-   <span data-ttu-id="e2bb7-110">Rowset-Objekt, unterstützender **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** und **IRowsetInfo**.</span><span class="sxs-lookup"><span data-stu-id="e2bb7-110">Rowset Object, supporting **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset**, and **IRowsetInfo**.</span></span>

<span data-ttu-id="e2bb7-111">Weitere Informationen zu OLE DB finden Sie in der OLE DB Programmierer-Referenz im Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e2bb7-111">For more information about OLE DB, see the OLE DB Programmer's Reference in the Platform Software Development Kit (SDK).</span></span>

 

 




