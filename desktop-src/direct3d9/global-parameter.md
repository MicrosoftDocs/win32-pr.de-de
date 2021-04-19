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
# <a name="global-parameter"></a>Globaler Parameter

Jeder dxsas-kompatible Effekt muss mindestens einen einzelnen globalen Effektparameter mit der globalen Semantik definieren. Der globale Parameter kann auch eine oder mehrere optionale Anmerkungen verwenden. Die Syntax lautet wie folgt:


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



Dabei gilt:

-   VariableName ist ein vom Benutzer angegebener ASCII-Text Zeichenfolgen-Variablenname.
-   Sasglobal ist das semantische Schlüsselwort, mit dem dieser Parameter als globaler dxsas-Parameter identifiziert wird.
-   Sasversion ist die einzige erforderliche Anmerkung.
-   Optionalannotations kann Folgendes umfassen:
    -   [Saseffectauthor](#saseffectauthor)
    -   [Saseffectauthoringsoftware](#saseffectauthoringsoftware)
    -   [Saseffectcategory](#saseffectcategory)
    -   [Saseffectcompany](#saseffectcompany)
    -   [Saseffectdescription](#saseffectdescription)
    -   [Saseffecthelp](#saseffecthelp)
    -   [Saseffectrevision](#saseffectrevision)

## <a name="sasversion"></a>Sasversion

Die einzige erforderliche Anmerkung ist sasversion. Es wird wie folgt deklariert:


```
int3 SasVersion = { major, minor, revision };
```



Dabei gilt:

-   Major gibt die dxsas-Hauptversion an. Hauptversionen von dxsas können tiefgreifende Änderungen am Satz von Semantik und Anmerkungen enthalten, die definiert sind. Semantik und Anmerkungen können hinzugefügt und entfernt werden, und im Allgemeinen ist die Abwärtskompatibilität mit früheren Releases nicht sichergestellt.
-   "Minor" gibt die SAS-neben Version an. Kleinere Releases von dxsas können das Hinzufügen neuer Semantik oder Anmerkungen einschließen. Darüber hinaus können Semantik und Anmerkungen im dxsas-Standard als veraltet markiert werden. Veraltete Semantik und Anmerkungen müssen von Host Anwendungen weiterhin unterstützt werden, Sie können jedoch eine Warnungs Diagnose ausgeben, wenn eine solche Semantik oder Anmerkung verwendet wird. Neben Versionen sind abwärts kompatibel mit früheren Versionen.
-   Revision gibt die dxsas-Revision an. Revisionen von dxsas sind nur als Mittel zum Beheben von Fehlern, Entfernen von Mehrdeutigkeit und verfeinern des Standards vorhanden. Revisionen des Standards sind abwärts kompatibel mit früheren Versionen.

Die aktuelle Version ist 1.0.0. Es gibt keinen Standardwert für diese Anmerkung.

## <a name="saseffectauthor"></a>Saseffectauthor

Dadurch wird die Person deklariert, die den Effekt erstellt hat. Es wird wie folgt deklariert:


```
string SasEffectAuthor = "value";
```



wobei value eine Zeichenfolge ist, die den Effekt Autor identifiziert. Der Standardwert ist eine leere Zeichenfolge.

## <a name="saseffectauthoringsoftware"></a>Saseffectauthoringsoftware

Dadurch wird die Software deklariert, auf der der Effekt erstellt wurde. Es wird wie folgt deklariert:


```
string SasEffectAuthoringSoftware = "value";
```



Dabei ist value eine Zeichenfolge, die die Auswirkungen der Authoring Software identifiziert. Der Standardwert ist eine leere Zeichenfolge.

## <a name="saseffectcategory"></a>Saseffectcategory

Dadurch wird die Kategorie "Effekt" deklariert. Es wird wie folgt deklariert:


```
string SasEffectCategory = "value";
```



Dabei ist value eine Zeichenfolge, die die Effekt Kategorie bezeichnet. Der Standardwert ist eine leere Zeichenfolge. Die Kategorie wird über einen Pfad ähnlich dem Wert ausgedrückt, wobei der Schrägstrich als Trennzeichen verwendet wird. Effekte können nur zu einer Kategorie gehören, da es keine Syntax zum Ausdrücken von Inklusions in mehrere Pfade innerhalb eines einzelnen saseffectcategory-Werts gibt. Der Wert dieser Anmerkung wird von der Host Anwendung nicht als Unterscheidung nach Groß-/Kleinschreibung behandelt.

## <a name="saseffectcompany"></a>Saseffectcompany

Dadurch wird das Unternehmen deklariert, das den Effekt erzeugt hat. Es wird wie folgt deklariert:


```
string SasEffectCompany = "value";
```



Dabei ist value eine Zeichenfolge, die den Namen des Unternehmens identifiziert, das den Effekt besitzt. Der Standardwert ist eine leere Zeichenfolge.

## <a name="saseffectdescription"></a>Saseffectdescription

Dies beschreibt den Effekt. Es wird wie folgt deklariert:


```
string SasEffectDescription = "value";
```



wobei value eine Zeichenfolge ist, die den Effekt beschreibt. Der Standardwert ist eine leere Zeichenfolge.

## <a name="saseffecthelp"></a>Saseffecthelp

Dabei handelt es sich um eine Hilfe Zeichenfolge, die dem Benutzer angezeigt werden kann, wenn Hilfe zu den zugehörigen Effekten angefordert wird. Es wird wie folgt deklariert:


```
string SasEffectHelp = "value";
```



Dabei ist value eine Zeichenfolge, die angezeigt werden kann, wenn der Benutzerhilfe anfordert. Der Standardwert ist eine leere Zeichenfolge.

## <a name="saseffectrevision"></a>Saseffectrevision

Diese Anmerkung ermöglicht es Tools und Benutzern, die Revisionsnummer der zugehörigen Wirkungs Datei aufzuzeichnen. Beispielsweise könnten Benutzer geeignete Schlüsselwörter in den Wert dieser Anmerkung einfügen, um die Schlüsselwort Ersetzung in Ihrer bevorzugten Revisions Steuerungssoftware aufzurufen. Es wird wie folgt deklariert:


```
string SasEffectRevision = "value";
```



Dabei ist value eine Zeichenfolge, die die Auswirkung Revision bezeichnet. Der Standardwert ist eine leere Zeichenfolge.

## <a name="examples"></a>Beispiele

Es folgt ein Beispiel, in dem nur die einzige erforderliche Anmerkung verwendet wird:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



Im folgenden finden Sie ein Beispiel, in dem die erforderliche Anmerkung und einige optionale Anmerkungen verwendet werden:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Standard Anmerkungen und Semantik Referenz](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



