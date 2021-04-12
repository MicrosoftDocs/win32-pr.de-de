---
title: Voreinstellungen
description: Voreinstellungen
ms.assetid: fb2ccd8b-eda2-414a-870c-85b658f40eb9
keywords:
- Visualisierungen, Voreinstellungen
- benutzerdefinierte Visualisierungen, Voreinstellungen
- Visualisierungen, Balken Voreinstellung
- benutzerdefinierte Visualisierungen, Balken Voreinstellung
- Visualisierungen, Wellen Voreinstellung
- benutzerdefinierte Visualisierungen, Wellen Voreinstellung
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Funktion "Rendering", Voreinstellungen
- Visualisierungen, getpresettitle-Funktion
- benutzerdefinierte Visualisierungen, getpresettitle-Funktion
- Getpresettitle-Funktion
- Enumerationen, Visualisierungs Voreinstellungen
- Visualisierungen, Enumerationen
- benutzerdefinierte Visualisierungen, Enumerationen
- Visualisierungen, Ressourcen Header und Zeichen folgen
- benutzerdefinierte Visualisierungen, Ressourcen Header und Zeichen folgen
- Voreinstellungen in Visualisierungen, Balken Voreinstellung
- Voreinstellungen in Visualisierungen, Wellen Voreinstellung
- Voreinstellungen in Visualisierungen, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e024427d19da0a30f54d9ebc0590feedb8d0f97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206611"
---
# <a name="presets"></a>Voreinstellungen

Voreinstellungen werden als Möglichkeit zur Verfügung gestellt, um unterschiedliche Effekte aus derselben Visualisierung zu haben. Sie könnten z. b. einen Glanzeffekt erstellen, der von einem Codeblock generiert wurde, aber eine Voreinstellung verwenden, um die Farbe des Leucht ens zu bestimmen. Die Voreinstellungs Namen sind u. u. rot, grün und blau.

Der Assistent definiert zwei Voreinstellungen für den generierten Code. Eine wird als Balken bezeichnet, und die andere wird als Wave bezeichnet. In der voreingestellten Leiste werden Balken angezeigt, die die Aktivität im Audiospektrum anzeigen, und die Wellenform Daten werden verwendet. In der Wave-Voreinstellung wird eine ausspiel Linie angezeigt, die die audiopotenz des Waveforms anzeigt.

Wenn Sie die voreingestellten Informationen ändern, müssen Sie auch die folgenden Teile des generierten Codes ändern.

## <a name="render-function"></a>Rendering-Funktion

Die **iwmpeffects:: Rendering** -Funktion befindet sich in der Datei " *ProjectName*. cpp", wobei *ProjectName* der Projektname ist, den Sie beim Ausführen des Assistenten ausgewählt haben.

Der generierte Code in der Funktion " **Rendering** " verwendet eine Switch-Anweisung, um zwischen zwei Voreinstellungen zu wählen. Die aktuelle Voreinstellung ist das, was der Benutzer in Windows Media Player auswählt. Wenn Sie den Code für eine bestimmte Voreinstellung ändern oder eine Voreinstellung hinzufügen oder subtrahieren möchten, ändern Sie die Switch-Anweisung entsprechend.

Die beiden Voreinstellungen werden durch die **voreingestellten \_ leisten** und **voreingestellten \_** bereichsenumerationen definiert. Die Auswahl der Voreinstellung, die aufgerufen wird, wird durch m \_ nvoreinstellung definiert.

## <a name="getpresettitle"></a>Getpresettitle

Die **iwmpeffects:: getpresettitle** -Funktion befindet sich in der Datei " *ProjectName*. cpp", wobei *ProjectName* der Projektname ist, den Sie beim Ausführen des Assistenten ausgewählt haben.

Mit der **getpresettitle** -Funktion werden die Beziehungen zwischen den vordefinierten Enumerationen und den Zeichen folgen Ressourcen festgelegt. Die **enumerationsvorschauleisten \_** und der **voreingestellte \_ Bereich** werden vom Assistenten generiert und verwenden die Zeichen folgen Ressourcen-IDs \_ barationsetname und IDs \_ scopepresetname.

Sie müssen die Enumerationen und Zeichen folgen Ressourcen ändern, wenn Sie Voreinstellungen hinzufügen, subtrahieren oder ändern.

## <a name="preset-enumerations"></a>Voreingestellte Enumerationen

Die voreingestellte Enumeration wird in der Datei *ProjectName*. h definiert, wobei *ProjectName* der Projektname ist, den Sie beim Durchlaufen des Assistenten ausgewählt haben.

Die-Enumeration definiert die aktuellen beiden Voreinstellungen und die Anzahl. Wenn Sie Voreinstellungen hinzufügen oder subtrahieren oder die Enumeration ändern, stellen Sie sicher, dass Sie diese Enumeration ändern, sodass die Anzahl und die Reihenfolge der Voreinstellungen korrekt ist. Diese Enumeration wird verwendet, um sicherzustellen, dass Sie die richtige Voreinstellung in der Funktion " **Rendering** " aufzurufen.

## <a name="resource-header"></a>Ressourcen Header

Sie müssen die Ressourcen für die Namen Ihrer Voreinstellung in der Header Datei "Resource. h" festlegen. Die aktuellen Voreinstellungen werden wie folgt definiert:


```C++
#define IDS_BARSPRESETNAME              102
#define IDS_SCOPEPRESETNAME             103
```



Wenn Sie Voreinstellungen hinzufügen oder subtrahieren, müssen Sie den Ressourcen Header und die Zahlen für diese ändern.

## <a name="resource-strings"></a>Ressourcen Zeichenfolgen

Die tatsächlichen Namen der Voreinstellungen sind in der Ressourcen Datei *ProjectName* dll. rc definiert, wobei *ProjectName* der Projektname ist, den Sie beim Durchlaufen des Assistenten ausgewählt haben. Sie können diese Datei manuell bearbeiten oder den Ressourcen-Editor verwenden, der in Microsoft Visual C++ enthalten ist.

Die generierten Namen sind der Name der Visualisierung und die jeweilige Voreinstellung. Die Ressourcen Datei für den generierten Code definiert Sie wie folgt:


```C++
IDS_BARSPRESETNAME      "projectname Bars"
IDS_SCOPEPRESETNAME     "projectname Wave"
```



Dabei ist *ProjectName* der Name des Projekt namens, den Sie beim Durchlaufen des Assistenten ausgewählt haben. An dieser Stelle ändern Sie die tatsächlichen Namen der Voreinstellungen, und auf diese Weise werden Sie von Windows Media Player verwiesen und angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren des Codes**](implementing-your-code.md)
</dt> </dl>

 

 




