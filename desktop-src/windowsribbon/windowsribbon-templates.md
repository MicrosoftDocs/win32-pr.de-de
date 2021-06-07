---
title: Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien
description: Steuerelemente, die auf der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menübandframework erzwungen werden und auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl frameworkdefiniert als auch benutzerdefiniert) basieren, wie im Menübandmarkup deklariert. Diese Regeln definieren das adaptive Layoutverhalten des Menübandframework, das beeinflusst, wie steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menübandgrößen angepasst werden.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows-Menüband, Anpassen
- Menüband,Anpassen
- Windows-Menüband, SizeDefinition-Vorlagen
- Menüband, SizeDefinition-Vorlagen
- Windows-Menüband, benutzerdefinierte Vorlagen
- Menüband, benutzerdefinierte Vorlagen
- Anpassen des Windows-Menübands
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6576a672aa8c3d328a341370a7568595e988908
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444141"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien

Steuerelemente, die auf der Menüband-Befehlsleiste gehostet werden, unterliegen Layoutregeln, die vom Windows-Menübandframework erzwungen werden und auf einer Kombination aus Standardverhalten und Layoutvorlagen (sowohl frameworkdefiniert als auch benutzerdefiniert) basieren, wie im Menübandmarkup deklariert. Diese Regeln definieren das adaptive Layoutverhalten des Menübandframework, das beeinflusst, wie steuerelemente in der Befehlsleiste zur Laufzeit an verschiedene Menübandgrößen angepasst werden.

