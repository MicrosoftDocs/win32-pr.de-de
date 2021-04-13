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
# <a name="ui-annotation"></a>UI-Anmerkung

Verwenden Sie diese Anmerkung, um einen Effektparameter einem UI-Steuerelement in der Host Umgebung zuzuordnen. Dies ermöglicht es einem Benutzer, einen Effektparameter über die Host Anwendung interaktiv zu steuern.

Dxsas definiert einen Satz von Standard Steuerelementen in Bezug auf das Datenmodell und das grundlegende Verhalten, das von den Autoren von Host Anwendungen erwartet werden kann. Die Steuerelement Anmerkung wird wie folgt verwendet:


```
string SasUiControl = "ControlType";
```



where


```
ControlType
```



ist einer der folgenden:



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| ControlType | BESCHREIBUNG                                                                                                                                                                     | Interner Datentyp                                                                                 | Steuerelement-Eigenschafts Anmerkungen                                                                                 |
| Keine        | Es sollte kein Steuerelement angezeigt werden. Beachten Sie, dass ein Steuerelement sichtbar ist, wenn [sasuivisible](#sasuivisible) den Wert true hat und der Typ des Steuer Elements ein anderer Typ als None ist.                           | –                                                                                                | –                                                                                                          |
| Any         | Dies bedeutet, dass kein spezielles Steuerelement angefordert wird. Das angegebene Steuerelement ist das Ergebnis von Anwendungs definiertem Verhalten.                                                         | –                                                                                                | –                                                                                                          |
| ColorPicker | Stellt einen Farbwert als Farbmuster dar. Der Wert wird in die XYZ-Komponenten des zugeordneten Vektors gepackt. Die W-Komponente des zugeordneten Vektors wird immer auf einen Wert festgelegt. | float *n* , wobei *n* 1 bis 4 ist.                                                            | [Sasuiaufumum](#sasuienum)                                                                                      |
| Richtung   | Ein Richtungsvektor.                                                                                                                                                             | float *n* , wobei *n* zwischen 2 und 4 (einschließlich) liegt.                                                            | Keine                                                                                                         |
| FilePicker  | Ein Dialogfeld, in dem der Benutzer eine Datei durchsuchen und auswählen kann.                                                                                                                  | Zeichenfolge                                                                                             | Keine                                                                                                         |
| ListPicker  | Eine Liste von Zeichen folgen Werten, aus denen der Benutzer einen Eintrag auswählen kann. Die Werte werden aus der [sasuienum](#sasuienum) -Anmerkung generiert.                                         | Ein Array von Zeichen folgen zusammen mit einem ganzzahligen Wert, der den Index des ausgewählten Zeichen folgen Werts enthält. | [Sasuiaufumum](#sasuienum)                                                                                      |
| Numeric     | Ein Satz numerischer Eingabe Steuerelemente (z. b. Textfelder).                                                                                                                         | float *m* x *N* , wobei *m* und *N* 1 bis 4 einschließen.                                               | [Sasuimin](#sasuimin), [sasuimax](#sasuimax), [sasuistride](#sasuistride)                                    |
| Schieberegler      | Ein Satz von Schiebereglern.                                                                                                                                                               | float *m* x *N* , wobei *m* und *N* 1 bis 4 inklusiv sind                                                | [Sasuimin](#sasuimin), [sasuimax](#sasuimax), [sasuisteps](#sasuisteps), [sasuistepspower](#sasuistepspower) |
| String      | Ein Textfeld zum Bearbeiten von Zeichen folgen Inhalten.                                                                                                                                         | Zeichenfolge                                                                                             | Keine                                                                                                         |



 

Wenn der interne Datentyp nicht mit dem Typ des zugeordneten Parameters identisch ist, erfolgt eine Umwandlung, wenn Daten vom Host Anwendungsparameter an den Effect-Parameter übertragen werden.

Der Standardwert ist die Zeichenfolge "None".

## <a name="ui-common-properties"></a>Allgemeine Eigenschaften der Benutzeroberfläche

### <a name="sasuidescription"></a>Sasuideabo

Verwenden Sie diese Anmerkung, um eine Zeichenfolge zum Beschreiben eines Tools anzugeben. Dies kann für Elemente der Benutzeroberfläche, z. b. Quick Infos, verwendet werden.


```
string SasUiDescription = "descriptive string";
```



Beispiel:


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



Der Standardwert ist eine leere Zeichenfolge.

### <a name="sasuilabel"></a>Sasuilabel

Verwenden Sie diese Anmerkung, um eine Zeichenfolge für die Bezeichnung eines beliebigen UI-Steuer Elements anzugeben.


```
string SasUiLabel = "some label;
```



Beispiel:


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



Der Standardwert ist eine leere Zeichenfolge.

### <a name="sasuivisible"></a>Sasuivisible

Verwenden Sie diese Anmerkung, um anzugeben, ob der zugeordnete Parameter dem Benutzer angezeigt werden soll.


```
bool SasUiVisible = false;
```



Wenn der Wert auf true festgelegt ist, sollte die Host Anwendung ein UI-Steuerelement zum Bearbeiten des Parameters mit kommentierten Effekten anzeigen. False gibt an, dass in der Host Anwendung keine Benutzeroberfläche angezeigt wird.

Beispiel:


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



Der Standardwert ist True.

## <a name="ui-control-properties"></a>UI-Steuerelement Eigenschaften

Steuerelement-Eigenschafts Anmerkungen sind zusätzliche modifiziererer, mit denen bestimmt wird, wie ein bestimmtes Steuerelement funktioniert.

### <a name="sasuienum"></a>Sasuiaufumum

Diese Anmerkung ermöglicht es Ihnen, den Wertebereich für ein Steuerelement einzuschränken. Die-Anmerkung enthält eine Zeichenfolge mit Werten, die durch Kommas getrennt sind.

Der Standardwert ist eine leere Zeichenfolge.

### <a name="sasuimax"></a>Sasuimax

Diese Anmerkung gibt den maximalen Wert des zugeordneten Parameters an. Sie kann nur einem numerisch typisierten Parameter zugeordnet werden. Der maximale Wert des-Parameters wird tatsächlich wie folgt berechnet:


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



Der \_ Parametertyp " \_ Max" ist der Höchstwert für den Typ, der vom zugeordneten Parameter verwendet wird. Dies bedeutet, dass der Wert des-Parameters, der die [sasuimax](#sasuimax) -Anmerkung berücksichtigt, wie folgt berechnet wird:


```
ParameterValue = min(NewParameterValue, MaxValue);
```



Der Standardwert ist "SLT Max", \_ wie in "Math. h" definiert.

### <a name="sasuimin"></a>Sasuimin

Diese Anmerkung gibt den minimalen Wert des zugeordneten Parameters an. Sie kann nur mit einem numerisch typisierten Parameter verknüpft werden. Der minimale Wert des-Parameters wird tatsächlich wie folgt berechnet:


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



Der \_ Parametertyp " \_ min" ist der minimale Wert für den Typ, der vom zugeordneten Parameter verwendet wird. Dies bedeutet, dass der Wert des-Parameters, der die [sasuimin](#sasuimin) -Anmerkung berücksichtigt, wie folgt berechnet wird:


```
ParameterValue = max(NewParameterValue, MinValue);
```



Der Standardwert ist-"Max", \_ wie in "Math. h" definiert.

### <a name="sasuisteps"></a>Sasuisteps

Diese Anmerkung gibt die Anzahl der Schritte an, die verwendet werden können, wenn der zugeordnete Parameterwert inkrementiert oder dekrementiert wird. Die-Anmerkung ist nur für einen numerisch typisierten Parameter von Bedeutung. NULL gibt an, dass die Host Anwendung eine angemessene Anzahl von Schritten wählt.

Der Standardwert ist 0.

### <a name="sasuistepspower"></a>Sasuistepspower

Diese Anmerkung gibt den Exponenten in der Power-Funktion an, der den Bereich \[ 0,0 f, 1.0 f hat \] . Host Anwendungen müssen beim Berechnen von Parameterwerten folgende Methode implementieren:


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



Der Standardwert ist 1.0 f.

### <a name="sasuistride"></a>Sasuistride

Diese Anmerkung gibt das Inkrement an, das beim Inkrementieren oder Dekrementieren dieses Werts verwendet werden soll. Im Gegensatz zu [sasuisteps](#sasuisteps)ist [sasuistride](#sasuistride) beispielsweise bei einem Spinner-Steuerelement nützlich, bei dem die Daten unbegrenzt sind und der Benutzer den Parameterwert eher um Stride als eine vordefinierte Anzahl von Schritten erhöhen würde. Host Anwendungen sollten den Wert von sasuistride wie folgt erhöhen (oder je nach Verhalten des Steuer Elements herabsetzen):


```
ParameterValue = ParameterValue +/- SasUiStride
```



Der Standardwert ist 1.0 f.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Standard Anmerkungen und Semantik Referenz](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



