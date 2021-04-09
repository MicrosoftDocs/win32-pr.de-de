---
description: Die UIText-Tabelle enthält die lokalisierten Versionen einiger der Zeichen folgen, die in der Benutzeroberfläche verwendet werden. Diese Zeichen folgen sind nicht Teil einer anderen Tabelle. Die UIText-Tabelle ist für Zeichen folgen, die keine logische Position in einer anderen Tabelle aufweisen.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: UIText-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128100"
---
# <a name="uitext-table"></a><span data-ttu-id="425ca-105">UIText-Tabelle</span><span class="sxs-lookup"><span data-stu-id="425ca-105">UIText Table</span></span>

<span data-ttu-id="425ca-106">Die UIText-Tabelle enthält die lokalisierten Versionen einiger der Zeichen folgen, die in der Benutzeroberfläche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="425ca-106">The UIText table contains the localized versions of some of the strings used in the user interface.</span></span> <span data-ttu-id="425ca-107">Diese Zeichen folgen sind nicht Teil einer anderen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="425ca-107">These strings are not part of any other table.</span></span> <span data-ttu-id="425ca-108">Die UIText-Tabelle ist für Zeichen folgen, die keine logische Position in einer anderen Tabelle aufweisen.</span><span class="sxs-lookup"><span data-stu-id="425ca-108">The UIText table is for strings that have no logical place in any other table.</span></span>

<span data-ttu-id="425ca-109">Die UIText-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="425ca-109">The UIText table has the following columns.</span></span>



| <span data-ttu-id="425ca-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="425ca-110">Column</span></span> | <span data-ttu-id="425ca-111">Typ</span><span class="sxs-lookup"><span data-stu-id="425ca-111">Type</span></span>                         | <span data-ttu-id="425ca-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="425ca-112">Key</span></span> | <span data-ttu-id="425ca-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="425ca-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="425ca-114">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="425ca-114">Key</span></span>    | [<span data-ttu-id="425ca-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="425ca-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="425ca-116">J</span><span class="sxs-lookup"><span data-stu-id="425ca-116">Y</span></span>   | <span data-ttu-id="425ca-117">N</span><span class="sxs-lookup"><span data-stu-id="425ca-117">N</span></span>        |
| <span data-ttu-id="425ca-118">Text</span><span class="sxs-lookup"><span data-stu-id="425ca-118">Text</span></span>   | [<span data-ttu-id="425ca-119">Text</span><span class="sxs-lookup"><span data-stu-id="425ca-119">Text</span></span>](text.md)             | <span data-ttu-id="425ca-120">N</span><span class="sxs-lookup"><span data-stu-id="425ca-120">N</span></span>   | <span data-ttu-id="425ca-121">J</span><span class="sxs-lookup"><span data-stu-id="425ca-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="425ca-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="425ca-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="425ca-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen</span><span class="sxs-lookup"><span data-stu-id="425ca-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="425ca-124">Ein eindeutiger Schlüssel, der die jeweilige Zeichenfolge identifiziert.</span><span class="sxs-lookup"><span data-stu-id="425ca-124">A unique key that identifies the particular string.</span></span>

</dd> <dt>

<span data-ttu-id="425ca-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span><span class="sxs-lookup"><span data-stu-id="425ca-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="425ca-126">Die lokalisierte Version der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="425ca-126">The localized version of the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="425ca-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="425ca-127">Remarks</span></span>

<span data-ttu-id="425ca-128">Einige Steuerelemente verwenden die UIText-Tabelle als Quelle von Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="425ca-128">Some controls use the UIText table as a source of strings.</span></span> <span data-ttu-id="425ca-129">Informationen dazu, welche Zeichen folgen in dieser Tabelle für jedes bestimmte Steuerelement erforderlich sind, finden Sie unter den einzelnen Steuerelementen in der [Benutzeroberflächen Referenz](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="425ca-129">For information about which strings are required in this table for each particular control, see the individual controls in the [User Interface Reference](user-interface-reference.md).</span></span>

## <a name="validation"></a><span data-ttu-id="425ca-130">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="425ca-130">Validation</span></span>

<dl>

[<span data-ttu-id="425ca-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="425ca-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="425ca-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="425ca-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



