---
description: Die ResolveSource-Aktion bestimmt den Speicherort der Quelle und legt die SourceDir-Eigenschaft fest, wenn die Quelle noch nicht aufgelöst wurde.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: ResolveSource-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350056"
---
# <a name="resolvesource-action"></a><span data-ttu-id="6abbb-103">ResolveSource-Aktion</span><span class="sxs-lookup"><span data-stu-id="6abbb-103">ResolveSource Action</span></span>

<span data-ttu-id="6abbb-104">Die ResolveSource-Aktion bestimmt den Speicherort der Quelle und legt die [**SourceDir**](sourcedir.md) -Eigenschaft fest, wenn die Quelle noch nicht aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6abbb-104">The ResolveSource action determines the location of the source and sets the [**SourceDir**](sourcedir.md) property if the source has not been resolved yet.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6abbb-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="6abbb-105">Sequence Restrictions</span></span>

<span data-ttu-id="6abbb-106">Die ResolveSource-Aktion muss nach der [costinitialize-Aktion](costinitialize-action.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="6abbb-106">The ResolveSource action must come after the [CostInitialize action](costinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6abbb-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="6abbb-107">ActionData Messages</span></span>

<span data-ttu-id="6abbb-108">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6abbb-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="6abbb-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6abbb-109">Remarks</span></span>

<span data-ttu-id="6abbb-110">Die ResolveSource-Aktion muss vor der Verwendung der [**SourceDir**](sourcedir.md) -Eigenschaft in einem beliebigen Ausdruck aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6abbb-110">The ResolveSource action must be called before using the [**SourceDir**](sourcedir.md) property in any expression.</span></span> <span data-ttu-id="6abbb-111">Es muss auch aufgerufen werden, bevor versucht wird, den Wert der **SourceDir** -Eigenschaft mithilfe von " [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)" abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6abbb-111">It must also be called before attempting to retrieve the value of the **SourceDir** property using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="6abbb-112">Die ResolveSource-Aktion sollte nicht ausgeführt werden, wenn die Quelle nicht verfügbar ist, da Sie möglicherweise beim Deinstallieren der Anwendung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6abbb-112">The ResolveSource action should not be executed when the source is unavailable, as it may be when uninstalling the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6abbb-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6abbb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6abbb-114">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="6abbb-114">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



