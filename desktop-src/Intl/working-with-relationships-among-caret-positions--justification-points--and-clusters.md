---
description: In der folgenden Tabelle werden die verschiedenen Methoden angezeigt, mit denen die Anwendung die Einfügemarke, die Begründung und die Cluster verarbeiten kann.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Arbeiten mit Beziehungen zwischen Einfügepositionen, Ausrichtungspunkten und Clustern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368092"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a><span data-ttu-id="b89fe-103">Arbeiten mit Beziehungen zwischen Einfügepositionen, Ausrichtungspunkten und Clustern</span><span class="sxs-lookup"><span data-stu-id="b89fe-103">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>

<span data-ttu-id="b89fe-104">In der folgenden Tabelle werden die verschiedenen Methoden angezeigt, mit denen die Anwendung die Einfügemarke, die Begründung und die Cluster verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b89fe-104">The following table shows the various methods that the application can use to handle the caret, justification, and clusters.</span></span>



| <span data-ttu-id="b89fe-105">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="b89fe-105">Task</span></span>                             | <span data-ttu-id="b89fe-106">Uniscriunterstützung</span><span class="sxs-lookup"><span data-stu-id="b89fe-106">Uniscribe support</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b89fe-107">Caretzeichen nach Zeichen Cluster verschieben</span><span class="sxs-lookup"><span data-stu-id="b89fe-107">Caret move by character cluster</span></span>  | <span data-ttu-id="b89fe-108">Der *pwlogclust* -Parameter von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionthe **fclusterstart** -Member der Skript-Struktur " [**\_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) "</span><span class="sxs-lookup"><span data-stu-id="b89fe-108">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="b89fe-109">Das **fcharstopmember** der [**Skript- \_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b89fe-109">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="b89fe-110">Zeilenumbruch zwischen Zeichen</span><span class="sxs-lookup"><span data-stu-id="b89fe-110">Line breaking between characters</span></span> | <span data-ttu-id="b89fe-111">Der *pwlogclust* -Parameter von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionthe **fclusterstart** -Member der Skript-Struktur " [**\_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) "</span><span class="sxs-lookup"><span data-stu-id="b89fe-111">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="b89fe-112">Das **fcharstopmember** der [**Skript- \_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b89fe-112">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="b89fe-113">Caretzeichen nach Wort verschieben</span><span class="sxs-lookup"><span data-stu-id="b89fe-113">Caret move by word</span></span>               | <span data-ttu-id="b89fe-114">Der **fwordstoppt** -Member der [**\_ logattr-Skript**](/windows/win32/api/usp10/ns-usp10-script_logattr) Struktur</span><span class="sxs-lookup"><span data-stu-id="b89fe-114">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="b89fe-115">Zeilenumbruch zwischen Wörtern</span><span class="sxs-lookup"><span data-stu-id="b89fe-115">Line breaking between words</span></span>      | <span data-ttu-id="b89fe-116">Der **fwordstoppt** -Member der [**\_ logattr-Skript**](/windows/win32/api/usp10/ns-usp10-script_logattr) Struktur</span><span class="sxs-lookup"><span data-stu-id="b89fe-116">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="b89fe-117">Begründung</span><span class="sxs-lookup"><span data-stu-id="b89fe-117">Justification</span></span>                    | <span data-ttu-id="b89fe-118">Der Benutzer **definierte Member der** Skript- [**\_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b89fe-118">The **uJustification** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="b89fe-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b89fe-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b89fe-120">Verwenden von uniscri</span><span class="sxs-lookup"><span data-stu-id="b89fe-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




