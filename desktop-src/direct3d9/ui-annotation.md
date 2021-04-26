---
description: Verwenden Sie diese Anmerkung, um einem Ui-Steuerelement in der Hostumgebung einen Effect-Parameter zuzuordnen. Dadurch kann ein Benutzer einen Effect-Parameter interaktiv über die Hostanwendung steuern.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Benutzeroberflächenanmerkung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef6af352b7dea25df34ce8a5712ad30143d6426
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998587"
---
# <a name="ui-annotation"></a><span data-ttu-id="50078-104">Benutzeroberflächenanmerkung</span><span class="sxs-lookup"><span data-stu-id="50078-104">UI Annotation</span></span>

<span data-ttu-id="50078-105">Verwenden Sie diese Anmerkung, um einem Ui-Steuerelement in der Hostumgebung einen Effect-Parameter zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="50078-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="50078-106">Dadurch kann ein Benutzer einen Effect-Parameter interaktiv über die Hostanwendung steuern.</span><span class="sxs-lookup"><span data-stu-id="50078-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="50078-107">DXSAS definiert eine Reihe von Standardsteuerelementen im Hinblick auf das Datenmodell und das grundlegende Verhalten, die Autoren von Hostanwendungen erwarten können.</span><span class="sxs-lookup"><span data-stu-id="50078-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="50078-108">Die Steuerelementanmerkung wird wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="50078-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="50078-109">where</span><span class="sxs-lookup"><span data-stu-id="50078-109">where</span></span>


```
ControlType
```



<span data-ttu-id="50078-110">ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="50078-110">is one of the following:</span></span>



