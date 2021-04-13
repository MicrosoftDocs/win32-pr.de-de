---
description: Verwenden Sie diese Anmerkung, um einen Effektparameter einem UI-Steuerelement in der Host Umgebung zuzuordnen. Dies ermöglicht es einem Benutzer, einen Effektparameter über die Host Anwendung interaktiv zu steuern.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: UI-Anmerkung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482678"
---
# <a name="ui-annotation"></a><span data-ttu-id="8bcf9-104">UI-Anmerkung</span><span class="sxs-lookup"><span data-stu-id="8bcf9-104">UI Annotation</span></span>

<span data-ttu-id="8bcf9-105">Verwenden Sie diese Anmerkung, um einen Effektparameter einem UI-Steuerelement in der Host Umgebung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="8bcf9-106">Dies ermöglicht es einem Benutzer, einen Effektparameter über die Host Anwendung interaktiv zu steuern.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="8bcf9-107">Dxsas definiert einen Satz von Standard Steuerelementen in Bezug auf das Datenmodell und das grundlegende Verhalten, das von den Autoren von Host Anwendungen erwartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="8bcf9-108">Die Steuerelement Anmerkung wird wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="8bcf9-109">where</span><span class="sxs-lookup"><span data-stu-id="8bcf9-109">where</span></span>


```
ControlType
```



