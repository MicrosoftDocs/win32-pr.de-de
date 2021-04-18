---
title: Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien
description: Steuerelemente, die in der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menü Band Framework erzwungen werden, und basieren auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl Framework-definiert als auch Benutzer definiert), wie im Menü Band Markup Diese Regeln definieren das Verhalten des adaptiven Layouts des Multifunktionsleisten-Frameworks, das beeinflussen, wie die Steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menü Bandgrößen angepasst werden.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows-Menüband, anpassen
- Multifunktionsleiste, anpassen
- Windows-Multifunktionsleiste, sizedefinition-Vorlagen
- Multifunktionsleiste, sizedefinition-Vorlagen
- Windows-Menüband, benutzerdefinierte Vorlagen
- Multifunktionsleiste, benutzerdefinierte Vorlagen
- Anpassen des Menübands von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b12618f88576cddeff119534215e501216193c3
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2020
ms.locfileid: "104569881"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien

Steuerelemente, die in der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menü Band Framework erzwungen werden, und basieren auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl Framework-definiert als auch Benutzer definiert), wie im Menü Band Markup Diese Regeln definieren das Verhalten des adaptiven Layouts des Multifunktionsleisten-Frameworks, das beeinflussen, wie die Steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menü Bandgrößen angepasst werden.

