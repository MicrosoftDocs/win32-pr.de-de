---
title: Informationen zu .NET Framework-Datentypen
description: Informationen zu .NET Framework-Datentypen
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player,. NET-Framework
- Windows Media Player-Objektmodell,. NET-Framework
- Objektmodell,. NET-Framework
- Windows Media Player Mobile,. NET-Framework
- Windows Media Player ActiveX-Steuerelement,. NET-Framework
- Windows Media Player Mobile ActiveX-Steuerelement,. NET-Framework
- ActiveX-Steuerelement,. NET-Framework
- .NET Framework, Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037462"
---
# <a name="about-net-framework-data-types"></a><span data-ttu-id="a2f32-111">Informationen zu .NET Framework-Datentypen</span><span class="sxs-lookup"><span data-stu-id="a2f32-111">About .NET Framework Data Types</span></span>

<span data-ttu-id="a2f32-112">Dieser Abschnitt enthält die Informationen, die Sie zum Übersetzen der Skript orientierten Objektmodell Referenz in Microsoft .NET Framework-Basis Datentypen benötigen.</span><span class="sxs-lookup"><span data-stu-id="a2f32-112">This section contains the information you need to translate the script-oriented Object Model Reference into Microsoft .NET Framework base data types.</span></span> <span data-ttu-id="a2f32-113">Die Windows Media Player Skript Referenz enthält fast alle Informationen, die Sie benötigen, um das Windows Media Player-Steuerelement in einem .NET Framework basierten Programm zu verwenden, und in den meisten Fällen ähnelt die Syntax dem anderer Skriptsprachen, wie z. b. Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="a2f32-113">The Windows Media Player script reference has almost all the information you need to use the Windows Media Player control in a .NET Framework-based program, and in most cases, the syntax will be similar to that of other scripting languages such as Microsoft JScript.</span></span>

<span data-ttu-id="a2f32-114">Die Windows-Media Player Referenz stellt den JScript-Datentyp und ggf. die C++-Konvertierung bereit.</span><span class="sxs-lookup"><span data-stu-id="a2f32-114">The Windows Media Player reference provides the JScript data type and, if necessary, the C++ conversion.</span></span> <span data-ttu-id="a2f32-115">Beispielsweise kann eine- **Zahl** von einer-Methode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a2f32-115">For example, a **Number** might be returned by a method.</span></span> <span data-ttu-id="a2f32-116">JScript behandelt alle Zahlen auf die gleiche Weise, aber andere Sprachen unterscheiden zwischen verschiedenen Arten von Zahlen (Integer, Gleit Komma usw.).</span><span class="sxs-lookup"><span data-stu-id="a2f32-116">JScript treats all numbers in the same way, but other languages distinguish between different types of numbers (integer, floating point, and so on).</span></span> <span data-ttu-id="a2f32-117">Der Verweis ermöglicht die C++-Konvertierung für Zahlen Datentypen, da Zahlen von C++ anders verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="a2f32-117">The reference gives the C++ conversion for number data types because numbers can be processed differently by C++.</span></span> <span data-ttu-id="a2f32-118">Beispielsweise verwendet C++ den **int** -Datentyp für ganzzahlige Arithmetik und **float** für Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="a2f32-118">For example, C++ uses the **int** data type for integer arithmetic and **float** for floating point.</span></span>

<span data-ttu-id="a2f32-119">Der .NET Framework verwendet ein geringfügig anderes System von Basis Datentypen.</span><span class="sxs-lookup"><span data-stu-id="a2f32-119">The .NET Framework uses a slightly different system of base data types.</span></span> <span data-ttu-id="a2f32-120">In der folgenden Tabelle sind die Unterschiede in den häufig verwendeten Datentypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2f32-120">The following table shows the differences in the common data types you are likely to use.</span></span> <span data-ttu-id="a2f32-121">Weitere Informationen zu .NET Framework Basis Datentypen und der Konvertierung in andere Datentyp Systeme finden Sie im .NET Framework Entwicklerhandbuch zu System Namespace-Basis Datentypen.</span><span class="sxs-lookup"><span data-stu-id="a2f32-121">For more information on .NET Framework base data types and the conversion to other data type systems, see the .NET Framework Developer's Guide discussion of System Namespace base data types.</span></span>

