---
description: Die processcomponents-Aktion registriert und hebt die Registrierung von Komponenten, Ihren Schlüssel Pfaden und den Komponenten Clients auf.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Processcomponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363654"
---
# <a name="processcomponents-action"></a><span data-ttu-id="5830a-103">Processcomponents-Aktion</span><span class="sxs-lookup"><span data-stu-id="5830a-103">ProcessComponents Action</span></span>

<span data-ttu-id="5830a-104">Die processcomponents-Aktion registriert und hebt die Registrierung von Komponenten, Ihren Schlüssel Pfaden und den Komponenten Clients auf.</span><span class="sxs-lookup"><span data-stu-id="5830a-104">The ProcessComponents action registers and unregisters components, their key paths, and the component clients.</span></span> <span data-ttu-id="5830a-105">Mit der processcomponents-Aktion wird die KEYPATH-Spalte der [Component-Tabelle](component-table.md) abgefragt, um KEYPATH zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5830a-105">The ProcessComponents action queries the KeyPath column of the [Component table](component-table.md) to determine keypaths.</span></span> <span data-ttu-id="5830a-106">Diese Registrierung wird von [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) verwendet, um den Pfad einer Komponente für einen Produkt Client zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="5830a-106">This registration is used by [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to return the path of a component for a product client.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5830a-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="5830a-107">Sequence Restrictions</span></span>

<span data-ttu-id="5830a-108">Die Aktion processcomponents muss nach der [InstallInitialize](installinitialize-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="5830a-108">The ProcessComponents action must come after the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5830a-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="5830a-109">ActionData Messages</span></span>

<span data-ttu-id="5830a-110">Für jede Komponente, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="5830a-110">For each component being registered.</span></span>



| <span data-ttu-id="5830a-111">Feld</span><span class="sxs-lookup"><span data-stu-id="5830a-111">Field</span></span> | <span data-ttu-id="5830a-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="5830a-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="5830a-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5830a-113">\[1\]</span></span> | <span data-ttu-id="5830a-114">ProductId</span><span class="sxs-lookup"><span data-stu-id="5830a-114">ProductId</span></span>                       |
| <span data-ttu-id="5830a-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5830a-115">\[2\]</span></span> | <span data-ttu-id="5830a-116">ComponentID</span><span class="sxs-lookup"><span data-stu-id="5830a-116">ComponentId</span></span>                     |
| <span data-ttu-id="5830a-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="5830a-117">\[3\]</span></span> | <span data-ttu-id="5830a-118">Der Schlüssel Pfad für die Komponente.</span><span class="sxs-lookup"><span data-stu-id="5830a-118">The key path for the component.</span></span> |



 

<span data-ttu-id="5830a-119">Für jede Komponente, deren Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="5830a-119">For each component being unregistered.</span></span>



| <span data-ttu-id="5830a-120">Feld</span><span class="sxs-lookup"><span data-stu-id="5830a-120">Field</span></span> | <span data-ttu-id="5830a-121">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="5830a-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="5830a-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5830a-122">\[1\]</span></span> | <span data-ttu-id="5830a-123">ProductId</span><span class="sxs-lookup"><span data-stu-id="5830a-123">ProductId</span></span>                  |
| <span data-ttu-id="5830a-124">\[2\]</span><span class="sxs-lookup"><span data-stu-id="5830a-124">\[2\]</span></span> | <span data-ttu-id="5830a-125">ComponentID</span><span class="sxs-lookup"><span data-stu-id="5830a-125">ComponentId</span></span>                |



 

 

 