-   [Introduction (Einführung)](#introduction)
    -   [Menü Band-sizedefinition-Vorlagen](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Benutzerdefinierte Vorlagen](#custom-templates)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das Adaptive Layout, wie im Menüband-Framework definiert, ist die Fähigkeit aller Steuerelemente auf der Multifunktionsleisten-Benutzeroberfläche, die Organisation, Größe, das Format und die relative Skalierung basierend auf den Änderungen an der Größe des Menübands zur Laufzeit dynamisch anzupassen.

Das Framework stellt mithilfe eines Satzes von Markup Elementen, die für die Angabe und Anpassung verschiedener layoutverhaltensweisen vorgesehen sind, Adaptive Layoutfunktionen zur Verfügung. Eine Auflistung von Vorlagen, die als [**sizedefinitions**](windowsribbon-element-sizedefinition.md)bezeichnet wird, wird durch das Framework definiert, von denen jedes verschiedene Steuerungs-und Layoutszenarien unterstützt. Das Framework unterstützt jedoch auch benutzerdefinierte Vorlagen, wenn die vordefinierten Vorlagen nicht die Benutzeroberfläche oder die Layouts bereitstellen, die für eine Anwendung erforderlich sind.

Zum Anzeigen von Steuerelementen in einem bevorzugten Layout auf einer bestimmten Menü Band Größe funktionieren sowohl vordefinierte Vorlagen als auch benutzerdefinierte Vorlagen in Verbindung mit dem [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Element. Dieses Element enthält ein Manifest von Größen Einstellungen, das vom Framework beim Rendern des Menübands als Leitfaden verwendet wird.

> [!Note]  
> Das Menüband-Framework bietet Standardlayout-Verhalten, das auf einer Reihe integrierter Heuristik für die Organisation und Darstellung von Steuerelementen zur Laufzeit basiert, ohne dass die vordefinierten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen benötigt werden. Diese Funktion ist jedoch nur für prototypenzwecke gedacht.

 

### <a name="ribbon-sizedefinition-templates"></a>Menü Band-sizedefinition-Vorlagen

Das Menüband-Framework bietet einen umfassenden Satz von [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen, die das Größen-und Layoutverhalten für eine [Gruppe](windowsribbon-controls-group.md) von Menü Band Steuerelementen angeben. Diese Vorlagen behandeln die häufigsten Szenarien zum Organisieren von Steuerelementen in einer Menüband-Anwendung.

Um eine konsistente Benutzer Darstellung über Multifunktionsleisten-Anwendungen hinweg zu erzwingen, erzwingt jede [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage Beschränkungen für die Steuerelemente oder die von ihr unterstützte Steuerelement Familie.

Die Schaltflächen Familie der Steuerelemente umfasst z. b. Folgendes:

-   [Schaltfläche](windowsribbon-controls-button.md)
-   [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md)
-   [Dropdown Schaltfläche](windowsribbon-controls-dropdownbutton.md)
-   [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)
-   [Dropdown-Katalog](windowsribbon-controls-dropdowngallery.md)
-   [Split Button-Katalog](windowsribbon-controls-splitbuttongallery.md)
-   [Dropdown-Farbauswahl](windowsribbon-controls-dropdowncolorpicker.md)

Die Eingabe Familie der Steuerelemente umfasst Folgendes:

-   [Kombinations Feld](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

Das [Kontrollkästchen](windowsribbon-controls-checkbox.md) und der [in-Ribbon-](windowsribbon-controls-inribbongallery.md) Katalog gehören weder zur Schaltflächen Familie noch zur Eingabe Familie. Diese beiden Steuerelemente können nur verwendet werden, wenn Sie explizit in einer [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage angegeben werden.

Im folgenden finden Sie eine Liste der [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen mit einer Beschreibung des Layouts und der Steuerelemente, die für jede Vorlage zulässig sind.

> [!IMPORTANT]
> Wenn die in Markup deklarierten Steuerelemente nicht exakt der Steuerung von Typ, Reihenfolge und Menge zugeordnet werden, die in der zugeordneten Vorlage definiert ist, wird vom [Markup Compiler](windowsribbon-intentcl.md) ein [Validierungs Fehler](windowsribbon-compilationerrors.md) protokolliert, und die Kompilierung wird beendet.

 



OneButton

Ein Schaltflächen-familiensteuer Element.<br/> Es wird nur eine große Gruppengröße unterstützt.<br/>

![Bild der oneButton-sizedefinition-Vorlage.](images/overviews/sizedefinition-onebutton.png)

Twobuttons

Zwei Schaltflächen-familiensteuer Elemente.<br/> Nur große und mittlere Gruppengrößen werden unterstützt.<br/>

![Bild der Vorlage "twobuttons Large sizedefinition".](images/overviews/sizedefinition-twobuttons-large.png)

![Bild der "twobuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-twobuttons-medium.png)

Drei Schaltflächen

Drei Schaltflächen-familiensteuer Elemente.<br/> Nur große und mittlere Gruppengrößen werden unterstützt.<br/>

![Bild der großen sizedefinition-Vorlage mit drei Schaltflächen.](images/overviews/sizedefinition-threebuttons-large.png)

![Bild der mittleren sizedefinition-Vorlage mit drei Buttons.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Drei Schaltflächen-familiensteuer Elemente.<br/> Die erste Schaltfläche wird in allen drei Größen hervorgehoben dargestellt.<br/>

![Bild der drei-Schaltflächen: onebigandtwosmall Large sizedefinition-Vorlage.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![Abbildung von "Dreifach Buttons": onebigandtwosmall Mittel sizedefinition-Vorlage.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![Abbildung von "Dreifach Buttons": onebigandtwosmall Small sizedefinition-Vorlage.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

Dreibuttonsandonecheckbox

Drei Schaltflächen-familiensteuer Elemente, die von einem einzelnen CheckBox-Steuerelement begleitet werden<br/> Nur große und mittlere Gruppengrößen werden unterstützt.<br/>

![Bild der großen sizedefinition-Vorlage "dreibuttonsandonecheckbox".](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![Bild der "dreibuttonsandonecheckbox mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

Fourbuttons

Vier Schaltflächen-familiensteuer Elemente.<br/>

![Bild der Vorlage "große sizedefinition" von fourbuttons.](images/overviews/sizedefinition-fourbuttons-large.png)

![Bild der "fourbuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-fourbuttons-medium.png)

![Bild der "fourbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-fourbuttons-small.png)

Schaltflächen

Fünf Schaltflächen-familiensteuer Elemente.<br/>

![Bild der Vorlage "große sizedefinition" für "fvebuttons".](images/overviews/sizedefinition-fivebuttons-large.png)

![Bild der "fvebuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Bild der Vorlage "Small sizedefinition" von "List".](images/overviews/sizedefinition-fivebuttons-small.png)

"Fveorsixbuttons"

Fünf Schaltflächen-familiensteuer Elemente und eine optionale sechste Schaltfläche.<br/>

![Bild der Vorlage "große sizedefinition" von "fveorsixbuttons".](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![Bild der "fveorsixbuttons mittelgroßen sizedefinition"-Vorlage.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![Bild der "tvorsixbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

Sixbuttons

Sechs Schaltflächen-familiensteuer Elemente.<br/>

![Bild der sixbuttons-Vorlage "große sizedefinition".](images/overviews/sizedefinition-sixbuttons-large.png)

![Bild der sixbuttons mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-medium.png)

![Bild der sixbuttons Small sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Sechs Schaltflächen-familiensteuer Elemente (alternative Darstellung).<br/>

![Bild von sixbuttons-twocolumns Large sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns mittlere sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![Bild von sixbuttons-twocolumns Small sizedefinition-Vorlage.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

Sevenbuttons

Sieben Schaltflächen-familiensteuer Elemente.<br/>

![Bild der Vorlage "große sizedefinition" von sevenbuttons.](images/overviews/sizedefinition-sevenbuttons-large.png)

![Bild der Vorlage "mediensizedefinition" von sevenbuttons.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![Bild der "sevenbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-sevenbuttons-small.png)

Eightbuttons

Acht Schaltflächen-familiensteuer Elemente.<br/>

![Bild der Vorlage "eightbuttons-lastthreesmall Large sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Bild der Vorlage "eightbuttons-lastthreesmall Mittel sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![Bild der Vorlage "eightbuttons-lastthreesmall Small sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Acht Schaltflächen-familiensteuer Elemente (alternative Darstellung).<br/>

> [!Note]  
> Alle Steuerelemente, die mit dieser Vorlage deklariert werden, müssen in zwei [**controlgroup**](windowsribbon-element-controlgroup.md) -Elementen enthalten sein: einer für die ersten fünf Elemente und einer für die letzten drei Elemente.

<br/> Im folgenden Beispiel wird das für diese Vorlage erforderliche Markup veranschaulicht.<br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![Bild der "eightbuttons Large sizedefinition"-Vorlage.](images/overviews/sizedefinition-eightbuttons-large.png)

![Bild der Vorlage "eightbuttons mittlere sizedefinition".](images/overviews/sizedefinition-eightbuttons-medium.png)

![Bild der eightbuttons Small sizedefinition-Vorlage.](images/overviews/sizedefinition-eightbuttons-small.png)

Neunschalt Flächen

Neun Schaltflächen-familiensteuer Elemente.

![Abbildung von "neunschalt Flächen große sizedefinition"-Vorlage.](images/overviews/sizedefinition-ninebuttons-large.png)

![Bild der "neunbuttons mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-ninebuttons-medium.png)

![Abbildung von "neunbuttons Small sizedefinition Template".](images/overviews/sizedefinition-ninebuttons-small.png)

Tenbuttons

Zehn Schaltflächen-familiensteuer Elemente.

![Bild der "tenbuttons Large sizedefinition"-Vorlage.](images/overviews/sizedefinition-tenbuttons-large.png)

![Bild der Vorlage "tenbuttons Mittel (mittlere sizedefinition)".](images/overviews/sizedefinition-tenbuttons-medium.png)

![Bild der "tenbuttons Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-tenbuttons-small.png)

Elevumbuttons

Elf Steuerelemente der Schaltflächen-Familie.

![Bild der elevenbuttons Large sizedefinition-Vorlage.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Bild der elevenbuttons mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![Bild der elevenbuttons Small sizedefinition-Vorlage.](images/overviews/sizedefinition-elevenbuttons-small.png)

Onefontcontrol

Ein [**FontControl**](windowsribbon-element-fontcontrol.md)-Element.

Nur große und mittlere Gruppengrößen werden unterstützt.

> [!IMPORTANT]
> Das Einschließen eines [**FontControl**](windowsribbon-element-fontcontrol.md) -Elements in eine benutzerdefinierte Vorlagen Definition wird vom Framework nicht unterstützt.

 

![Bild der Vorlage "große sizedefinition" von onefontcontrol.](images/overviews/sizedefinition-onefontcontrol-large.png)

![Bild der "onefontcontrol mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-onefontcontrol-medium.png)

Oneinribbongallery

Ein [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Steuerelement.

Nur große und Kleine Gruppengrößen werden unterstützt.

![Bild der Vorlage "große sizedefinition" von oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![Bild der "oneinribbongallery Small sizedefinition"-Vorlage.](images/overviews/sizedefinition-oneinribbongallery-small.png)

Inribbongalleryandbigbutton

Ein [**inribbongallery**](windowsribbon-element-inribbongallery.md) -Steuerelement und ein Schaltflächen-familiensteuer Element.

Nur große und Kleine Gruppengrößen werden unterstützt.

![Bild der inribbongalleryandbigbutton Large sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![Bild der inribbongalleryandbigbutton Small sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Ein [in-Ribbon](windowsribbon-controls-inribbongallery.md) -Katalog Steuerelement und zwei oder drei Schaltflächen-familiensteuer Elemente.

Der Katalog wird auf die Popup Darstellung in mittelgroßen und kleinen Gruppengrößen reduziert.

![Bild der inribbongalleryandbuttons-galleryscalesfirst Large sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Bild der inribbongalleryandbuttons-galleryscalesfirst mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![Bild der inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition-Vorlage.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

Buttongroups

Eine komplexe Anordnung von 32-Schaltflächen-familiensteuer Elementen (die meisten sind optional).

> [!Note]  
> Abgesehen von der optionalen vollständigen Schaltfläche der Vorlage für große buttongroups müssen alle Steuerelemente, die mit dieser Vorlage deklariert werden, in [**controlgroup**](windowsribbon-element-controlgroup.md) -Elementen enthalten sein.

 

Das folgende Beispiel zeigt das Markup, das erforderlich ist, um alle 32-Steuerelement Elemente (erforderlich und optional) mit dieser Vorlage anzuzeigen.


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![Bild der buttongroups Large sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroups-large.png)

![Bild der buttongroups mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroups-medium.png)

![Bild der buttongroups Small sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroups-small.png)

Buttongroupsandinputs

Zwei eingabefamiliensteuerelemente (die zweite ist optional), gefolgt von einer komplexen Anordnung von 29 Schaltflächen-familiensteuer Elementen (die meisten sind optional).

Nur große und mittlere Gruppengrößen werden unterstützt.

> [!Note]  
> Alle Steuerelemente, die mit dieser Vorlage deklariert werden, müssen in [**controlgroup**](windowsribbon-element-controlgroup.md) -Elementen enthalten sein.

 

Das folgende Beispiel zeigt das Markup, das erforderlich ist, um alle Steuerelemente (erforderlich und optional) mit dieser Vorlage anzuzeigen.


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![Bild der buttongroupsandinputs Large sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Bild der buttongroupsandinputs mittelgroßen sizedefinition-Vorlage.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

Bigbuttonsandsmallbuttonsorinputs

Zwei Schaltflächen-familiensteuer Elemente (optional), gefolgt von zwei oder drei Schaltflächen-oder eingabefamiliensteuerelementen.

Nur große und mittlere Gruppengrößen werden unterstützt.

![Abbildung der Vorlage "große sizedefinition" von bigbuttonsandsmallbuttonsorinputs.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Bild der "bigbuttonsandsmallbuttonsorinputs mittlere sizedefinition"-Vorlage.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Einfaches Beispiel für sizedefinition

Das folgende Codebeispiel veranschaulicht, wie Sie eine [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage im Menü Band Markup deklarieren.

Die " *oneinribbongallery* " [**sizedefinition**](windowsribbon-element-sizedefinition.md) wird für dieses spezielle Beispiel verwendet, aber alle frameworkvorlagen sind auf ähnliche Weise angegeben.


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Komplexes sizedefinition-Beispiel mit Skalierungs Richtlinien

Das reduzierende Verhalten von [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen kann durch die Verwendung von Skalierungs Richtlinien im Menüband-Markup gesteuert werden.

Das [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Element enthält ein Manifest der [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) -und [**Scale**](windowsribbon-element-scale.md) -Deklarationen, die Adaptive Layouteinstellungen für ein oder mehrere [**Gruppen**](windowsribbon-element-group.md) Elemente angeben, wenn die Größe des Menübands geändert wird.

> [!Note]  
> Es wird dringend empfohlen, dass ausreichend Details zur Skalierungs Richtlinie angegeben werden, sodass die meisten, wenn nicht alle [**Gruppen**](windowsribbon-element-group.md) Elemente einem [**Scale**](windowsribbon-element-scale.md) -Element zugeordnet sind, in dem das *size* -Attribut gleich ist `Popup` . Auf diese Weise kann das-Framework das Menüband mit der kleinsten Größe darstellen und die breiteste Palette von Anzeigegeräten unterstützen, bevor es automatisch einen scrollmechanismus einführt.

 

Das folgende Codebeispiel veranschaulicht ein [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Manifest, das eine [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Einstellung für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Home** angibt. Außerdem werden [**Skalierungs**](windowsribbon-element-scale.md) Elemente angegeben, um das reduzierende Verhalten der einzelnen Gruppen in absteigender Reihenfolge zu beeinflussen.


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a>Benutzerdefinierte Vorlagen

Wenn das Standardlayoutverhalten und die vordefinierten [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlagen die Flexibilität oder Unterstützung für ein bestimmtes Layoutszenario nicht bieten, werden benutzerdefinierte Vorlagen durch das Ribbon [**. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) -Element vom Multifunktionsleisten-Framework unterstützt.

Benutzerdefinierte Vorlagen können auf zweierlei Weise deklariert werden: eine eigenständige Methode, die das [**Ribbon. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) -Element verwendet, um wiederverwendbare, benannte Vorlagen oder eine Inline Methode, die [**Gruppen**](windowsribbon-element-group.md)spezifisch ist, zu deklarieren.

### <a name="standalone-template"></a>Eigenständige Vorlage

Das folgende Codebeispiel veranschaulicht eine einfache, wiederverwendbare benutzerdefinierte Vorlage.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a>Inline Vorlage

Die folgenden Codebeispiele veranschaulichen eine einfache Inline benutzerdefinierte Vorlage für eine Gruppe von vier Schaltflächen.

In diesem Code Abschnitt werden die Befehls Deklarationen für eine Gruppe von Schaltflächen angezeigt. Hier werden auch große und kleine Bild Ressourcen angegeben.


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



In diesem Code Abschnitt wird veranschaulicht, wie Sie die Vorlagen "Large", "Medium" und "Small [**groupsizedefinition**](windowsribbon-element-groupsizedefinition.md) " definieren, um die vier Schaltflächen in verschiedenen Größen und Layouts anzuzeigen. Die [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) -Deklaration für die Registerkarte definiert, welche Vorlage für eine Gruppe von Steuerelementen basierend auf der Menü Band Größe und dem für die aktive Registerkarte erforderlichen Speicherplatz verwendet wird.


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



Die folgenden Bilder veranschaulichen, wie die Vorlagen aus dem vorherigen Beispiel auf die Multifunktionsleisten-Benutzeroberfläche angewendet werden, um eine Verkleinerung der Menüband-Größe zu ermöglichen.



|        |                                                                                                    |
|--------|----------------------------------------------------------------------------------------------------|
| Groß  | ![Bild einer großen benutzerdefinierten Inline Vorlage.](images/overviews/sizedefinition-custom-large.png)   |
| Medium | ![Bild einer benutzerdefinierten Inline-Vorlage.](images/overviews/sizedefinition-custom-medium.png) |
| Klein  | ![Bild einer kleinen benutzerdefinierten Inline Vorlage.](images/overviews/sizedefinition-custom-small.png)   |
| Popup  | ![Bild einer benutzerdefinierten Inline-Popup Vorlage.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Sizedefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Migen**](windowsribbon-element-scale.md)
</dt> <dt>

[**Gruppe**](windowsribbon-element-group.md)
</dt> </dl>

 

 