<span data-ttu-id="a2f32-122">Diese Tabelle gibt den .NET Framework Klassennamen und den c#-Datentyp an.</span><span class="sxs-lookup"><span data-stu-id="a2f32-122">This table gives the .NET Framework class name and the C# data type.</span></span> <span data-ttu-id="a2f32-123">Datentypen für andere Sprachen werden in den jeweiligen sprach verweisen für jede Sprache definiert.</span><span class="sxs-lookup"><span data-stu-id="a2f32-123">Data types for other languages are defined for each language in their respective language references.</span></span>



| <span data-ttu-id="a2f32-124">Skript Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2f32-124">Script data type</span></span> | <span data-ttu-id="a2f32-125">C++-Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2f32-125">C++ data type</span></span>     | <span data-ttu-id="a2f32-126">.NET Framework-Klasse (c#-Datentyp)</span><span class="sxs-lookup"><span data-stu-id="a2f32-126">.NET Framework class (C# data type )</span></span> |
|------------------|-------------------|---------------------------------------|
| <span data-ttu-id="a2f32-127">**Number**</span><span class="sxs-lookup"><span data-stu-id="a2f32-127">**Number**</span></span>       | <span data-ttu-id="a2f32-128">**int**</span><span class="sxs-lookup"><span data-stu-id="a2f32-128">**int**</span></span>           | <span data-ttu-id="a2f32-129">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="a2f32-129">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="a2f32-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="a2f32-130">**Number**</span></span>       | <span data-ttu-id="a2f32-131">**long**</span><span class="sxs-lookup"><span data-stu-id="a2f32-131">**long**</span></span>          | <span data-ttu-id="a2f32-132">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="a2f32-132">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="a2f32-133">**Number**</span><span class="sxs-lookup"><span data-stu-id="a2f32-133">**Number**</span></span>       | <span data-ttu-id="a2f32-134">**double**</span><span class="sxs-lookup"><span data-stu-id="a2f32-134">**double**</span></span>        | <span data-ttu-id="a2f32-135">**Double** (**Double**)</span><span class="sxs-lookup"><span data-stu-id="a2f32-135">**Double** (**double**)</span></span>               |
| <span data-ttu-id="a2f32-136">**Number**</span><span class="sxs-lookup"><span data-stu-id="a2f32-136">**Number**</span></span>       | <span data-ttu-id="a2f32-137">**float**</span><span class="sxs-lookup"><span data-stu-id="a2f32-137">**float**</span></span>         | <span data-ttu-id="a2f32-138">**Single** (**float**)</span><span class="sxs-lookup"><span data-stu-id="a2f32-138">**Single** (**float**)</span></span>                |
| <span data-ttu-id="a2f32-139">**String**</span><span class="sxs-lookup"><span data-stu-id="a2f32-139">**String**</span></span>       | <span data-ttu-id="a2f32-140">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="a2f32-140">**BSTR**</span></span>          | <span data-ttu-id="a2f32-141">**String** (**Zeichenfolge**)</span><span class="sxs-lookup"><span data-stu-id="a2f32-141">**String** (**string**)</span></span>               |
| <span data-ttu-id="a2f32-142">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="a2f32-142">**Boolean**</span></span>      | <span data-ttu-id="a2f32-143">**Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a2f32-143">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="a2f32-144">**Boolean** (**bool**)</span><span class="sxs-lookup"><span data-stu-id="a2f32-144">**Boolean** (**bool**)</span></span>                |
| <span data-ttu-id="a2f32-145">**Object**</span><span class="sxs-lookup"><span data-stu-id="a2f32-145">**Object**</span></span>       | <span data-ttu-id="a2f32-146">**Object**</span><span class="sxs-lookup"><span data-stu-id="a2f32-146">**Object**</span></span>        | <span data-ttu-id="a2f32-147">**Object** (**Objekt**)</span><span class="sxs-lookup"><span data-stu-id="a2f32-147">**Object** (**object**)</span></span>               |



 

<span data-ttu-id="a2f32-148">Wenn Sie Visual Studio verwenden, können Sie die Microsoft IntelliSense-Technologie verwenden, um zu bestimmen, welcher Datentyp für eine bestimmte Funktion erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="a2f32-148">If you are using Visual Studio, you can use the Microsoft IntelliSense technology to determine what data type is expected for a specific function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2f32-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a2f32-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2f32-150">**Einbetten des Windows Media Player-Steuer Elements in eine .NET Framework Lösung**</span><span class="sxs-lookup"><span data-stu-id="a2f32-150">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="a2f32-151">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="a2f32-151">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




