---
description: Jeder dxsas-kompatible Effekt muss mindestens einen einzelnen globalen Effektparameter mit der globalen Semantik definieren.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Globaler Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345997"
---
# <a name="global-parameter"></a><span data-ttu-id="70495-103">Globaler Parameter</span><span class="sxs-lookup"><span data-stu-id="70495-103">Global Parameter</span></span>

<span data-ttu-id="70495-104">Jeder dxsas-kompatible Effekt muss mindestens einen einzelnen globalen Effektparameter mit der globalen Semantik definieren.</span><span class="sxs-lookup"><span data-stu-id="70495-104">Each DXSAS compliant effect must define, as a minimum, a single global effect parameter with the global semantic.</span></span> <span data-ttu-id="70495-105">Der globale Parameter kann auch eine oder mehrere optionale Anmerkungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="70495-105">The global parameter can also use one or more optional annotations.</span></span> <span data-ttu-id="70495-106">Die Syntax lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="70495-106">The syntax is as follows:</span></span>


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



<span data-ttu-id="70495-107">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="70495-107">where:</span></span>

-   <span data-ttu-id="70495-108">VariableName ist ein vom Benutzer angegebener ASCII-Text Zeichenfolgen-Variablenname.</span><span class="sxs-lookup"><span data-stu-id="70495-108">VariableName is a user-specified, ASCII text string variable name.</span></span>
-   <span data-ttu-id="70495-109">Sasglobal ist das semantische Schlüsselwort, mit dem dieser Parameter als globaler dxsas-Parameter identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="70495-109">SasGlobal is the semantic keyword that identifies this parameter as the global DXSAS parameter.</span></span>
-   <span data-ttu-id="70495-110">Sasversion ist die einzige erforderliche Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="70495-110">SasVersion is the only required annotation.</span></span>
-   <span data-ttu-id="70495-111">Optionalannotations kann Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="70495-111">OptionalAnnotations can include the following:</span></span>
    -   [<span data-ttu-id="70495-112">Saseffectauthor</span><span class="sxs-lookup"><span data-stu-id="70495-112">SasEffectAuthor</span></span>](#saseffectauthor)
    -   [<span data-ttu-id="70495-113">Saseffectauthoringsoftware</span><span class="sxs-lookup"><span data-stu-id="70495-113">SasEffectAuthoringSoftware</span></span>](#saseffectauthoringsoftware)
    -   [<span data-ttu-id="70495-114">Saseffectcategory</span><span class="sxs-lookup"><span data-stu-id="70495-114">SasEffectCategory</span></span>](#saseffectcategory)
    -   [<span data-ttu-id="70495-115">Saseffectcompany</span><span class="sxs-lookup"><span data-stu-id="70495-115">SasEffectCompany</span></span>](#saseffectcompany)
    -   [<span data-ttu-id="70495-116">Saseffectdescription</span><span class="sxs-lookup"><span data-stu-id="70495-116">SasEffectDescription</span></span>](#saseffectdescription)
    -   [<span data-ttu-id="70495-117">Saseffecthelp</span><span class="sxs-lookup"><span data-stu-id="70495-117">SasEffectHelp</span></span>](#saseffecthelp)
    -   [<span data-ttu-id="70495-118">Saseffectrevision</span><span class="sxs-lookup"><span data-stu-id="70495-118">SasEffectRevision</span></span>](#saseffectrevision)

## <a name="sasversion"></a><span data-ttu-id="70495-119">Sasversion</span><span class="sxs-lookup"><span data-stu-id="70495-119">SasVersion</span></span>

<span data-ttu-id="70495-120">Die einzige erforderliche Anmerkung ist sasversion.</span><span class="sxs-lookup"><span data-stu-id="70495-120">The only required annotation is SasVersion.</span></span> <span data-ttu-id="70495-121">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-121">It is declared like this:</span></span>


```
int3 SasVersion = { major, minor, revision };
```



<span data-ttu-id="70495-122">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="70495-122">where:</span></span>

-   <span data-ttu-id="70495-123">Major gibt die dxsas-Hauptversion an.</span><span class="sxs-lookup"><span data-stu-id="70495-123">major indicates the DXSAS major release.</span></span> <span data-ttu-id="70495-124">Hauptversionen von dxsas können tiefgreifende Änderungen am Satz von Semantik und Anmerkungen enthalten, die definiert sind.</span><span class="sxs-lookup"><span data-stu-id="70495-124">Major releases of DXSAS can contain sweeping changes to the set of semantics and annotations defined.</span></span> <span data-ttu-id="70495-125">Semantik und Anmerkungen können hinzugefügt und entfernt werden, und im Allgemeinen ist die Abwärtskompatibilität mit früheren Releases nicht sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="70495-125">Semantics and annotations can be added and removed and, in general, backward compatibility with previous releases is not guaranteed.</span></span>
-   <span data-ttu-id="70495-126">"Minor" gibt die SAS-neben Version an.</span><span class="sxs-lookup"><span data-stu-id="70495-126">minor indicates the SAS minor release.</span></span> <span data-ttu-id="70495-127">Kleinere Releases von dxsas können das Hinzufügen neuer Semantik oder Anmerkungen einschließen.</span><span class="sxs-lookup"><span data-stu-id="70495-127">Minor releases of DXSAS can include the addition of new semantics or annotations.</span></span> <span data-ttu-id="70495-128">Darüber hinaus können Semantik und Anmerkungen im dxsas-Standard als veraltet markiert werden.</span><span class="sxs-lookup"><span data-stu-id="70495-128">Additionally, semantics and annotations may be marked as deprecated in the DXSAS standard.</span></span> <span data-ttu-id="70495-129">Veraltete Semantik und Anmerkungen müssen von Host Anwendungen weiterhin unterstützt werden, Sie können jedoch eine Warnungs Diagnose ausgeben, wenn eine solche Semantik oder Anmerkung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70495-129">Deprecated semantics and annotations must still be supported by host applications but can emit a warning diagnostic when such a semantic or annotation is used.</span></span> <span data-ttu-id="70495-130">Neben Versionen sind abwärts kompatibel mit früheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="70495-130">Minor releases are backward compatible with previous releases.</span></span>
-   <span data-ttu-id="70495-131">Revision gibt die dxsas-Revision an.</span><span class="sxs-lookup"><span data-stu-id="70495-131">revision indicates the DXSAS revision.</span></span> <span data-ttu-id="70495-132">Revisionen von dxsas sind nur als Mittel zum Beheben von Fehlern, Entfernen von Mehrdeutigkeit und verfeinern des Standards vorhanden.</span><span class="sxs-lookup"><span data-stu-id="70495-132">Revisions of DXSAS exist only as a means to fix bugs, remove ambiguity, and refine the standard.</span></span> <span data-ttu-id="70495-133">Revisionen des Standards sind abwärts kompatibel mit früheren Versionen.</span><span class="sxs-lookup"><span data-stu-id="70495-133">Revisions to the standard are backward compatible with previous releases.</span></span>

<span data-ttu-id="70495-134">Die aktuelle Version ist 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="70495-134">The current version is 1.0.0.</span></span> <span data-ttu-id="70495-135">Es gibt keinen Standardwert für diese Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="70495-135">There is no default value for this annotation.</span></span>

## <a name="saseffectauthor"></a><span data-ttu-id="70495-136">Saseffectauthor</span><span class="sxs-lookup"><span data-stu-id="70495-136">SasEffectAuthor</span></span>

<span data-ttu-id="70495-137">Dadurch wird die Person deklariert, die den Effekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="70495-137">This declares the person who created the effect.</span></span> <span data-ttu-id="70495-138">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-138">It is declared like this:</span></span>


```
string SasEffectAuthor = "value";
```



<span data-ttu-id="70495-139">wobei value eine Zeichenfolge ist, die den Effekt Autor identifiziert.</span><span class="sxs-lookup"><span data-stu-id="70495-139">where value is a string that identifies the effect author.</span></span> <span data-ttu-id="70495-140">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70495-140">The default is an empty string.</span></span>

## <a name="saseffectauthoringsoftware"></a><span data-ttu-id="70495-141">Saseffectauthoringsoftware</span><span class="sxs-lookup"><span data-stu-id="70495-141">SasEffectAuthoringSoftware</span></span>

<span data-ttu-id="70495-142">Dadurch wird die Software deklariert, auf der der Effekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="70495-142">This declares the software that the effect was authored on.</span></span> <span data-ttu-id="70495-143">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-143">It is declared like this:</span></span>


```
string SasEffectAuthoringSoftware = "value";
```



<span data-ttu-id="70495-144">Dabei ist value eine Zeichenfolge, die die Auswirkungen der Authoring Software identifiziert.</span><span class="sxs-lookup"><span data-stu-id="70495-144">where value is a string that identifies the effect authoring software.</span></span> <span data-ttu-id="70495-145">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70495-145">The default is an empty string.</span></span>

## <a name="saseffectcategory"></a><span data-ttu-id="70495-146">Saseffectcategory</span><span class="sxs-lookup"><span data-stu-id="70495-146">SasEffectCategory</span></span>

<span data-ttu-id="70495-147">Dadurch wird die Kategorie "Effekt" deklariert.</span><span class="sxs-lookup"><span data-stu-id="70495-147">This declares the effect category.</span></span> <span data-ttu-id="70495-148">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-148">It is declared like this:</span></span>


```
string SasEffectCategory = "value";
```



<span data-ttu-id="70495-149">Dabei ist value eine Zeichenfolge, die die Effekt Kategorie bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="70495-149">where value is a string that identifies the effect category.</span></span> <span data-ttu-id="70495-150">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70495-150">The default is an empty string.</span></span> <span data-ttu-id="70495-151">Die Kategorie wird über einen Pfad ähnlich dem Wert ausgedrückt, wobei der Schrägstrich als Trennzeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70495-151">The category is expressed via a path-like value using the forward slash as a delimiter.</span></span> <span data-ttu-id="70495-152">Effekte können nur zu einer Kategorie gehören, da es keine Syntax zum Ausdrücken von Inklusions in mehrere Pfade innerhalb eines einzelnen saseffectcategory-Werts gibt.</span><span class="sxs-lookup"><span data-stu-id="70495-152">Effects can only belong to one category as there is no syntax for expressing inclusion in multiple paths within a single SasEffectCategory value.</span></span> <span data-ttu-id="70495-153">Der Wert dieser Anmerkung wird von der Host Anwendung nicht als Unterscheidung nach Groß-/Kleinschreibung behandelt.</span><span class="sxs-lookup"><span data-stu-id="70495-153">The value of this annotation is not treated as case-sensitive by the host application.</span></span>

## <a name="saseffectcompany"></a><span data-ttu-id="70495-154">Saseffectcompany</span><span class="sxs-lookup"><span data-stu-id="70495-154">SasEffectCompany</span></span>

<span data-ttu-id="70495-155">Dadurch wird das Unternehmen deklariert, das den Effekt erzeugt hat.</span><span class="sxs-lookup"><span data-stu-id="70495-155">This declares the company that created the effect.</span></span> <span data-ttu-id="70495-156">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-156">It is declared like this:</span></span>


```
string SasEffectCompany = "value";
```



<span data-ttu-id="70495-157">Dabei ist value eine Zeichenfolge, die den Namen des Unternehmens identifiziert, das den Effekt besitzt.</span><span class="sxs-lookup"><span data-stu-id="70495-157">where value is a string that identifies the name of the company that owns the effect.</span></span> <span data-ttu-id="70495-158">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70495-158">The default is an empty string.</span></span>

## <a name="saseffectdescription"></a><span data-ttu-id="70495-159">Saseffectdescription</span><span class="sxs-lookup"><span data-stu-id="70495-159">SasEffectDescription</span></span>

<span data-ttu-id="70495-160">Dies beschreibt den Effekt.</span><span class="sxs-lookup"><span data-stu-id="70495-160">This describes the effect.</span></span> <span data-ttu-id="70495-161">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-161">It is declared like this:</span></span>


```
string SasEffectDescription = "value";
```



<span data-ttu-id="70495-162">wobei value eine Zeichenfolge ist, die den Effekt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="70495-162">where value is a string that describes the effect.</span></span> <span data-ttu-id="70495-163">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70495-163">The default is an empty string.</span></span>

## <a name="saseffecthelp"></a><span data-ttu-id="70495-164">Saseffecthelp</span><span class="sxs-lookup"><span data-stu-id="70495-164">SasEffectHelp</span></span>

<span data-ttu-id="70495-165">Dabei handelt es sich um eine Hilfe Zeichenfolge, die dem Benutzer angezeigt werden kann, wenn Hilfe zu den zugehörigen Effekten angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="70495-165">This is a help string that can be displayed to the user whenever help on the associated effect is requested.</span></span> <span data-ttu-id="70495-166">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-166">It is declared like this:</span></span>


```
string SasEffectHelp = "value";
```



<span data-ttu-id="70495-167">Dabei ist value eine Zeichenfolge, die angezeigt werden kann, wenn der Benutzerhilfe anfordert.</span><span class="sxs-lookup"><span data-stu-id="70495-167">where value is a string that can be displayed if the user requests help.</span></span> <span data-ttu-id="70495-168">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70495-168">The default is an empty string.</span></span>

## <a name="saseffectrevision"></a><span data-ttu-id="70495-169">Saseffectrevision</span><span class="sxs-lookup"><span data-stu-id="70495-169">SasEffectRevision</span></span>

<span data-ttu-id="70495-170">Diese Anmerkung ermöglicht es Tools und Benutzern, die Revisionsnummer der zugehörigen Wirkungs Datei aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="70495-170">This annotation allows tools and users to record the revision number of the associated effect file.</span></span> <span data-ttu-id="70495-171">Beispielsweise könnten Benutzer geeignete Schlüsselwörter in den Wert dieser Anmerkung einfügen, um die Schlüsselwort Ersetzung in Ihrer bevorzugten Revisions Steuerungssoftware aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="70495-171">For example, users could insert appropriate keywords in the value of this annotation to invoke keyword substitution in their favorite revision control software.</span></span> <span data-ttu-id="70495-172">Es wird wie folgt deklariert:</span><span class="sxs-lookup"><span data-stu-id="70495-172">It is declared like this:</span></span>


```
string SasEffectRevision = "value";
```



<span data-ttu-id="70495-173">Dabei ist value eine Zeichenfolge, die die Auswirkung Revision bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="70495-173">where value is a string that identifies the effect revision.</span></span> <span data-ttu-id="70495-174">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70495-174">The default is an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="70495-175">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70495-175">Examples</span></span>

<span data-ttu-id="70495-176">Es folgt ein Beispiel, in dem nur die einzige erforderliche Anmerkung verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="70495-176">Here is an example that uses only the single, required annotation:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



<span data-ttu-id="70495-177">Im folgenden finden Sie ein Beispiel, in dem die erforderliche Anmerkung und einige optionale Anmerkungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="70495-177">Here is an example that uses the required annotation and several optional annotations:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a><span data-ttu-id="70495-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70495-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70495-179">DirectX-Standard Anmerkungen und Semantik Referenz</span><span class="sxs-lookup"><span data-stu-id="70495-179">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



