---
description: ICE09 überprüft, ob das permanente Bit für jede für die Installation markierte Komponente im Systemordner festgelegt ist.
ms.assetid: b4e11d75-4214-49de-ac12-6f360771ad73
title: ICE09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01cd20a1b354888877be0f5d456b6d6af2bdec82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757632"
---
# <a name="ice09"></a><span data-ttu-id="ac14c-103">ICE09</span><span class="sxs-lookup"><span data-stu-id="ac14c-103">ICE09</span></span>

<span data-ttu-id="ac14c-104">ICE09 überprüft, ob das permanente Bit für jede für die Installation markierte Komponente im Systemordner festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac14c-104">ICE09 validates that the permanent bit is set for every component marked for installation into the SystemFolder.</span></span> <span data-ttu-id="ac14c-105">ICE09 gibt eine Warnung aus, da Sie vermeiden sollten, nicht permanente Systemkomponenten im Systemordner zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ac14c-105">ICE09 posts a warning because you should avoid installing non-permanent system components to the SystemFolder.</span></span> <span data-ttu-id="ac14c-106">Wenn Sie diese Warnung vermeiden möchten, legen Sie das permanente Bit in der Spalte Attribute der [Komponenten Tabelle](component-table.md) für jede Komponente fest, die für die Installation im Systemordner markiert ist.</span><span class="sxs-lookup"><span data-stu-id="ac14c-106">To prevent this warning, set the Permanent bit in the Attributes column of the [Component table](component-table.md) for every component that is marked for installation into the SystemFolder.</span></span> <span data-ttu-id="ac14c-107">Wenn die Datenbank keine Komponenten Tabelle enthält, erfolgt keine Validierung.</span><span class="sxs-lookup"><span data-stu-id="ac14c-107">No validation is done if the database does not have a Component table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac14c-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ac14c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac14c-109">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="ac14c-109">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



