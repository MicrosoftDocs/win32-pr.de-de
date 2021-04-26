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
# <a name="ui-annotation"></a>Benutzeroberflächenanmerkung

Verwenden Sie diese Anmerkung, um einem Ui-Steuerelement in der Hostumgebung einen Effect-Parameter zuzuordnen. Dadurch kann ein Benutzer einen Effect-Parameter interaktiv über die Hostanwendung steuern.

DXSAS definiert eine Reihe von Standardsteuerelementen im Hinblick auf das Datenmodell und das grundlegende Verhalten, die Autoren von Hostanwendungen erwarten können. Die Steuerelementanmerkung wird wie folgt verwendet:


```
string SasUiControl = "ControlType";
```



where


```
ControlType
```



ist einer der folgenden:



| ControlType | BESCHREIBUNG                                                                                                                                                                     | Interner Datentyp                                                                                 | Steuerelementeigenschaftenanmerkungen                                                                                 |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Keine        | Es sollte kein Steuerelement angezeigt werden. Beachten Sie, dass ein Steuerelement sichtbar ist, wenn [SasUiVisible](#sasuivisible) true ist und der Steuerelementtyp ein anderer Typ als None ist.                           | –                                                                                                | –                                                                                                          |
| Any         | Dies bedeutet, dass kein spezielles Steuerelement angefordert wird. Das dargestellte Steuerelement ist das Ergebnis eines anwendungsdefiniertes Verhaltens.                                                         | –                                                                                                | –                                                                                                          |
| ColorPicker | Stellen Sie einen Farbwert als Farbwatch dar. Der Wert wird in die XYZ-Komponenten des zugeordneten Vektors gepackt. Die W-Komponente des zugeordneten Vektors ist immer auf 1 festgelegt. | float *N,* wobei *N* 1 bis 4 einschließlich ist.                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| Direction   | Ein Richtungsvektor.                                                                                                                                                             | float *N,* wobei *N* 2 bis einschließlich 4 ist.                                                            | Keine                                                                                                         |
| FilePicker  | Ein Dialogfeld, in dem der Benutzer eine Datei durchsuchen und auswählen kann.                                                                                                                  | Zeichenfolge                                                                                             | Keine                                                                                                         |
| ListPicker  | Eine Liste von Zeichenfolgenwerten, aus denen der Benutzer einen Eintrag auswählen kann. Die Werte werden aus der [SasUiEnum-Anmerkung](#sasuienum) generiert.                                         | Ein Array von Zeichenfolgen zusammen mit einem ganzzahligen Wert, der den Index des ausgewählten Zeichenfolgenwerts enthält. | [SasUiEnum](#sasuienum)                                                                                      |
| Numeric     | Eine Reihe von numerischen Eingabesteuerelementen (z. B. Textfelder).                                                                                                                         | float *M* x *N,* *wobei M* und *N* inklusive 1 bis 4 sind.                                               | [SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiStride](#sasuistride)                                    |
| Schieberegler      | Eine Gruppe von Schiebereglern.                                                                                                                                                               | float *M* x *N,* *wobei M* und *N* inklusive 1 bis 4 sind                                                | [SasUiMin,](#sasuimin) [SasUiMax,](#sasuimax) [SasUiSteps,](#sasuisteps) [SasUiStepsPower](#sasuistepspower) |
| Zeichenfolge      | Ein Textfeld zum Bearbeiten von Zeichenfolgeninhalten.                                                                                                                                         | Zeichenfolge                                                                                             | Keine                                                                                                         |



 

Wenn der interne Datentyp nicht mit dem Typ des zugeordneten Parameters identisch ist, erfolgt die Umwandlung, wenn Daten aus dem Hostanwendungsparameter in den Effect-Parameter übertragen werden.

Der Standardwert ist die Zeichenfolge "None".

## <a name="ui-common-properties"></a>Allgemeine Eigenschaften der Benutzeroberfläche

### <a name="sasuidescription"></a>SasUiDescription

Verwenden Sie diese Anmerkung, um eine Zeichenfolge zum Beschreiben eines Tools anzugeben. Dies kann für Benutzeroberflächenelemente wie QuickInfos verwendet werden.


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

### <a name="sasuilabel"></a>SasUiLabel

Verwenden Sie diese Anmerkung, um eine Zeichenfolge zum Bezeichnen eines beliebigen Ui-Steuerelements anzugeben.


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

### <a name="sasuivisible"></a>SasUiVisible

Verwenden Sie diese Anmerkung, um anzugeben, ob der zugeordnete Parameter dem Benutzer angezeigt werden soll.


```
bool SasUiVisible = false;
```



Wenn diese Einstellung auf TRUE festgelegt ist, sollte die Hostanwendung ein Ui-Steuerelement zum Bearbeiten des Parameters mit Anmerkungen anzeigen. False gibt an, dass in der Hostanwendung keine Benutzeroberfläche angezeigt wird.

Beispiel:


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



Der Standardwert ist True.

## <a name="ui-control-properties"></a>Eigenschaften des UI-Steuerelements

Steuerelementeigenschaftenanmerkungen sind zusätzliche Modifizierer, mit denen bestimmt werden kann, wie ein bestimmtes Steuerelement funktioniert.

### <a name="sasuienum"></a>SasUiEnum

Mit dieser Anmerkung können Sie den Wertebereich für ein Steuerelement einschränken. Die Anmerkung enthält eine Zeichenfolge von Werten, die durch Kommas getrennt sind.

Der Standardwert ist eine leere Zeichenfolge.

### <a name="sasuimax"></a>SasUiMax

Diese Anmerkung gibt den maximalen Wert des zugeordneten Parameters an. Sie kann nur einem numerisch typisierten Parameter zugeordnet werden. Der Höchstwert des Parameters wird tatsächlich wie folgt berechnet:


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



PARAMETER \_ TYPE MAX ist der Maximale Wert für den \_ Typ, der vom zugeordneten Parameter verwendet wird. Dies bedeutet, dass der Wert des Parameters unter Berücksichtigung der [SasUiMax-Anmerkung](#sasuimax) wie folgt berechnet wird:


```
ParameterValue = min(NewParameterValue, MaxValue);
```



Der Standardwert ist FLT \_ MAX, wie in Math.h definiert.

### <a name="sasuimin"></a>SasUiMin

Diese Anmerkung gibt den Minimalwert des zugeordneten Parameters an. Sie kann nur einem beliebigen numerisch typierten Parameter zugeordnet werden. Der Mindestwert des Parameters wird tatsächlich wie folgt berechnet:


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



PARAMETER \_ TYPE MIN ist der \_ Mindestwert für den Typ, der vom zugeordneten Parameter verwendet wird. Dies bedeutet, dass der Wert des Parameters unter Berücksichtigung der [SasUiMin-Anmerkung](#sasuimin) wie folgt berechnet wird:


```
ParameterValue = max(NewParameterValue, MinValue);
```



Der Standardwert ist -FLT \_ MAX, wie in Math.h definiert.

### <a name="sasuisteps"></a>SasUiSteps

Diese Anmerkung gibt die Anzahl der Schritte an, die beim Erhöhen oder Dekrementen des zugeordneten Parameterwerts verwendet werden können. Die Anmerkung ist nur für einen numerisch typierten Parameter aussagekräftig. Null gibt an, dass die Hostanwendung eine angemessene Anzahl von Schritten auswählt.

Der Standardwert ist 0.

### <a name="sasuistepspower"></a>SasUiStepsPower

Diese Anmerkung gibt den Exponenten in der Power-Funktion an, die den Bereich \[ 0,0f, 1,0f \] hat. Hostanwendungen müssen beim Berechnen von Parameterwerten die folgende Methode implementieren:


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



Der Standardwert ist 1,0f.

### <a name="sasuistride"></a>SasUiStride

Diese Anmerkung gibt das Inkrement an, das beim Erhöhen oder Dekrementen dieses Werts verwendet werden soll. Im Gegensatz zu [SasUiSteps](#sasuisteps)ist [SasUiStride](#sasuistride) bei einem Spinner-Steuerelement nützlich, bei dem die Daten ungebunden sind und der Benutzer den Parameterwert eher durch Stride als durch eine vordefinierte Anzahl von Schritten erhöhen möchte. Hostanwendungen sollten je nach Steuerelementverhalten um den Wert von SasUiStride wie folgt erhöht (oder dekrementiert) werden:


```
ParameterValue = ParameterValue +/- SasUiStride
```



Der Standardwert ist 1,0f.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu DirectX-Standardanmerkungen und -semantik](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



