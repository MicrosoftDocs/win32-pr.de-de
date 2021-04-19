---
description: In der CheckBox-Tabelle sind die Werte für die Kontrollkästchen aufgeführt.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: CheckBox-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349808"
---
# <a name="checkbox-table"></a><span data-ttu-id="d65b5-103">CheckBox-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d65b5-103">CheckBox Table</span></span>

<span data-ttu-id="d65b5-104">In der CheckBox-Tabelle sind die Werte für die Kontrollkästchen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d65b5-104">The CheckBox table lists the values for the check boxes.</span></span>

<span data-ttu-id="d65b5-105">Die CheckBox-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="d65b5-105">The CheckBox table has the following columns.</span></span>



| <span data-ttu-id="d65b5-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="d65b5-106">Column</span></span>   | <span data-ttu-id="d65b5-107">Typ</span><span class="sxs-lookup"><span data-stu-id="d65b5-107">Type</span></span>                         | <span data-ttu-id="d65b5-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d65b5-108">Key</span></span> | <span data-ttu-id="d65b5-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d65b5-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="d65b5-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d65b5-110">Property</span></span> | [<span data-ttu-id="d65b5-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d65b5-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d65b5-112">J</span><span class="sxs-lookup"><span data-stu-id="d65b5-112">Y</span></span>   | <span data-ttu-id="d65b5-113">N</span><span class="sxs-lookup"><span data-stu-id="d65b5-113">N</span></span>        |
| <span data-ttu-id="d65b5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d65b5-114">Value</span></span>    | [<span data-ttu-id="d65b5-115">Großformatige</span><span class="sxs-lookup"><span data-stu-id="d65b5-115">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d65b5-116">N</span><span class="sxs-lookup"><span data-stu-id="d65b5-116">N</span></span>   | <span data-ttu-id="d65b5-117">J</span><span class="sxs-lookup"><span data-stu-id="d65b5-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d65b5-118">Spalten</span><span class="sxs-lookup"><span data-stu-id="d65b5-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d65b5-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="d65b5-119"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="d65b5-120">Eine benannte Eigenschaft, die an dieses Element gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="d65b5-120">A named property to be tied to this item.</span></span>

</dd> <dt>

<span data-ttu-id="d65b5-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="d65b5-121"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="d65b5-122">Die diesem Element zugeordnete Wert Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d65b5-122">The value string associated with this item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d65b5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d65b5-123">Remarks</span></span>

<span data-ttu-id="d65b5-124">Wenn das Kontrollkästchen aktiviert ist, wird die entsprechende Eigenschaft auf den angegebenen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d65b5-124">If the check box is selected, then the corresponding property is set to the specified value.</span></span> <span data-ttu-id="d65b5-125">Wenn kein Wert angegeben ist oder diese Tabelle nicht vorhanden ist, wird die-Eigenschaft auf den ursprünglichen Wert festgelegt, wenn das Kontrollkästchen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d65b5-125">If there is no value specified or this table does not exist, then the property is set to its original value when the check box is selected.</span></span> <span data-ttu-id="d65b5-126">Wenn der ursprüngliche Wert NULL ist, wird die-Eigenschaft auf "1" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d65b5-126">If the original value is null, the property is set to "1".</span></span>

<span data-ttu-id="d65b5-127">Der Inhalt der Value-Spalte wird bei der Erstellung des Steuer Elements durch die [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion formatiert.</span><span class="sxs-lookup"><span data-stu-id="d65b5-127">The contents of the Value column are formatted by the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function when the control is created.</span></span> <span data-ttu-id="d65b5-128">Daher kann Sie jeden beliebigen Ausdruck enthalten, der von der **msiformatrecord** -Funktion interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d65b5-128">Therefore, it can contain any expression that the **MsiFormatRecord** function can interpret.</span></span> <span data-ttu-id="d65b5-129">Die Value-Spalte wird nur formatiert, wenn das Steuerelement erstellt wird, und wird nicht aktualisiert, wenn eine an einem Ausdruck beteiligte Eigenschaft während der Lebensdauer des Steuer Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d65b5-129">The Value column is formatted only when the control is created, and it is not updated if a property involved in an expression is modified during the life of the control.</span></span>

## <a name="validation"></a><span data-ttu-id="d65b5-130">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d65b5-130">Validation</span></span>

<dl>

[<span data-ttu-id="d65b5-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="d65b5-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d65b5-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="d65b5-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d65b5-133">ICE46</span><span class="sxs-lookup"><span data-stu-id="d65b5-133">ICE46</span></span>](ice46.md)  
</dl>

 

 