<span data-ttu-id="8bcf9-110">ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-110">is one of the following:</span></span>



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcf9-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="8bcf9-111">ControlType</span></span> | <span data-ttu-id="8bcf9-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bcf9-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="8bcf9-113">Interner Datentyp</span><span class="sxs-lookup"><span data-stu-id="8bcf9-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="8bcf9-114">Steuerelement-Eigenschafts Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="8bcf9-114">Control Property Annotations</span></span>                                                                                 |
| <span data-ttu-id="8bcf9-115">Keine</span><span class="sxs-lookup"><span data-stu-id="8bcf9-115">None</span></span>        | <span data-ttu-id="8bcf9-116">Es sollte kein Steuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-116">No control should be shown.</span></span> <span data-ttu-id="8bcf9-117">Beachten Sie, dass ein Steuerelement sichtbar ist, wenn [sasuivisible](#sasuivisible) den Wert true hat und der Typ des Steuer Elements ein anderer Typ als None ist.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="8bcf9-118">–</span><span class="sxs-lookup"><span data-stu-id="8bcf9-118">n/a</span></span>                                                                                                | <span data-ttu-id="8bcf9-119">–</span><span class="sxs-lookup"><span data-stu-id="8bcf9-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="8bcf9-120">Any</span><span class="sxs-lookup"><span data-stu-id="8bcf9-120">Any</span></span>         | <span data-ttu-id="8bcf9-121">Dies bedeutet, dass kein spezielles Steuerelement angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-121">This implies that no special control is requested.</span></span> <span data-ttu-id="8bcf9-122">Das angegebene Steuerelement ist das Ergebnis von Anwendungs definiertem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="8bcf9-123">–</span><span class="sxs-lookup"><span data-stu-id="8bcf9-123">n/a</span></span>                                                                                                | <span data-ttu-id="8bcf9-124">–</span><span class="sxs-lookup"><span data-stu-id="8bcf9-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="8bcf9-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="8bcf9-125">ColorPicker</span></span> | <span data-ttu-id="8bcf9-126">Stellt einen Farbwert als Farbmuster dar.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="8bcf9-127">Der Wert wird in die XYZ-Komponenten des zugeordneten Vektors gepackt.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="8bcf9-128">Die W-Komponente des zugeordneten Vektors wird immer auf einen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="8bcf9-129">float *n* , wobei *n* 1 bis 4 ist.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="8bcf9-130">Sasuiaufumum</span><span class="sxs-lookup"><span data-stu-id="8bcf9-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="8bcf9-131">Richtung</span><span class="sxs-lookup"><span data-stu-id="8bcf9-131">Direction</span></span>   | <span data-ttu-id="8bcf9-132">Ein Richtungsvektor.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="8bcf9-133">float *n* , wobei *n* zwischen 2 und 4 (einschließlich) liegt.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="8bcf9-134">Keine</span><span class="sxs-lookup"><span data-stu-id="8bcf9-134">None</span></span>                                                                                                         |
| <span data-ttu-id="8bcf9-135">FilePicker</span><span class="sxs-lookup"><span data-stu-id="8bcf9-135">FilePicker</span></span>  | <span data-ttu-id="8bcf9-136">Ein Dialogfeld, in dem der Benutzer eine Datei durchsuchen und auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="8bcf9-137">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8bcf9-137">string</span></span>                                                                                             | <span data-ttu-id="8bcf9-138">Keine</span><span class="sxs-lookup"><span data-stu-id="8bcf9-138">None</span></span>                                                                                                         |
| <span data-ttu-id="8bcf9-139">ListPicker</span><span class="sxs-lookup"><span data-stu-id="8bcf9-139">ListPicker</span></span>  | <span data-ttu-id="8bcf9-140">Eine Liste von Zeichen folgen Werten, aus denen der Benutzer einen Eintrag auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="8bcf9-141">Die Werte werden aus der [sasuienum](#sasuienum) -Anmerkung generiert.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="8bcf9-142">Ein Array von Zeichen folgen zusammen mit einem ganzzahligen Wert, der den Index des ausgewählten Zeichen folgen Werts enthält.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="8bcf9-143">Sasuiaufumum</span><span class="sxs-lookup"><span data-stu-id="8bcf9-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="8bcf9-144">Numeric</span><span class="sxs-lookup"><span data-stu-id="8bcf9-144">Numeric</span></span>     | <span data-ttu-id="8bcf9-145">Ein Satz numerischer Eingabe Steuerelemente (z. b. Textfelder).</span><span class="sxs-lookup"><span data-stu-id="8bcf9-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="8bcf9-146">float *m* x *N* , wobei *m* und *N* 1 bis 4 einschließen.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="8bcf9-147">[Sasuimin](#sasuimin), [sasuimax](#sasuimax), [sasuistride](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="8bcf9-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="8bcf9-148">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="8bcf9-148">Slider</span></span>      | <span data-ttu-id="8bcf9-149">Ein Satz von Schiebereglern.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="8bcf9-150">float *m* x *N* , wobei *m* und *N* 1 bis 4 inklusiv sind</span><span class="sxs-lookup"><span data-stu-id="8bcf9-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="8bcf9-151">[Sasuimin](#sasuimin), [sasuimax](#sasuimax), [sasuisteps](#sasuisteps), [sasuistepspower](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="8bcf9-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="8bcf9-152">String</span><span class="sxs-lookup"><span data-stu-id="8bcf9-152">String</span></span>      | <span data-ttu-id="8bcf9-153">Ein Textfeld zum Bearbeiten von Zeichen folgen Inhalten.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="8bcf9-154">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8bcf9-154">string</span></span>                                                                                             | <span data-ttu-id="8bcf9-155">Keine</span><span class="sxs-lookup"><span data-stu-id="8bcf9-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="8bcf9-156">Wenn der interne Datentyp nicht mit dem Typ des zugeordneten Parameters identisch ist, erfolgt eine Umwandlung, wenn Daten vom Host Anwendungsparameter an den Effect-Parameter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="8bcf9-157">Der Standardwert ist die Zeichenfolge "None".</span><span class="sxs-lookup"><span data-stu-id="8bcf9-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="8bcf9-158">Allgemeine Eigenschaften der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="8bcf9-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="8bcf9-159">Sasuideabo</span><span class="sxs-lookup"><span data-stu-id="8bcf9-159">SasUiDescription</span></span>

<span data-ttu-id="8bcf9-160">Verwenden Sie diese Anmerkung, um eine Zeichenfolge zum Beschreiben eines Tools anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="8bcf9-161">Dies kann für Elemente der Benutzeroberfläche, z. b. Quick Infos, verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="8bcf9-162">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="8bcf9-163">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="8bcf9-164">Sasuilabel</span><span class="sxs-lookup"><span data-stu-id="8bcf9-164">SasUiLabel</span></span>

<span data-ttu-id="8bcf9-165">Verwenden Sie diese Anmerkung, um eine Zeichenfolge für die Bezeichnung eines beliebigen UI-Steuer Elements anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="8bcf9-166">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="8bcf9-167">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="8bcf9-168">Sasuivisible</span><span class="sxs-lookup"><span data-stu-id="8bcf9-168">SasUiVisible</span></span>

<span data-ttu-id="8bcf9-169">Verwenden Sie diese Anmerkung, um anzugeben, ob der zugeordnete Parameter dem Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="8bcf9-170">Wenn der Wert auf true festgelegt ist, sollte die Host Anwendung ein UI-Steuerelement zum Bearbeiten des Parameters mit kommentierten Effekten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="8bcf9-171">False gibt an, dass in der Host Anwendung keine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="8bcf9-172">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="8bcf9-173">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="8bcf9-174">UI-Steuerelement Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8bcf9-174">UI Control Properties</span></span>

<span data-ttu-id="8bcf9-175">Steuerelement-Eigenschafts Anmerkungen sind zusätzliche modifiziererer, mit denen bestimmt wird, wie ein bestimmtes Steuerelement funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="8bcf9-176">Sasuiaufumum</span><span class="sxs-lookup"><span data-stu-id="8bcf9-176">SasUiEnum</span></span>

<span data-ttu-id="8bcf9-177">Diese Anmerkung ermöglicht es Ihnen, den Wertebereich für ein Steuerelement einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="8bcf9-178">Die-Anmerkung enthält eine Zeichenfolge mit Werten, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="8bcf9-179">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="8bcf9-180">Sasuimax</span><span class="sxs-lookup"><span data-stu-id="8bcf9-180">SasUiMax</span></span>

<span data-ttu-id="8bcf9-181">Diese Anmerkung gibt den maximalen Wert des zugeordneten Parameters an.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="8bcf9-182">Sie kann nur einem numerisch typisierten Parameter zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="8bcf9-183">Der maximale Wert des-Parameters wird tatsächlich wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="8bcf9-184">Der \_ Parametertyp " \_ Max" ist der Höchstwert für den Typ, der vom zugeordneten Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="8bcf9-185">Dies bedeutet, dass der Wert des-Parameters, der die [sasuimax](#sasuimax) -Anmerkung berücksichtigt, wie folgt berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="8bcf9-186">Der Standardwert ist "SLT Max", \_ wie in "Math. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="8bcf9-187">Sasuimin</span><span class="sxs-lookup"><span data-stu-id="8bcf9-187">SasUiMin</span></span>

<span data-ttu-id="8bcf9-188">Diese Anmerkung gibt den minimalen Wert des zugeordneten Parameters an.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="8bcf9-189">Sie kann nur mit einem numerisch typisierten Parameter verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="8bcf9-190">Der minimale Wert des-Parameters wird tatsächlich wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="8bcf9-191">Der \_ Parametertyp " \_ min" ist der minimale Wert für den Typ, der vom zugeordneten Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="8bcf9-192">Dies bedeutet, dass der Wert des-Parameters, der die [sasuimin](#sasuimin) -Anmerkung berücksichtigt, wie folgt berechnet wird:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="8bcf9-193">Der Standardwert ist-"Max", \_ wie in "Math. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="8bcf9-194">Sasuisteps</span><span class="sxs-lookup"><span data-stu-id="8bcf9-194">SasUiSteps</span></span>

<span data-ttu-id="8bcf9-195">Diese Anmerkung gibt die Anzahl der Schritte an, die verwendet werden können, wenn der zugeordnete Parameterwert inkrementiert oder dekrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="8bcf9-196">Die-Anmerkung ist nur für einen numerisch typisierten Parameter von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="8bcf9-197">NULL gibt an, dass die Host Anwendung eine angemessene Anzahl von Schritten wählt.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="8bcf9-198">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="8bcf9-199">Sasuistepspower</span><span class="sxs-lookup"><span data-stu-id="8bcf9-199">SasUiStepsPower</span></span>

<span data-ttu-id="8bcf9-200">Diese Anmerkung gibt den Exponenten in der Power-Funktion an, der den Bereich \[ 0,0 f, 1.0 f hat \] .</span><span class="sxs-lookup"><span data-stu-id="8bcf9-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="8bcf9-201">Host Anwendungen müssen beim Berechnen von Parameterwerten folgende Methode implementieren:</span><span class="sxs-lookup"><span data-stu-id="8bcf9-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="8bcf9-202">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="8bcf9-203">Sasuistride</span><span class="sxs-lookup"><span data-stu-id="8bcf9-203">SasUiStride</span></span>

<span data-ttu-id="8bcf9-204">Diese Anmerkung gibt das Inkrement an, das beim Inkrementieren oder Dekrementieren dieses Werts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="8bcf9-205">Im Gegensatz zu [sasuisteps](#sasuisteps)ist [sasuistride](#sasuistride) beispielsweise bei einem Spinner-Steuerelement nützlich, bei dem die Daten unbegrenzt sind und der Benutzer den Parameterwert eher um Stride als eine vordefinierte Anzahl von Schritten erhöhen würde.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="8bcf9-206">Host Anwendungen sollten den Wert von sasuistride wie folgt erhöhen (oder je nach Verhalten des Steuer Elements herabsetzen):</span><span class="sxs-lookup"><span data-stu-id="8bcf9-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="8bcf9-207">Der Standardwert ist 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="8bcf9-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bcf9-208">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8bcf9-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bcf9-209">DirectX-Standard Anmerkungen und Semantik Referenz</span><span class="sxs-lookup"><span data-stu-id="8bcf9-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