-   [Introduction (Einführung)](#introduction)
    -   [MenübandgrößeDefinitionsvorlagen](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Benutzerdefinierte Vorlagen](#custom-templates)
-   [Verwandte Themen](#related-topics)

## <a name="introduction"></a>Einführung

Adaptives Layout, wie durch das Menübandframework definiert, ist die Fähigkeit aller Steuerelemente auf der Menübandbenutzeroberfläche, ihre Organisation, Größe, Format und relative Skalierung basierend auf Änderungen an der Größe des Menübands zur Laufzeit dynamisch anzupassen.

Das Framework macht adaptive Layoutfunktionen über eine Reihe von Markupelementen verfügbar, die für das Angeben und Anpassen verschiedener Layoutverhaltensverhalten dediert sind. Eine Sammlung von Vorlagen namens [**SizeDefinitions**](windowsribbon-element-sizedefinition.md)wird durch das Framework definiert, von denen jede verschiedene Steuerelement- und Layoutszenarien unterstützt. Das Framework unterstützt jedoch auch benutzerdefinierte Vorlagen, wenn die vordefinierten Vorlagen nicht die Benutzeroberflächenerfahrung oder layouts bereitstellen, die für eine Anwendung erforderlich sind.

Um Steuerelemente in einem bevorzugten Layout mit einer bestimmten Menübandgröße anzuzeigen, funktionieren sowohl vordefinierte Vorlagen als auch benutzerdefinierte Vorlagen in Verbindung mit dem [**ScalingPolicy-Element.**](windowsribbon-element-scalingpolicy.md) Dieses Element enthält ein Manifest der Größeneinstellungen, die das Framework beim Rendern des Menübands als Leitfaden verwendet.

> [!Note]  
> Das Menübandframework bietet Standardlayoutverhalten, das auf einer Reihe integrierter Heuristiken für die Organisation und Darstellung von Steuerelementen zur Laufzeit basiert, ohne dass die [**vordefinierten SizeDefinition-Vorlagen benötigt**](windowsribbon-element-sizedefinition.md) werden. Diese Funktion ist jedoch nur für Prototypzwecke vorgesehen.

 

### <a name="ribbon-sizedefinition-templates"></a>MenübandgrößeDefinitionsvorlagen

Das Menübandframework bietet einen umfassenden Satz von [**SizeDefinition-Vorlagen,**](windowsribbon-element-sizedefinition.md) die Größe und Layoutverhalten für eine Gruppe von Menüband-Steuerelementen angeben. [](windowsribbon-controls-group.md) Diese Vorlagen decken die gängigsten Szenarien zum Organisieren von Steuerelementen in einer Menübandanwendung ab.

Um eine konsistente Benutzeroberfläche für Menübandanwendungen zu erzwingen, erzwingt jede [**SizeDefinition-Vorlage**](windowsribbon-element-sizedefinition.md) Einschränkungen für die Steuerelemente oder die Von ihr unterstützten Steuerelementfamilien.

Die Schaltflächenfamilie von Steuerelementen umfasst beispielsweise Folgendes:

-   [Button](windowsribbon-controls-button.md) (Schaltfläche)
-   [Umschaltfläche](windowsribbon-controls-togglebutton.md)
-   [Dropdownschaltfläche](windowsribbon-controls-dropdownbutton.md)
-   [Schaltfläche "Teilen"](windowsribbon-controls-splitbutton.md)
-   [Dropdownkatalog](windowsribbon-controls-dropdowngallery.md)
-   [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md)
-   [Dropdownliste Farbwähler](windowsribbon-controls-dropdowncolorpicker.md)

Die Eingabefamilie von Steuerelementen umfasst Folgendes:

-   [Kombinationsfeld](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

[Kontrollkästchen und](windowsribbon-controls-checkbox.md) [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) gehören weder zur Schaltflächenfamilie noch zur Eingabefamilie. Diese beiden Steuerelemente können nur verwendet werden, wenn sie explizit in einer [**SizeDefinition-Vorlage angegeben**](windowsribbon-element-sizedefinition.md) sind.

Im Folgenden finden Sie eine Liste der [**SizeDefinition-Vorlagen**](windowsribbon-element-sizedefinition.md) mit einer Beschreibung des Layouts und der Steuerelemente, die für jede Vorlage zulässig sind.

> [!IMPORTANT]
> Wenn die im Markup deklarierten Steuerelemente nicht genau dem in der zugeordneten [](windowsribbon-compilationerrors.md) Vorlage definierten Steuerelementtyp, [](windowsribbon-intentcl.md) der Reihenfolge und der Menge zugeordnet sind, wird ein Validierungsfehler vom Markupcompiler protokolliert, und die Kompilierung wird beendet.

 



OneButton

Ein Steuerelement der Schaltflächenfamilie.<br/> Nur große Gruppen werden unterstützt.<br/>

![Abbildung der Vorlage "onebutton sizedefinition".](images/overviews/sizedefinition-onebutton.png)

TwoButtons

Zwei Steuerelemente der Schaltflächenfamilie.<br/> Es werden nur die Gruppengrößen Groß und Mittel unterstützt.<br/>

![Abbildung der Vorlage "twobuttons large sizedefinition".](images/overviews/sizedefinition-twobuttons-large.png)

![Abbildung der Vorlage twobuttons medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

Drei Steuerelemente der Schaltflächenfamilie.<br/> Es werden nur die Gruppengrößen Groß und Mittel unterstützt.<br/>

![Abbildung der Vorlage "Threebuttons large sizedefinition".](images/overviews/sizedefinition-threebuttons-large.png)

![Abbildung der Vorlage "Threebuttons medium sizedefinition".](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Drei Steuerelemente der Schaltflächenfamilie.<br/> Die erste Schaltfläche wird in allen drei Größen deutlich dargestellt.<br/>

![Abbildung der Vorlage threebuttons-onebigandtwosmall large sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![Abbildung der Vorlage threebuttons-onebigandtwosmall medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![Abbildung der Vorlage threebuttons-onebigandtwosmall small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

Drei Steuerelemente der Schaltflächenfamilie, die von einem einzelnen CheckBox-Steuerelement begleitet werden.<br/> Es werden nur die Gruppengrößen Groß und Mittel unterstützt.<br/>

![Abbildung der Vorlage threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![Abbildung der Vorlage threebuttonsandonecheckbox medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

Vier Steuerelemente der Schaltflächenfamilie.<br/>

![Abbildung der Vorlage "Fourbuttons large sizedefinition".](images/overviews/sizedefinition-fourbuttons-large.png)

![Abbildung der Vorlage "Fourbuttons medium sizedefinition".](images/overviews/sizedefinition-fourbuttons-medium.png)

![Abbildung der Small-SizeDefinition-Vorlage für vierButtons.](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

Fünf Steuerelemente der Schaltflächenfamilie.<br/>

![Abbildung der Vorlage "Fivebuttons large sizedefinition".](images/overviews/sizedefinition-fivebuttons-large.png)

![Abbildung der Vorlage fivebuttons medium sizedefinition.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Abbildung der Small-SizeDefinition-Vorlage für fivebuttons.](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

Fünf Steuerelemente der Schaltflächenfamilie und eine optionale sechste Schaltfläche.<br/>

![Abbildung der Vorlage "fiveorsixbuttons large sizedefinition".](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![Abbildung der Vorlage fiveorsixbuttons medium sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![Abbildung der Small SizeDefinition-Vorlage für fiveorsixbuttons.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

Sechs Steuerelemente der Schaltflächenfamilie.<br/>

![Abbildung der Vorlage "large sizedefinition" von sixbuttons.](images/overviews/sizedefinition-sixbuttons-large.png)

![Abbildung der Vorlage "sixbuttons medium sizedefinition".](images/overviews/sizedefinition-sixbuttons-medium.png)

![Abbildung der Vorlage "Sixbuttons small sizedefinition".](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Sechs Steuerelemente der Schaltflächenfamilie (alternative Darstellung).<br/>

![Abbildung der Vorlage "sixbuttons-twocolumns large sizedefinition".](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns medium sizedefinition template.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![Abbildung der Vorlage "sixbuttons-twocolumns small sizedefinition".](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

Sieben Steuerelemente der Schaltflächenfamilie.<br/>

![Abbildung der Vorlage "sevenbuttons large sizedefinition".](images/overviews/sizedefinition-sevenbuttons-large.png)

![Abbildung der Vorlage "sevenbuttons mediumsizedefinition".](images/overviews/sizedefinition-sevenbuttons-medium.png)

![Abbildung der Vorlage "Sevenbuttons small sizedefinition".](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

Acht Steuerelemente der Schaltflächenfamilie.<br/>

![Abbildung der Vorlage "eightbuttons-lastthreesmall large sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Abbildung der Vorlage "eightbuttons-lastthreesmall medium sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![Abbildung der Vorlage "eightbuttons-lastthreesmall small sizedefinition".](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Acht Steuerelemente der Schaltflächenfamilie (alternative Darstellung).<br/>

> [!Note]  
> Alle mit dieser Vorlage deklarierten Steuerelementelemente müssen in zwei [**ControlGroup-Elementen**](windowsribbon-element-controlgroup.md) enthalten sein: eines für die ersten fünf Elemente und eines für die letzten drei Elemente.

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



![Abbildung der Vorlage "eightbuttons large sizedefinition".](images/overviews/sizedefinition-eightbuttons-large.png)

![Abbildung der Vorlage "Eightbuttons medium sizedefinition".](images/overviews/sizedefinition-eightbuttons-medium.png)

![Abbildung der Vorlage "eightbuttons small sizedefinition".](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

Neun Steuerelemente der Schaltflächenfamilie.

![Abbildung der Vorlage "ninebuttons large sizedefinition".](images/overviews/sizedefinition-ninebuttons-large.png)

![Abbildung der Vorlage "ninebuttons medium sizedefinition".](images/overviews/sizedefinition-ninebuttons-medium.png)

![Abbildung der Vorlage "ninebuttons small sizedefinition".](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

Zehn Steuerelemente der Schaltflächenfamilie.

![Abbildung der Vorlage "tenbuttons large sizedefinition".](images/overviews/sizedefinition-tenbuttons-large.png)

![Abbildung der Vorlage "Tenbuttons medium sizedefinition".](images/overviews/sizedefinition-tenbuttons-medium.png)

![Abbildung der Vorlage "tenbuttons small sizedefinition".](images/overviews/sizedefinition-tenbuttons-small.png)

ElferButtons

Elf Steuerelemente der Schaltflächenfamilie.

![Abbildung der Vorlage "elfbuttons large sizedefinition".](images/overviews/sizedefinition-elevenbuttons-large.png)

![Abbildung der Vorlage für die mittlere Größendefinition von elfButtons.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![Abbildung der Vorlage "elfbuttons small sizedefinition".](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

Ein [**FontControl -Zeichen.**](windowsribbon-element-fontcontrol.md)

Es werden nur große und mittlere Gruppengrößen unterstützt.

> [!IMPORTANT]
> Das Einschließen von [**FontControl**](windowsribbon-element-fontcontrol.md) in eine benutzerdefinierte Vorlagendefinition wird vom Framework nicht unterstützt.

 

![Abbildung der Onefontcontrol-Vorlage "large sizedefinition".](images/overviews/sizedefinition-onefontcontrol-large.png)

![Abbildung der Vorlage onefontcontrol medium sizedefinition.](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

Ein [**InRibbonGallery-Steuerelement.**](windowsribbon-element-inribbongallery.md)

Nur große und kleine Gruppengrößen werden unterstützt.

![Abbildung der Vorlage oneinribbongallery large sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![Abbildung der Vorlage oneinribbongallery small sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

Ein [**InRibbonGallery-Steuerelement**](windowsribbon-element-inribbongallery.md) und ein Steuerelement der Schaltflächenfamilie.

Nur große und kleine Gruppengrößen werden unterstützt.

![Abbildung der Vorlage inribbongalleryandbigbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![Abbildung der Vorlage inribbongalleryandbigbigbutton small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Ein [Menübandkatalog-Steuerelement](windowsribbon-controls-inribbongallery.md) und zwei oder drei Steuerelemente der Schaltflächenfamilie.

Der Katalog wird auf die Popupdarstellung in den Gruppengrößen "Mittel" und "Klein" reduziert.

![Abbildung der Vorlage inribbongalleryandbuttons-galleryscalesfirst large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Abbildung der Vorlage inribbongalleryandbuttons-galleryscalesfirst medium sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![Abbildung der Vorlage inribbongalleryandbuttons-galleryscalesfirst small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

Eine komplexe Anordnung von 32 Steuerelementen der Schaltflächenfamilie (die meisten sind optional).

> [!Note]  
> Abgesehen von der optionalen Schaltfläche in voller Größe der großen ButtonGroups-Vorlage müssen alle mit dieser Vorlage deklarierten Steuerelementelemente in [**ControlGroup-Elementen**](windowsribbon-element-controlgroup.md) enthalten sein.

 

Im folgenden Beispiel wird das Markup veranschaulicht, das erforderlich ist, um alle 32 Steuerelementelemente (erforderlich und optional) mit dieser Vorlage anzuzeigen.


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



![Abbildung der GroßenDefinitionsvorlage für Schaltflächengruppen.](images/overviews/sizedefinition-buttongroups-large.png)

![Abbildung der Vorlage für mittlere Größendefinition von Schaltflächengruppen.](images/overviews/sizedefinition-buttongroups-medium.png)

![Abbildung der Vorlage für kleine Größendefinitionen von Schaltflächengruppen.](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

Zwei Steuerelemente der Eingabefamilie (das zweite ist optional), gefolgt von einer komplexen Anordnung von 29 Steuerelementen der Schaltflächenfamilie (die meisten sind optional).

Es werden nur große und mittlere Gruppengrößen unterstützt.

> [!Note]  
> Alle mit dieser Vorlage deklarierten Steuerelementelemente müssen in [**ControlGroup-Elementen**](windowsribbon-element-controlgroup.md) enthalten sein.

 

Im folgenden Beispiel wird das Markup veranschaulicht, das zum Anzeigen aller (erforderlichen und optionalen) Steuerelementelemente mit dieser Vorlage erforderlich ist.


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



![Abbildung der Vorlage "buttongroups", "large sizedefinition".](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Abbildung der Vorlage "buttongroups's medium sizedefinition".](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

Zwei Steuerelemente der Schaltflächenfamilie (beide optional), gefolgt von zwei oder drei Schaltflächen- oder Eingabefamilien-Steuerelementen.

Es werden nur große und mittlere Gruppengrößen unterstützt.

![Abbildung der Vorlage bigbuttonsandsmallbuttonsorinputs large sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Abbildung der Vorlage bigbuttonsandsmallbuttonsorinputs medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Beispiel für "Basic SizeDefinition"

Im folgenden Codebeispiel wird veranschaulicht, wie eine [**SizeDefinition-Vorlage**](windowsribbon-element-sizedefinition.md) im Menübandmarkup deklariert wird.

*OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) wird für dieses spezielle Beispiel verwendet, aber alle Frameworkvorlagen werden auf ähnliche Weise angegeben.


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



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Beispiel für komplexe GrößeDefinition mit Skalierungsrichtlinien

Das Reduzierungsverhalten von [**SizeDefinition-Vorlagen**](windowsribbon-element-sizedefinition.md) kann durch die Verwendung von Skalierungsrichtlinien im Menübandmarkup gesteuert werden.

Das [**ScalingPolicy-Element**](windowsribbon-element-scalingpolicy.md) enthält ein Manifest von [**ScalingPolicy.IdealSizes-**](windowsribbon-element-scalingpolicy-idealsizes.md) und [**Scale-Deklarationen,**](windowsribbon-element-scale.md) die adaptive Layouteinstellungen für ein oder mehrere [**Group-Elemente**](windowsribbon-element-group.md) angeben, wenn die Größe des Menübands geändert wird.

> [!Note]  
> Es wird dringend empfohlen, ausreichende Skalierungsrichtliniendetails anzugeben, sodass die meisten, wenn nicht alle [**Gruppenelemente**](windowsribbon-element-group.md) einem [**Scale-Element**](windowsribbon-element-scale.md) zugeordnet werden, bei dem das *Size-Attribut* gleich `Popup` ist. Auf diese Weise kann das Framework das Menüband in der kleinstmöglichen Größe rendern und die breite palette von Anzeigegeräten unterstützen, bevor automatisch ein Bildlaufmechanismus eingeführt wird.

 

Im folgenden Codebeispiel wird ein [**ScalingPolicy-Manifest**](windowsribbon-element-scalingpolicy.md) veranschaulicht, das eine [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition-Einstellung**](windowsribbon-element-sizedefinition.md) für jede von vier Gruppen von Steuerelementen auf einer Registerkarte **Home** angibt. Darüber hinaus werden [**Skalierungselemente**](windowsribbon-element-scale.md) angegeben, um das Reduzierungsverhalten jeder Gruppe in absteigender Größenreihenfolge zu beeinflussen.


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

Wenn das Standardlayoutverhalten und die vordefinierten [**SizeDefinition-Vorlagen**](windowsribbon-element-sizedefinition.md) nicht die Flexibilität oder Unterstützung für ein bestimmtes Layoutszenario bieten, werden benutzerdefinierte Vorlagen vom Menübandframework über das [**Ribbon.SizeDefinitions-Element**](windowsribbon-element-ribbon-sizedefinitions.md) unterstützt.

Benutzerdefinierte Vorlagen können auf zwei Arten deklariert werden: eine eigenständige Methode, die das [**Ribbon.SizeDefinitions-Element**](windowsribbon-element-ribbon-sizedefinitions.md) zum Deklarieren von wiederverwendbaren, benannten Vorlagen oder eine [**Gruppenspezifische**](windowsribbon-element-group.md)Inlinemethode verwendet.

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



### <a name="inline-template"></a>Inlinevorlage

Die folgenden Codebeispiele veranschaulichen eine einfache benutzerdefinierte Inlinevorlage für eine Gruppe von vier Schaltflächen.

Dieser Codeabschnitt zeigt die Befehlsdeklarationen für eine Gruppe von Schaltflächen. Hier werden auch große und kleine Imageressourcen angegeben.


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



In diesem Codeabschnitt wird veranschaulicht, wie Sie große, mittlere und kleine [**GroupSizeDefinition-Vorlagen**](windowsribbon-element-groupsizedefinition.md) definieren, um die vier Schaltflächen in verschiedenen Größen und Layouts anzuzeigen. Die [**ScalingPolicy-Deklaration**](windowsribbon-element-scalingpolicy.md) für die Registerkarte definiert, welche Vorlage für eine Gruppe von Steuerelementen verwendet wird, basierend auf der Größe und dem Speicherplatz des Menübands, die für die aktive Registerkarte erforderlich sind.


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



Die folgenden Abbildungen zeigen, wie die Vorlagen aus dem vorherigen Beispiel auf die Menüband-Benutzeroberfläche angewendet werden, um eine Verringerung der Menübandgröße zu ermöglichen.



|  Typ  |      Image                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| Large  | ![Abbildung einer inline großen benutzerdefinierten Vorlage.](images/overviews/sizedefinition-custom-large.png)   |
| Medium | ![Abbildung einer benutzerdefinierten Inlinevorlage mit mittlerem Inline-](images/overviews/sizedefinition-custom-medium.png) |
| Small  | ![Abbildung einer kleinen benutzerdefinierten Inlinevorlage.](images/overviews/sizedefinition-custom-small.png)   |
| Popup  | ![Abbildung einer benutzerdefinierten Inline-Popupvorlage.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Skalieren**](windowsribbon-element-scale.md)
</dt> <dt>

[**Gruppe**](windowsribbon-element-group.md)
</dt> </dl>

 

 





