---
description: Die Eigenschaften Tabelle enthält die Eigenschaftsnamen und-Werte für alle definierten Eigenschaften in der Installation. Eigenschaften mit NULL-Werten sind nicht in der Tabelle vorhanden.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Eigenschaften Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756481"
---
# <a name="property-table"></a><span data-ttu-id="5de78-104">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="5de78-104">Property Table</span></span>

<span data-ttu-id="5de78-105">Die Eigenschaften Tabelle enthält die Eigenschaftsnamen und-Werte für alle definierten Eigenschaften in der Installation.</span><span class="sxs-lookup"><span data-stu-id="5de78-105">The Property table contains the property names and values for all defined properties in the installation.</span></span> <span data-ttu-id="5de78-106">Eigenschaften mit NULL-Werten sind nicht in der Tabelle vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5de78-106">Properties with Null values are not present in the table.</span></span>

<span data-ttu-id="5de78-107">Die Eigenschaften Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="5de78-107">The Property table has the following columns.</span></span>



| <span data-ttu-id="5de78-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="5de78-108">Column</span></span>   | <span data-ttu-id="5de78-109">Typ</span><span class="sxs-lookup"><span data-stu-id="5de78-109">Type</span></span>                         | <span data-ttu-id="5de78-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="5de78-110">Key</span></span> | <span data-ttu-id="5de78-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="5de78-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="5de78-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5de78-112">Property</span></span> | [<span data-ttu-id="5de78-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="5de78-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="5de78-114">J</span><span class="sxs-lookup"><span data-stu-id="5de78-114">Y</span></span>   | <span data-ttu-id="5de78-115">N</span><span class="sxs-lookup"><span data-stu-id="5de78-115">N</span></span>        |
| <span data-ttu-id="5de78-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5de78-116">Value</span></span>    | [<span data-ttu-id="5de78-117">Text</span><span class="sxs-lookup"><span data-stu-id="5de78-117">Text</span></span>](text.md)             | <span data-ttu-id="5de78-118">N</span><span class="sxs-lookup"><span data-stu-id="5de78-118">N</span></span>   | <span data-ttu-id="5de78-119">N</span><span class="sxs-lookup"><span data-stu-id="5de78-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5de78-120">Spalten</span><span class="sxs-lookup"><span data-stu-id="5de78-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5de78-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span><span class="sxs-lookup"><span data-stu-id="5de78-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="5de78-122">Der Name einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5de78-122">The name of a property.</span></span> <span data-ttu-id="5de78-123">Siehe [Eigenschaften](properties.md).</span><span class="sxs-lookup"><span data-stu-id="5de78-123">See [Properties](properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="5de78-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="5de78-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="5de78-125">Ein Lokalisier barer Zeichen folgen Wert für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5de78-125">A localizable string value for the property.</span></span> <span data-ttu-id="5de78-126">Dies darf niemals NULL oder eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="5de78-126">This may never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5de78-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5de78-127">Remarks</span></span>

<span data-ttu-id="5de78-128">Beachten Sie, dass Sie die Eigenschafts Tabelle nicht verwenden können, um eine Eigenschaft auf den Wert einer anderen Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5de78-128">Note that you cannot use the Property table to set a property to the value of another property.</span></span> <span data-ttu-id="5de78-129">Das Installationsprogramm führt keine Aktion für die Text Zeichenfolge aus, die in der Spalte Wert eingegeben wurde, bevor die Eigenschaft in der Eigenschafts Spalte</span><span class="sxs-lookup"><span data-stu-id="5de78-129">The installer does nothing to the text string entered in the Value column before setting the property in the Property column.</span></span> <span data-ttu-id="5de78-130">Wenn firstproperty in die Eigenschafts Spalte und \[ secondproperty \] in der Spalte Wert eingegeben wird, wird der Wert von firstproperty auf die Text Zeichenfolge " \[ secondproperty \] " und nicht auf den Wert der secondproperty-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5de78-130">If FirstProperty is entered into the Property column and \[SecondProperty\] in the Value column, the value of FirstProperty is set to the text string "\[SecondProperty\]" and not to the value of the SecondProperty property.</span></span> <span data-ttu-id="5de78-131">Dies ist erforderlich, um zu verhindern, dass Zirkel Verweise in der Eigenschaften Tabelle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5de78-131">This is necessary to prevent creating circular references in the Property table.</span></span> <span data-ttu-id="5de78-132">Stattdessen können Sie eine Eigenschaft mit einem [benutzerdefinierten Aktionstyp 51](custom-action-type-51.md)auf einen anderen festlegen.</span><span class="sxs-lookup"><span data-stu-id="5de78-132">Instead, you can set one property to another by using a [Custom Action Type 51](custom-action-type-51.md).</span></span>

<span data-ttu-id="5de78-133">Beachten Sie, dass die Eigenschaft [**adminproperties**](adminproperties.md) verwendet werden kann, um die Werte in der Eigenschaften Tabelle während einer [administrativen Installation](administrative-installation.md)zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="5de78-133">Note that the [**AdminProperties**](adminproperties.md) property can be used to override the values in the Property table during an [Administrative Installation](administrative-installation.md).</span></span>

<span data-ttu-id="5de78-134">Verwenden Sie keine Eigenschaften für Kenn Wörter oder andere Informationen, die sicher bleiben müssen.</span><span class="sxs-lookup"><span data-stu-id="5de78-134">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="5de78-135">Das Installationsprogramm kann den Wert einer Eigenschaft, die in die Eigenschaften Tabelle geschrieben oder zur Laufzeit erstellt wurde, in ein Protokoll oder die Systemregistrierung schreiben.</span><span class="sxs-lookup"><span data-stu-id="5de78-135">The installer may write the value of a property authored into the Property table, or created at runtime, into a log or the system registry.</span></span>

## <a name="validation"></a><span data-ttu-id="5de78-136">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="5de78-136">Validation</span></span>

<dl>

[<span data-ttu-id="5de78-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="5de78-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5de78-138">ICE05</span><span class="sxs-lookup"><span data-stu-id="5de78-138">ICE05</span></span>](ice05.md)  
[<span data-ttu-id="5de78-139">ICE06</span><span class="sxs-lookup"><span data-stu-id="5de78-139">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5de78-140">ICE16</span><span class="sxs-lookup"><span data-stu-id="5de78-140">ICE16</span></span>](ice16.md)  
[<span data-ttu-id="5de78-141">ICE24</span><span class="sxs-lookup"><span data-stu-id="5de78-141">ICE24</span></span>](ice24.md)  
[<span data-ttu-id="5de78-142">ICE31</span><span class="sxs-lookup"><span data-stu-id="5de78-142">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="5de78-143">ICE34</span><span class="sxs-lookup"><span data-stu-id="5de78-143">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="5de78-144">ICE36</span><span class="sxs-lookup"><span data-stu-id="5de78-144">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="5de78-145">ICE40</span><span class="sxs-lookup"><span data-stu-id="5de78-145">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="5de78-146">ICE46</span><span class="sxs-lookup"><span data-stu-id="5de78-146">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="5de78-147">ICE48</span><span class="sxs-lookup"><span data-stu-id="5de78-147">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="5de78-148">ICE52</span><span class="sxs-lookup"><span data-stu-id="5de78-148">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="5de78-149">ICE61</span><span class="sxs-lookup"><span data-stu-id="5de78-149">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="5de78-150">ICE73</span><span class="sxs-lookup"><span data-stu-id="5de78-150">ICE73</span></span>](ice73.md)  
[<span data-ttu-id="5de78-151">ICE74</span><span class="sxs-lookup"><span data-stu-id="5de78-151">ICE74</span></span>](ice74.md)  
[<span data-ttu-id="5de78-152">ICE80</span><span class="sxs-lookup"><span data-stu-id="5de78-152">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="5de78-153">ICE87</span><span class="sxs-lookup"><span data-stu-id="5de78-153">ICE87</span></span>](ice87.md)  
[<span data-ttu-id="5de78-154">ICE88</span><span class="sxs-lookup"><span data-stu-id="5de78-154">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="5de78-155">ICE91</span><span class="sxs-lookup"><span data-stu-id="5de78-155">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="5de78-156">ICE99</span><span class="sxs-lookup"><span data-stu-id="5de78-156">ICE99</span></span>](ice99.md)  
</dl>

 

 



