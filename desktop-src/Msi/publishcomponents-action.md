---
description: Die PublishComponents-Aktion verwaltet die Ankündigung der Komponenten aus der PublishComponent-Tabelle.
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: PublishComponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c8967e737193922a9dbc3d9e03bc95131d5a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864852"
---
# <a name="publishcomponents-action"></a><span data-ttu-id="fd812-103">PublishComponents-Aktion</span><span class="sxs-lookup"><span data-stu-id="fd812-103">PublishComponents Action</span></span>

<span data-ttu-id="fd812-104">Die PublishComponents-Aktion verwaltet die Ankündigung der Komponenten aus der [PublishComponent](publishcomponent-table.md) -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd812-104">The PublishComponents action manages the advertisement of the components from the [PublishComponent](publishcomponent-table.md) table.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="fd812-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="fd812-105">Sequence Restrictions</span></span>

<span data-ttu-id="fd812-106">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="fd812-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="fd812-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="fd812-107">ActionData Messages</span></span>



| <span data-ttu-id="fd812-108">Feld</span><span class="sxs-lookup"><span data-stu-id="fd812-108">Field</span></span> | <span data-ttu-id="fd812-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="fd812-109">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="fd812-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fd812-110">\[1\]</span></span> | <span data-ttu-id="fd812-111">GUID, die die Komponenten-ID eines angekündigten Features darstellt.</span><span class="sxs-lookup"><span data-stu-id="fd812-111">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="fd812-112">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fd812-112">\[2\]</span></span> | <span data-ttu-id="fd812-113">Qualifizierer der Komponenten-ID.</span><span class="sxs-lookup"><span data-stu-id="fd812-113">Qualifier of component ID.</span></span>                                   |



 

## <a name="remarks"></a><span data-ttu-id="fd812-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd812-114">Remarks</span></span>

<span data-ttu-id="fd812-115">Mit der Aktion PublishComponents werden alle Komponenten aus der Tabelle PublishComponents veröffentlicht, die zu den Funktionen gehören, die für die Ankündigung oder Installation ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="fd812-115">The PublishComponents action publishes all of the components from the PublishComponents table that belong to features that have been selected for advertisement or installation.</span></span>

 

 



