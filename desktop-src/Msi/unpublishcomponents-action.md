---
description: Mit der unpublishcomponents-Aktion wird die nicht Ankündigung der in der Tabelle PublishComponent aufgeführten Komponenten verwaltet.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Unpublishcomponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104394038"
---
# <a name="unpublishcomponents-action"></a><span data-ttu-id="e01e0-103">Unpublishcomponents-Aktion</span><span class="sxs-lookup"><span data-stu-id="e01e0-103">UnpublishComponents Action</span></span>

<span data-ttu-id="e01e0-104">Mit der unpublishcomponents-Aktion wird die nicht Ankündigung der in der Tabelle PublishComponent aufgeführten Komponenten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e01e0-104">The UnpublishComponents action manages the unadvertisement of components listed in the PublishComponent table.</span></span> <span data-ttu-id="e01e0-105">Dabei handelt es sich um Komponenten, bei denen möglicherweise von anderen Produkten ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e01e0-105">These are components that may be faulted in by other products.</span></span> <span data-ttu-id="e01e0-106">Diese Aktion entfernt Informationen zu veröffentlichten Komponenten aus der [PublishComponent-Tabelle](publishcomponent-table.md) , für die die entsprechende Funktion zurzeit für die Deinstallation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="e01e0-106">This action removes information about published components from the [PublishComponent table](publishcomponent-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e01e0-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e01e0-107">Sequence Restrictions</span></span>

<span data-ttu-id="e01e0-108">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="e01e0-108">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e01e0-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="e01e0-109">ActionData Messages</span></span>



| <span data-ttu-id="e01e0-110">Feld</span><span class="sxs-lookup"><span data-stu-id="e01e0-110">Field</span></span> | <span data-ttu-id="e01e0-111">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="e01e0-111">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="e01e0-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e01e0-112">\[1\]</span></span> | <span data-ttu-id="e01e0-113">GUID, die die Komponenten-ID eines angekündigten Features darstellt.</span><span class="sxs-lookup"><span data-stu-id="e01e0-113">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="e01e0-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="e01e0-114">\[2\]</span></span> | <span data-ttu-id="e01e0-115">Qualifizierer der Komponenten-ID.</span><span class="sxs-lookup"><span data-stu-id="e01e0-115">Qualifier of the component ID.</span></span>                               |



 