| <span data-ttu-id="50078-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="50078-111">ControlType</span></span> | <span data-ttu-id="50078-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50078-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="50078-113">Interner Datentyp</span><span class="sxs-lookup"><span data-stu-id="50078-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="50078-114">Steuerelementeigenschaftenanmerkungen</span><span class="sxs-lookup"><span data-stu-id="50078-114">Control Property Annotations</span></span>                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50078-115">Keine</span><span class="sxs-lookup"><span data-stu-id="50078-115">None</span></span>        | <span data-ttu-id="50078-116">Es sollte kein Steuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="50078-116">No control should be shown.</span></span> <span data-ttu-id="50078-117">Beachten Sie, dass ein Steuerelement sichtbar ist, wenn [SasUiVisible](#sasuivisible) true ist und der Steuerelementtyp ein anderer Typ als None ist.</span><span class="sxs-lookup"><span data-stu-id="50078-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="50078-118">–</span><span class="sxs-lookup"><span data-stu-id="50078-118">n/a</span></span>                                                                                                | <span data-ttu-id="50078-119">–</span><span class="sxs-lookup"><span data-stu-id="50078-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="50078-120">Any</span><span class="sxs-lookup"><span data-stu-id="50078-120">Any</span></span>         | <span data-ttu-id="50078-121">Dies bedeutet, dass kein spezielles Steuerelement angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="50078-121">This implies that no special control is requested.</span></span> <span data-ttu-id="50078-122">Das dargestellte Steuerelement ist das Ergebnis eines anwendungsdefiniertes Verhaltens.</span><span class="sxs-lookup"><span data-stu-id="50078-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="50078-123">–</span><span class="sxs-lookup"><span data-stu-id="50078-123">n/a</span></span>                                                                                                | <span data-ttu-id="50078-124">–</span><span class="sxs-lookup"><span data-stu-id="50078-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="50078-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="50078-125">ColorPicker</span></span> | <span data-ttu-id="50078-126">Stellen Sie einen Farbwert als Farbwatch dar.</span><span class="sxs-lookup"><span data-stu-id="50078-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="50078-127">Der Wert wird in die XYZ-Komponenten des zugeordneten Vektors gepackt.</span><span class="sxs-lookup"><span data-stu-id="50078-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="50078-128">Die W-Komponente des zugeordneten Vektors ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50078-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="50078-129">float *N,* wobei *N* 1 bis 4 einschließlich ist.</span><span class="sxs-lookup"><span data-stu-id="50078-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="50078-130">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="50078-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="50078-131">Direction</span><span class="sxs-lookup"><span data-stu-id="50078-131">Direction</span></span>   | <span data-ttu-id="50078-132">Ein Richtungsvektor.</span><span class="sxs-lookup"><span data-stu-id="50078-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="50078-133">float *N,* wobei *N* 2 bis einschließlich 4 ist.</span><span class="sxs-lookup"><span data-stu-id="50078-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="50078-134">Keine</span><span class="sxs-lookup"><span data-stu-id="50078-134">None</span></span>                                                                                                         |
| <span data-ttu-id="50078-135">FilePicker</span><span class="sxs-lookup"><span data-stu-id="50078-135">FilePicker</span></span>  | <span data-ttu-id="50078-136">Ein Dialogfeld, in dem der Benutzer eine Datei durchsuchen und auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="50078-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="50078-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="50078-137">string</span></span>                                                                                             | <span data-ttu-id="50078-138">Keine</span><span class="sxs-lookup"><span data-stu-id="50078-138">None</span></span>                                                                                                         |
| <span data-ttu-id="50078-139">ListPicker</span><span class="sxs-lookup"><span data-stu-id="50078-139">ListPicker</span></span>  | <span data-ttu-id="50078-140">Eine Liste von Zeichenfolgenwerten, aus denen der Benutzer einen Eintrag auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="50078-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="50078-141">Die Werte werden aus der [SasUiEnum-Anmerkung](#sasuienum) generiert.</span><span class="sxs-lookup"><span data-stu-id="50078-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="50078-142">Ein Array von Zeichenfolgen zusammen mit einem ganzzahligen Wert, der den Index des ausgewählten Zeichenfolgenwerts enthält.</span><span class="sxs-lookup"><span data-stu-id="50078-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="50078-143">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="50078-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="50078-144">Numeric</span><span class="sxs-lookup"><span data-stu-id="50078-144">Numeric</span></span>     | <span data-ttu-id="50078-145">Eine Reihe von numerischen Eingabesteuerelementen (z. B. Textfelder).</span><span class="sxs-lookup"><span data-stu-id="50078-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="50078-146">float *M* x *N,* *wobei M* und *N* inklusive 1 bis 4 sind.</span><span class="sxs-lookup"><span data-stu-id="50078-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="50078-147">[SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiStride](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="50078-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="50078-148">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="50078-148">Slider</span></span>      | <span data-ttu-id="50078-149">Eine Gruppe von Schiebereglern.</span><span class="sxs-lookup"><span data-stu-id="50078-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="50078-150">float *M* x *N,* *wobei M* und *N* inklusive 1 bis 4 sind</span><span class="sxs-lookup"><span data-stu-id="50078-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="50078-151">[SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiSteps,](#sasuisteps) [SasUiStepsPower](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="50078-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="50078-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="50078-152">String</span></span>      | <span data-ttu-id="50078-153">Ein Textfeld zum Bearbeiten von Zeichenfolgeninhalten.</span><span class="sxs-lookup"><span data-stu-id="50078-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="50078-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="50078-154">string</span></span>                                                                                             | <span data-ttu-id="50078-155">Keine</span><span class="sxs-lookup"><span data-stu-id="50078-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="50078-156">Wenn der interne Datentyp nicht mit dem Typ des zugeordneten Parameters identisch ist, erfolgt die Umwandlung, wenn Daten aus dem Hostanwendungsparameter in den Effect-Parameter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="50078-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="50078-157">Der Standardwert ist die Zeichenfolge "None".</span><span class="sxs-lookup"><span data-stu-id="50078-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="50078-158">Allgemeine Eigenschaften der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="50078-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="50078-159">SasUiDescription</span><span class="sxs-lookup"><span data-stu-id="50078-159">SasUiDescription</span></span>

<span data-ttu-id="50078-160">Verwenden Sie diese Anmerkung, um eine Zeichenfolge zum Beschreiben eines Tools anzugeben.</span><span class="sxs-lookup"><span data-stu-id="50078-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="50078-161">Dies kann für Benutzeroberflächenelemente wie QuickInfos verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50078-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="50078-162">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="50078-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="50078-163">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="50078-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="50078-164">SasUiLabel</span><span class="sxs-lookup"><span data-stu-id="50078-164">SasUiLabel</span></span>

<span data-ttu-id="50078-165">Verwenden Sie diese Anmerkung, um eine Zeichenfolge zum Bezeichnen eines beliebigen Ui-Steuerelements anzugeben.</span><span class="sxs-lookup"><span data-stu-id="50078-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="50078-166">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="50078-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="50078-167">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="50078-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="50078-168">SasUiVisible</span><span class="sxs-lookup"><span data-stu-id="50078-168">SasUiVisible</span></span>

<span data-ttu-id="50078-169">Verwenden Sie diese Anmerkung, um anzugeben, ob der zugeordnete Parameter dem Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="50078-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="50078-170">Wenn diese Einstellung auf TRUE festgelegt ist, sollte die Hostanwendung ein Ui-Steuerelement zum Bearbeiten des Parameters mit Anmerkungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="50078-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="50078-171">False gibt an, dass in der Hostanwendung keine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="50078-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="50078-172">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="50078-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="50078-173">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="50078-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="50078-174">Eigenschaften des UI-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="50078-174">UI Control Properties</span></span>

<span data-ttu-id="50078-175">Steuerelementeigenschaftenanmerkungen sind zusätzliche Modifizierer, mit denen bestimmt werden kann, wie ein bestimmtes Steuerelement funktioniert.</span><span class="sxs-lookup"><span data-stu-id="50078-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="50078-176">SasUiEnum</span><span class="sxs-lookup"><span data-stu-id="50078-176">SasUiEnum</span></span>

<span data-ttu-id="50078-177">Mit dieser Anmerkung können Sie den Wertebereich für ein Steuerelement einschränken.</span><span class="sxs-lookup"><span data-stu-id="50078-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="50078-178">Die Anmerkung enthält eine Zeichenfolge von Werten, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="50078-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="50078-179">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="50078-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="50078-180">SasUiMax</span><span class="sxs-lookup"><span data-stu-id="50078-180">SasUiMax</span></span>

<span data-ttu-id="50078-181">Diese Anmerkung gibt den maximalen Wert des zugeordneten Parameters an.</span><span class="sxs-lookup"><span data-stu-id="50078-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="50078-182">Sie kann nur einem numerisch typisierten Parameter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="50078-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="50078-183">Der Höchstwert des Parameters wird tatsächlich wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="50078-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="50078-184">PARAMETER \_ TYPE MAX ist der Maximale Wert für den \_ Typ, der vom zugeordneten Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50078-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="50078-185">Dies bedeutet, dass der Wert des Parameters unter Berücksichtigung der [SasUiMax-Anmerkung](#sasuimax) wie folgt berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="50078-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="50078-186">Der Standardwert ist FLT \_ MAX, wie in Math.h definiert.</span><span class="sxs-lookup"><span data-stu-id="50078-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="50078-187">SasUiMin</span><span class="sxs-lookup"><span data-stu-id="50078-187">SasUiMin</span></span>

<span data-ttu-id="50078-188">Diese Anmerkung gibt den Minimalwert des zugeordneten Parameters an.</span><span class="sxs-lookup"><span data-stu-id="50078-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="50078-189">Sie kann nur einem beliebigen numerisch typierten Parameter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="50078-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="50078-190">Der Mindestwert des Parameters wird tatsächlich wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="50078-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="50078-191">PARAMETER \_ TYPE MIN ist der \_ Mindestwert für den Typ, der vom zugeordneten Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50078-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="50078-192">Dies bedeutet, dass der Wert des Parameters unter Berücksichtigung der [SasUiMin-Anmerkung](#sasuimin) wie folgt berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="50078-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="50078-193">Der Standardwert ist -FLT \_ MAX, wie in Math.h definiert.</span><span class="sxs-lookup"><span data-stu-id="50078-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="50078-194">SasUiSteps</span><span class="sxs-lookup"><span data-stu-id="50078-194">SasUiSteps</span></span>

<span data-ttu-id="50078-195">Diese Anmerkung gibt die Anzahl der Schritte an, die beim Erhöhen oder Dekrementen des zugeordneten Parameterwerts verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="50078-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="50078-196">Die Anmerkung ist nur für einen numerisch typierten Parameter aussagekräftig.</span><span class="sxs-lookup"><span data-stu-id="50078-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="50078-197">Null gibt an, dass die Hostanwendung eine angemessene Anzahl von Schritten auswählt.</span><span class="sxs-lookup"><span data-stu-id="50078-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="50078-198">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="50078-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="50078-199">SasUiStepsPower</span><span class="sxs-lookup"><span data-stu-id="50078-199">SasUiStepsPower</span></span>

<span data-ttu-id="50078-200">Diese Anmerkung gibt den Exponenten in der Power-Funktion an, die den Bereich \[ 0,0f, 1,0f \] hat.</span><span class="sxs-lookup"><span data-stu-id="50078-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="50078-201">Hostanwendungen müssen beim Berechnen von Parameterwerten die folgende Methode implementieren:</span><span class="sxs-lookup"><span data-stu-id="50078-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="50078-202">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="50078-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="50078-203">SasUiStride</span><span class="sxs-lookup"><span data-stu-id="50078-203">SasUiStride</span></span>

<span data-ttu-id="50078-204">Diese Anmerkung gibt das Inkrement an, das beim Erhöhen oder Dekrementen dieses Werts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="50078-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="50078-205">Im Gegensatz zu [SasUiSteps](#sasuisteps)ist [SasUiStride](#sasuistride) bei einem Spinner-Steuerelement nützlich, bei dem die Daten ungebunden sind und der Benutzer den Parameterwert eher durch Stride als durch eine vordefinierte Anzahl von Schritten erhöhen möchte.</span><span class="sxs-lookup"><span data-stu-id="50078-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="50078-206">Hostanwendungen sollten je nach Steuerelementverhalten um den Wert von SasUiStride wie folgt erhöht (oder dekrementiert) werden:</span><span class="sxs-lookup"><span data-stu-id="50078-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="50078-207">Der Standardwert ist 1,0f.</span><span class="sxs-lookup"><span data-stu-id="50078-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50078-208">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50078-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50078-209">Referenz zu DirectX-Standardanmerkungen und -semantik</span><span class="sxs-lookup"><span data-stu-id="50078-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



