---
description: Ein eingebettetes Objekt ist ein Objekt einer Klasse, das in einer Klassen-oder Instanzdeklaration einer anderen Klasse vorhanden ist.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Einbetten von Objekten in eine Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362853"
---
# <a name="embedding-objects-in-a-class"></a><span data-ttu-id="4dd9b-103">Einbetten von Objekten in eine Klasse</span><span class="sxs-lookup"><span data-stu-id="4dd9b-103">Embedding Objects in a Class</span></span>

<span data-ttu-id="4dd9b-104">Ein eingebettetes Objekt ist ein Objekt einer Klasse, das in einer Klassen-oder Instanzdeklaration einer anderen Klasse vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-104">An embedded object is an object of a class that exists within a class or instance declaration of another class.</span></span> <span data-ttu-id="4dd9b-105">Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse enthält z. b. Win32-Vertrauens nehmer eingebettete Objekte. [**\_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)</span><span class="sxs-lookup"><span data-stu-id="4dd9b-105">For example, the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class contains [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded objects.</span></span> <span data-ttu-id="4dd9b-106">Jedes der **Win32- \_ Treuhänder** -Objekte enthält ein [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-106">Each of the **Win32\_Trustee** objects contains a [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object.</span></span> <span data-ttu-id="4dd9b-107">Die Tiefe, in der eine Klasse über eingebettete Objekte verfügen kann, wird von WMI nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-107">WMI does not limit the depth to which a class can have embedded objects.</span></span> <span data-ttu-id="4dd9b-108">Die Verwendung eines anderen Entwurfs, z. b. das Erstellen einer Zuordnungs Klasse, kann jedoch zu einem besser verwaltbaren Schema führen.</span><span class="sxs-lookup"><span data-stu-id="4dd9b-108">However, using another design, such as creating an association class, may make a more manageable schema.</span></span>

<span data-ttu-id="4dd9b-109">Weitere Informationen zu eingebetteten Objekten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4dd9b-109">For more information about embedded objects, see the following topics:</span></span>

-   [<span data-ttu-id="4dd9b-110">Erstellen von eingebetteten Objekten</span><span class="sxs-lookup"><span data-stu-id="4dd9b-110">Creating Embedded Objects</span></span>](creating-embedded-objects.md)
-   [<span data-ttu-id="4dd9b-111">Abfragen von eingebetteten Objekten</span><span class="sxs-lookup"><span data-stu-id="4dd9b-111">Querying Embedded Objects</span></span>](querying-embedded-objects.md)

## <a name="related-topics"></a><span data-ttu-id="4dd9b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4dd9b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd9b-113">Entwerfen von Managed Object Format-Klassen (MOF)</span><span class="sxs-lookup"><span data-stu-id="4dd9b-113">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
