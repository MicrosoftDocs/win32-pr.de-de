---
description: Mit diesem Attribut wird gemessen, wie weit die Status Indikator Leiste ausgefüllt ist.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Fortschritts Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360855"
---
# <a name="progress-control-attribute"></a><span data-ttu-id="b0efc-103">Fortschritts Steuerungs Attribut</span><span class="sxs-lookup"><span data-stu-id="b0efc-103">Progress Control Attribute</span></span>

<span data-ttu-id="b0efc-104">Mit diesem Attribut wird gemessen, wie weit die Status Indikator Leiste ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="b0efc-104">This attribute measures how far the progress indicator bar is filled.</span></span> <span data-ttu-id="b0efc-105">Der Datensatz enthält zwei ganze Zahlen und eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b0efc-105">The record contains two integers and a string.</span></span> <span data-ttu-id="b0efc-106">Die erste Zahl ist der Fortschritt, die zweite Zahl der Bereich (die maximal mögliche Anzahl für den Fortschritt).</span><span class="sxs-lookup"><span data-stu-id="b0efc-106">The first number is the progress, the second number is the range (the maximal possible number for the progress).</span></span> <span data-ttu-id="b0efc-107">Bei der Einstellung können die ganzen Zahlen als ganzzahlige Felder oder Zeichen folgen eingegeben werden, die die ganzen Zahlen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0efc-107">On setting, the integers can be entered as integer fields or strings containing the integers.</span></span> <span data-ttu-id="b0efc-108">Wenn die zweite Zahl fehlt, wird angenommen, dass es sich um den Standardwert (1024) handelt.</span><span class="sxs-lookup"><span data-stu-id="b0efc-108">If the second number is missing it is assumed to be the default (1024).</span></span> <span data-ttu-id="b0efc-109">Wenn der Fortschritt größer als der Bereich ist, wird er in den Bereich geändert.</span><span class="sxs-lookup"><span data-stu-id="b0efc-109">If the progress is larger than the range then it is changed to be the range.</span></span> <span data-ttu-id="b0efc-110">Das dritte Feld ist eine Zeichenfolge, der Name der Aktion, deren Status angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b0efc-110">The third field is a string, the name of the action whose progress is displayed.</span></span>

<span data-ttu-id="b0efc-111">Weitere Informationen finden Sie unter [Erstellen eines ProgressBar-Steuer](authoring-a-progressbar-control.md)Elements und [Hinzufügen von benutzerdefinierten Aktionen zu "ProgressBar](adding-custom-actions-to-the-progressbar.md)".</span><span class="sxs-lookup"><span data-stu-id="b0efc-111">For related information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), and [Adding Custom Actions to the ProgressBar](adding-custom-actions-to-the-progressbar.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b0efc-112">Gültige Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="b0efc-112">Valid Controls</span></span>

[<span data-ttu-id="b0efc-113">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="b0efc-113">ProgressBar</span></span>](progressbar-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="b0efc-114">Zugehörige Bitflags</span><span class="sxs-lookup"><span data-stu-id="b0efc-114">Associated Bit Flags</span></span>

<span data-ttu-id="b0efc-115">Dieses Attribut verwendet keine Bitflags.</span><span class="sxs-lookup"><span data-stu-id="b0efc-115">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0efc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0efc-116">Remarks</span></span>

<span data-ttu-id="b0efc-117">Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="b0efc-117">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



