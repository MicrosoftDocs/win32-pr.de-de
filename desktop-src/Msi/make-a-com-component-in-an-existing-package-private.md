---
description: Ein Administrator kann erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers in einem vorhandenen Paket&8212, ohne dass sich dies auf \# andere Anwendungen auswirkt&\# 8212; durch Angeben einer isolierten Komponenten Beziehung zwischen dem com-Server und dem Client.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Erstellen einer COM-Komponente in einem vorhandenen Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363303"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a><span data-ttu-id="bae28-103">Erstellen einer COM-Komponente in einem vorhandenen Paket</span><span class="sxs-lookup"><span data-stu-id="bae28-103">Make a COM Component in an Existing Package Private</span></span>

<span data-ttu-id="bae28-104">Ein Administrator kann erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers in einem vorhandenen Paket verwendet – ohne dass sich dies auf andere Anwendungen auswirkt – indem eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem com-Server und dem Client angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bae28-104">An administrator can force a COM-client application to always use the same copy of a COM-server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="bae28-105">Dadurch wird eine private Kopie der com-Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bae28-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="bae28-106">Der-Administrator muss mit Transformationen oder einem Paket Erstellungs Tool wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="bae28-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="bae28-107">Platzieren Sie die com-Server-DLL und den exe-Client in separaten Komponenten.</span><span class="sxs-lookup"><span data-stu-id="bae28-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="bae28-108">Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der com-Client-Komponente in der frei \_ gegebenen Komponenten Spalte und der Client Anwendung in der \_ Spalte Komponenten Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="bae28-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="bae28-109">Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.</span><span class="sxs-lookup"><span data-stu-id="bae28-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="bae28-110">Legen Sie das **msidbcomponentattributesshareddllrefcount** -Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ .</span><span class="sxs-lookup"><span data-stu-id="bae28-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="bae28-111">Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.</span><span class="sxs-lookup"><span data-stu-id="bae28-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



