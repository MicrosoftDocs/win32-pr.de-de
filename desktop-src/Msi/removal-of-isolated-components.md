---
description: Windows Installer führt beim Entfernen einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält. In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Entfernen isolierter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358596"
---
# <a name="removal-of-isolated-components"></a><span data-ttu-id="339a3-104">Entfernen isolierter Komponenten</span><span class="sxs-lookup"><span data-stu-id="339a3-104">Removal of Isolated Components</span></span>

<span data-ttu-id="339a3-105">Windows Installer führt beim Entfernen einer Anwendung die folgenden Aktionen aus, wenn das Paket isolierte Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="339a3-105">Windows Installer performs the following actions during the removal of an application when the package contains isolated components.</span></span> <span data-ttu-id="339a3-106">In der Regel \_ handelt es sich bei der gemeinsam genutzten Komponente um eine DLL, die von Komponenten \_ Anwendungen und anderen ausführbaren Client Dateien gemeinsam genutzt wird</span><span class="sxs-lookup"><span data-stu-id="339a3-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="uninstall"></a><span data-ttu-id="339a3-107">Deinstallieren</span><span class="sxs-lookup"><span data-stu-id="339a3-107">Uninstall</span></span>

-   <span data-ttu-id="339a3-108">Entfernen Sie die Dateien der Komponente \_ , die aus dem Ordner mit der Komponenten Anwendung freigegeben \_ wurden, nur, wenn die Komponenten \_ Anwendung ebenfalls entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="339a3-108">Remove the files of Component\_Shared from the folder containing Component\_Application only if Component\_Application is also being removed.</span></span>
-   <span data-ttu-id="339a3-109">Wenn das msidbcomponentattributesshareddllrefcount-Bit in der [Komponenten Tabelle](component-table.md) festgelegt ist, wird der SHAREDDLL refcount-Wert verringert.</span><span class="sxs-lookup"><span data-stu-id="339a3-109">If the msidbComponentAttributesSharedDllRefCount bit is set in the [Component table](component-table.md) decrement the SharedDLL refcount.</span></span>
-   <span data-ttu-id="339a3-110">Entfernen Sie. Lokale 0-Byte-Datei aus dem Ordner, der die Komponenten \_ Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="339a3-110">Remove the .LOCAL zero-byte file from the folder containing Component\_Application.</span></span>
-   <span data-ttu-id="339a3-111">Entfernen Sie \_ die Komponenten Anwendung aus der Client Liste der frei \_ gegebenen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="339a3-111">Remove Component\_Application from the client list of Component\_Shared.</span></span>
-   <span data-ttu-id="339a3-112">Entfernen Sie alle Ressourcen der Komponenten \_ Anwendung wie üblich.</span><span class="sxs-lookup"><span data-stu-id="339a3-112">Remove all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="339a3-113">Wenn in der Liste der freigegebenen Komponenten andere Produkte verbleiben \_ :</span><span class="sxs-lookup"><span data-stu-id="339a3-113">If there are other products remaining on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="339a3-114">Entfernen Sie keine Dateien aus dem freigegebenen Speicherort der frei \_ gegebenen Komponente.</span><span class="sxs-lookup"><span data-stu-id="339a3-114">Remove no files from the shared location of Component\_Shared.</span></span>

<span data-ttu-id="339a3-115">Wenn SHAREDDLL refcount für die frei \_ gegebene Komponente 0 ist, nachdem Sie verringert wurde, oder wenn keine anderen verbleibenden Clients der Komponente frei \_ gegeben sind:</span><span class="sxs-lookup"><span data-stu-id="339a3-115">If the SharedDLL refcount for Component\_Shared is 0 after being decremented, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="339a3-116">Entfernen Sie die Dateien der Komponente, die \_ vom freigegebenen Speicherort verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="339a3-116">Remove the files of Component\_Shared from the shared location.</span></span>
-   <span data-ttu-id="339a3-117">Alle Deinstallations Aktionen in Bezug auf diese Komponente verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="339a3-117">Process all uninstall actions with respect to this component.</span></span>

 

 



