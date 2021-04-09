---
description: Die unregistercomplus-Aktion entfernt com+-Anwendungen aus der Registrierung.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Unregistercomplus-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960918"
---
# <a name="unregistercomplus-action"></a><span data-ttu-id="1cac5-103">Unregistercomplus-Aktion</span><span class="sxs-lookup"><span data-stu-id="1cac5-103">UnregisterComPlus Action</span></span>

<span data-ttu-id="1cac5-104">Die unregistercomplus-Aktion entfernt com+-Anwendungen aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="1cac5-104">The UnregisterComPlus action removes COM+ applications from the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1cac5-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="1cac5-105">Sequence Restrictions</span></span>

<span data-ttu-id="1cac5-106">Die Aktion [registercomplus](registercomplus-action.md) muss der Aktion [InstallFiles](installfiles-action.md) und der unregistercomplus-Aktion folgen.</span><span class="sxs-lookup"><span data-stu-id="1cac5-106">The [RegisterComPlus action](registercomplus-action.md) must follow the [InstallFiles action](installfiles-action.md) and the UnregisterComPlus action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1cac5-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="1cac5-107">ActionData Messages</span></span>



| <span data-ttu-id="1cac5-108">Feld</span><span class="sxs-lookup"><span data-stu-id="1cac5-108">Field</span></span> | <span data-ttu-id="1cac5-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="1cac5-109">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="1cac5-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1cac5-110">\[1\]</span></span> | <span data-ttu-id="1cac5-111">Anwendungs Bezeichner der zu entfernenden com+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="1cac5-111">Application identifier of the COM+ application being removed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1cac5-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1cac5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cac5-113">Registercomplus-Aktion</span><span class="sxs-lookup"><span data-stu-id="1cac5-113">RegisterComPlus action</span></span>](registercomplus-action.md)
</dt> <dt>

[<span data-ttu-id="1cac5-114">ComPlus-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1cac5-114">Complus table</span></span>](complus-table.md)
</dt> <dt>

[<span data-ttu-id="1cac5-115">Installieren einer COM+-Anwendung mit der Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1cac5-115">Installing a COM+ Application with the Windows Installer</span></span>](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



