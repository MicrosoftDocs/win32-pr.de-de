---
title: Binden an ein ADSI-Objekt
description: Das Herstellen einer Verbindung mit einem Objekt in einem Verzeichnisdienst wird als Bindung bezeichnet.
ms.assetid: f3963019-9b3a-42d5-a978-484f294110e5
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0fefcdb62d374d98e3007864168e2626ecc5d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707475"
---
# <a name="binding-to-an-adsi-object"></a><span data-ttu-id="099aa-104">Binden an ein ADSI-Objekt</span><span class="sxs-lookup"><span data-stu-id="099aa-104">Binding to an ADSI Object</span></span>

<span data-ttu-id="099aa-105">Das Herstellen einer Verbindung mit einem Objekt in einem Verzeichnisdienst wird als Bindung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="099aa-105">Connecting to an object in a directory service is known as binding.</span></span> <span data-ttu-id="099aa-106">Die Bindung an ein ADSI-Objekt ist der erste Schritt bei der Kommunikation mit dem zugrunde liegenden Verzeichnis System.</span><span class="sxs-lookup"><span data-stu-id="099aa-106">Binding to an ADSI object is the first step to communicating with the underlying directory system.</span></span> <span data-ttu-id="099aa-107">Ein Objekt muss an gebunden werden, um in seinem Namespace zu navigieren, nach Daten zu suchen, Daten zu ändern oder die Identität eines Benutzers anzunehmen.</span><span class="sxs-lookup"><span data-stu-id="099aa-107">An object must be bound to in order to navigate its namespace, search for data, modify data, or impersonate a user.</span></span> <span data-ttu-id="099aa-108">Es ist auch möglich, zusätzliche Bindungs Merkmale wie Benutzername, Kennwort, Servername, Verschlüsselungsmethoden und gesicherte Authentifizierung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="099aa-108">It is also possible to supply additional binding characteristics, such as user name, password, server name, encryption methods, and secured authentication.</span></span> <span data-ttu-id="099aa-109">Die tatsächlichen zusätzlichen Bindungseigenschaften, die verwendet werden können, hängen vom Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="099aa-109">The actual additional binding characteristics that can be used will depend on the provider.</span></span>

<span data-ttu-id="099aa-110">Weitere Informationen zur ADSI-Bindung finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="099aa-110">For more information about ADSI binding, see:</span></span>

-   [<span data-ttu-id="099aa-111">Bindungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="099aa-111">Binding String</span></span>](binding-string.md)
-   [<span data-ttu-id="099aa-112">Spezifische Bindungs Typen für Active Directory</span><span class="sxs-lookup"><span data-stu-id="099aa-112">Binding Types Specific to Active Directory</span></span>](binding-types-specific-to-active-directory.md)
-   [<span data-ttu-id="099aa-113">Bindungsprobleme für gemischte Umgebungen</span><span class="sxs-lookup"><span data-stu-id="099aa-113">Binding Issues for Mixed Environments</span></span>](binding-issues-for-mixed-environments.md)
-   [<span data-ttu-id="099aa-114">Programm gesteuertes binden mithilfe einer ADSI-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="099aa-114">Binding Programmatically Using an ADSI Interface</span></span>](binding-programmatically-using-an-adsi-interface.md)
-   [<span data-ttu-id="099aa-115">Zwischenspeichern von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="099aa-115">Connection Caching</span></span>](connection-caching.md)
-   [<span data-ttu-id="099aa-116">Binden an untergeordnete Objekte</span><span class="sxs-lookup"><span data-stu-id="099aa-116">Binding to Child Objects</span></span>](binding-to-child-objects.md)
-   [<span data-ttu-id="099aa-117">Binden an das übergeordnete Element eines Objekts</span><span class="sxs-lookup"><span data-stu-id="099aa-117">Binding to an Object's Parent</span></span>](binding-to-an-objectampaposs-parent.md)
-   [<span data-ttu-id="099aa-118">Fast Binding-Option für Batch Schreib-/Änderungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="099aa-118">Fast Binding Option for Batch Write/Modify Operations</span></span>](fast-binding-option-for-batch-writemodify-operations.md)
-   [<span data-ttu-id="099aa-119">Auswählen einer Schnittstelle für die Bindung</span><span class="sxs-lookup"><span data-stu-id="099aa-119">Choosing an Interface for Binding</span></span>](choosing-an-interface.md)

 

 




