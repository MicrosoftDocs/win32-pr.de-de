---
description: Um zu erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine isolierte Komponenten Beziehung zwischen dem Server und dem Client anzugeben.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Installieren einer nicht-COM-Komponente an einem privaten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868879"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a><span data-ttu-id="70199-103">Installieren einer nicht-COM-Komponente an einem privaten Speicherort</span><span class="sxs-lookup"><span data-stu-id="70199-103">Installing a non-COM Component to a Private Location</span></span>

<span data-ttu-id="70199-104">Um zu erzwingen, dass eine Client Anwendung immer dieselbe Kopie eines nicht-COM-Servers verwendet, erstellen Sie das Installationspaket der Anwendung, um eine [isolierte Komponenten](isolated-components.md) Beziehung zwischen dem Server und dem Client anzugeben.</span><span class="sxs-lookup"><span data-stu-id="70199-104">To force a client application to always use the same copy of a non-COM server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="70199-105">Dadurch wird eine private Kopie der Serverkomponente an einem Speicherort installiert, der ausschließlich von der Client Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70199-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="70199-106">Gehen Sie beim Erstellen des Pakets wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="70199-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="70199-107">Platzieren Sie die Server-DLL und den exe-Client in separaten Komponenten.</span><span class="sxs-lookup"><span data-stu-id="70199-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="70199-108">Geben Sie einen Datensatz in der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) mit der Client Komponente in der \_ Shared-Spalte der Komponente und der Client Anwendung in der Spalte Komponenten Anwendung ein \_ .</span><span class="sxs-lookup"><span data-stu-id="70199-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="70199-109">Schließen Sie die [isolatecomponents-Aktion](isolatecomponents-action.md) in die Sequenz Tabellen ein.</span><span class="sxs-lookup"><span data-stu-id="70199-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="70199-110">Legen Sie das msidbcomponentattributesshareddllrefcount-Bit im [Komponenten Tabellen](component-table.md) Daten Satz für die freigegebene Komponente fest \_ .</span><span class="sxs-lookup"><span data-stu-id="70199-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="70199-111">Das Installationsprogramm erfordert diesen globalen refcount am freigegebenen Speicherort, um die freigegebenen Dateien und die Registrierung in Fällen zu schützen, in denen die Freigabe mit anderen Installationstechnologien erfolgt.</span><span class="sxs-lookup"><span data-stu-id="70199-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>
-   <span data-ttu-id="70199-112">Vermeiden Sie das Erstellen eines gemeinsam genutzten, registrierten Pfads für Komponenten.</span><span class="sxs-lookup"><span data-stu-id="70199-112">Avoid authoring a shared registered path across components.</span></span>

 

 



