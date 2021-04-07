---
description: Um zu erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine isolierte Komponenten Beziehung zwischen dem com-Server und dem Client anzugeben.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Installieren einer COM-Komponente an einem privaten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863283"
---
# <a name="installing-a-com-component-to-a-private-location"></a><span data-ttu-id="34636-103">Installieren einer COM-Komponente an einem privaten Speicherort</span><span class="sxs-lookup"><span data-stu-id="34636-103">Installing a COM Component to a Private Location</span></span>

<span data-ttu-id="34636-104">Um zu erzwingen, dass eine com-Client Anwendung immer dieselbe Kopie eines COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem com-Server und dem Client anzugeben.</span><span class="sxs-lookup"><span data-stu-id="34636-104">To force a COM-client application to always use the same copy of a COM-server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="34636-105">Dadurch wird eine private Kopie der com-Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34636-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="34636-106">Gehen Sie beim Erstellen des Pakets wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="34636-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="34636-107">Platzieren Sie die com-Server-DLL und den exe-Client in separaten Komponenten.</span><span class="sxs-lookup"><span data-stu-id="34636-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="34636-108">Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der com-Client-Komponente in der frei \_ gegebenen Komponenten Spalte und der Client Anwendung in der \_ Spalte Komponenten Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="34636-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="34636-109">Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.</span><span class="sxs-lookup"><span data-stu-id="34636-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="34636-110">Legen Sie das msidbcomponentattributesshareddllrefcount-Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ .</span><span class="sxs-lookup"><span data-stu-id="34636-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="34636-111">Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.</span><span class="sxs-lookup"><span data-stu-id="34636-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



