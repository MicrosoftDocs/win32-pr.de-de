---
description: Ein Administrator kann erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers in einem vorhandenen Paket&8212, ohne dass sich dies auf \# andere Anwendungen auswirkt&\# 8212; durch Angeben einer isolierten Komponenten Beziehung zwischen dem Server und dem Client.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Erstellen einer nicht-COM-Komponente in einem vorhandenen Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343727"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a><span data-ttu-id="8a94d-103">Erstellen einer nicht-COM-Komponente in einem vorhandenen Paket</span><span class="sxs-lookup"><span data-stu-id="8a94d-103">Make a non-COM Component in an Existing Package Private</span></span>

<span data-ttu-id="8a94d-104">Ein Administrator kann erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers in einem vorhandenen Paket verwendet – ohne Auswirkungen auf andere Anwendungen – indem eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem Server und dem Client angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8a94d-104">An administrator can force a client application to always use the same copy of a non-COM server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="8a94d-105">Dadurch wird eine private Kopie der Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a94d-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="8a94d-106">Der-Administrator muss mit Transformationen oder einem Paket Erstellungs Tool wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="8a94d-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="8a94d-107">Platzieren Sie die Server-DLL und den exe-Client in separaten Komponenten.</span><span class="sxs-lookup"><span data-stu-id="8a94d-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="8a94d-108">Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der Client Komponente in der \_ Shared-Spalte der Komponente und der Client Anwendung in der Spalte Komponenten Anwendung ein \_ .</span><span class="sxs-lookup"><span data-stu-id="8a94d-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="8a94d-109">Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.</span><span class="sxs-lookup"><span data-stu-id="8a94d-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="8a94d-110">Legen Sie das **msidbcomponentattributesshareddllrefcount** -Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ .</span><span class="sxs-lookup"><span data-stu-id="8a94d-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="8a94d-111">Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.</span><span class="sxs-lookup"><span data-stu-id="8a94d-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



