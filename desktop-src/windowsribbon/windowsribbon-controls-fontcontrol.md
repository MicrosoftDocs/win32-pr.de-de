---
title: Schriftart-Steuerelement
description: Um die Integration und Konfiguration der Schriftart Unterstützung in Anwendungen zu vereinfachen, die Textverarbeitungs-und Textbearbeitungs Funktionen erfordern, bietet das Windows-Menüband-Framework ein spezielles Schriftart Steuerelement, das eine Vielzahl von Schriftart Eigenschaften wie z. b. Schriftart Name, Stil, Punktgröße und Effekte verfügbar macht.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390575"
---
# <a name="font-control"></a>Schriftart-Steuerelement

Um die Integration und Konfiguration der Schriftart Unterstützung in Anwendungen zu vereinfachen, die Textverarbeitungs-und Textbearbeitungs Funktionen erfordern, bietet das Windows-Menüband-Framework ein spezielles Schriftart Steuerelement, das eine Vielzahl von Schriftart Eigenschaften wie z. b. Schriftart Name, Stil, Punktgröße und Effekte verfügbar macht.

-   [Introduction (Einführung)](#introduction)
-   [Eine konsistente Darstellung](#a-consistent-experience)
-   [Einfache Integration und Konfiguration](#easy-integration-and-configuration)
-   [Ausrichtung mit allgemeinen GDI-Text Strukturen](#alignment-with-common-gdi-text-structures)
-   [Hinzufügen eines FontControl-Elements](#add-a-fontcontrol)
    -   [Deklarieren eines FontControl im Markup](#declaring-a-fontcontrol-in-markup)
    -   [Schriftart Steuerelement-Eigenschaften](#font-control-properties)
-   [Definieren eines FontControl-Befehls Handlers](#define-a-fontcontrol-command-handler)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Das Schriftart Steuerelement ist ein zusammengesetztes Steuerelement, das aus Schaltflächen, UMSCHALT Flächen, Dropdown-Listenfeldern und Kombinations Feldern besteht, die alle zum Angeben einer bestimmten Schriftart Eigenschaft oder Formatierungs Option verwendet werden.

Der folgende Screenshot zeigt das Menüband-Schriftart-Steuerelement in WordPad für Windows 7.

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>Eine konsistente Darstellung

Das Schriftart-Steuerelement ist ein integriertes Menüband-Steuerelement und verbessert die allgemeinen Funktionen für Schriftart Verwaltung, Auswahl und Formatierung und bietet eine umfangreiche, konsistente Benutzer Funktionalität für alle multifunktionsleistenanwendungen.

Diese konsistente Darstellung umfasst

-   Standardisierte Formatierung und Auswahl von Schriftarten in Menüband-Anwendungen.
-   Standardisierte Schriftart Darstellung über Menüband-Anwendungen hinweg.
-   Automatisch, in Windows 7, die Schriftart Aktivierung, die auf der Einstellung zum **anzeigen** oder **Ausblenden** der einzelnen Schriftart in der Systemsteuerung der **Schriftarten** basiert. Das Schriftart Steuerelement zeigt nur die Schriftarten an, die auf **anzeigen** festgelegt sind.
    > [!Note]  
    > In Windows Vista bietet die **Schriftarten** -Systemsteuerung keine Funktionen zum **anzeigen** oder **Ausblenden** , sodass alle Schriftarten aktiviert sind.

     

-   Schriftart Verwaltung, die direkt über das-Steuerelement verfügbar ist.

    Der folgende Screenshot zeigt, dass der Zugriff auf die Schrift **Arten** -Systemsteuerung direkt über das Schriftart Steuerelement möglich ist.

    ![Screenshot der Schriftart Familien Liste in WordPad für Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   Unterstützung für die automatische Vorschau.
-   Verfügbar machen von Schriftarten, die für einen Benutzer am relevantesten sind, z. b.
    -   Lokalisierte Schriftart Listen für internationale Benutzer.
    -   Auf dem Eingabegerät basierende Schriftart Listen.

    > [!Note]  
    > Die Unterstützung für diese Funktionalität ist auf keiner Plattform verfügbar, die älter als Windows 7 ist.

     

## <a name="easy-integration-and-configuration"></a>Einfache Integration und Konfiguration

Durch die Bereitstellung von standardmäßigen, wiederverwendbaren und leicht verwendbaren Funktionen erleichtert das Menüband-Schriftart Steuerelement das Integrieren der Schriftart Unterstützung in eine Anwendung.

Die Details der Schriftart Auswahl und-Formatierung werden in ein eigenständiges logisches Element umschließt, das

-   Eliminiert die komplexe Verwaltung von Steuerungs Abhängigkeiten, die typisch für die Implementierungen von Schriftart Steuerelementen sind.
-   Erfordert einen einzelnen Befehls Handler für alle Funktionen, die von den untergeordneten Steuerelementen für Schriftart Steuerelemente verfügbar gemacht werden.

Mit diesem einzelnen Befehls Handler kann das Schriftart Steuerelement die Funktionalität verschiedener untergeordneter Steuerelemente intern verwalten. ein unter Steuerelement interagiert niemals direkt mit der Anwendung, unabhängig von der Funktion.

Weitere Funktionen des Schriftart Steuer Elements sind u. a.

-   Automatische, dpi-fähige Generierung eines WYSIWYG (was Sie sehen, was Sie sehen) Bitmap-Darstellung für jede Schriftart im Menü **Schriftfamilie** .
-   Integration von [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .
-   Lokalisierte Bitmaps und Quick Infos der Schriftart Familie.
-   Schriftart Enumeration, Gruppierung und Metadaten für die Verwaltung und Darstellung von Schriftarten.
    > [!Note]  
    > Die Unterstützung für diese Funktionalität ist auf keiner Plattform verfügbar, die älter als Windows 7 ist.

     

-   Die Farbauswahl für **Textfarbe** und **Texthervorhebungen** , die das [Dropdown-Farb](windowsribbon-controls-dropdowncolorpicker.md) Auswahl Verhalten der Multifunktionsleiste widerspiegeln.
-   Unterstützung der automatischen Vorschau von allen Galerie basierten untergeordneten Steuerelementen auf Schriftart Steuerelementen: **Schriftfamilie**, **Schrift** Grad, **Textfarbe** und **Text** Hervorhebungs Farbe.

## <a name="alignment-with-common-gdi-text-structures"></a>Ausrichtung mit allgemeinen GDI-Text Strukturen

[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) -Text Stapel Komponenten werden verwendet, um die Schriftart Auswahl und Formatierungsfunktionen über das Menüband-Schriftart Steuerelement verfügbar zu machen. Die verschiedenen von der [LOGFONT-Struktur](/windows/win32/api/wingdi/ns-wingdi-logfonta), der [chooonfont-Struktur](/windows/win32/api/commdlg/ns-commdlg-choosefonta)und der [CHARFORMAT2-Struktur](/windows/win32/api/richedit/ns-richedit-charformat2a) unterstützten Schriftart Funktionen werden durch die untergeordneten Steuerelemente verfügbar gemacht, die im Schriftart Steuerelement enthalten sind.

Die untergeordneten Steuerelemente, die im Schriftart Steuerelement angezeigt werden, sind von der im Menüband-Markup deklarierten *fonttype* -Vorlage abhängig. Die *fonttype* -Vorlagen (im folgenden Abschnitt ausführlich erläutert) sind so konzipiert, dass Sie mit den allgemeinen [Windows Graphics Device Interface-Textstrukturen (GDI)](../gdi/windows-gdi.md) ausgerichtet werden.

## <a name="add-a-fontcontrol"></a>Hinzufügen eines FontControl-Elements

In diesem Abschnitt werden die grundlegenden Schritte zum Hinzufügen eines Schriftart Steuer Elements zu einer Menü Bandanwendung beschrieben.

### <a name="declaring-a-fontcontrol-in-markup"></a>Deklarieren eines FontControl im Markup

Wie andere Menü Band Steuerelemente wird das Schriftart Steuerelement im Markup mit einem [**FontControl**](windowsribbon-element-fontcontrol.md) -Element deklariert und einer Befehls Deklaration über eine Befehls-ID zugeordnet. Wenn die Anwendung kompiliert wird, wird die Befehls-ID verwendet, um den Befehl an einen Befehls Handler in der Host Anwendung zu binden.

> [!Note]  
> Wenn keine Befehls-ID mit dem [**FontControl**](windowsribbon-element-fontcontrol.md) im Markup deklariert ist, wird eine von dem Framework generiert.

 

Da die untergeordneten Steuerelemente des Schriftart-Steuer Elements nicht direkt verfügbar gemacht werden, ist die Anpassung des Schriftart-Steuer Elements auf drei vom Framework definierte *fonttype* -Layoutvorlagen beschränkt.

Weitere Anpassungen des Schriftart Steuer Elements können durch Kombinieren der Layoutvorlage mit [**FontControl**](windowsribbon-element-fontcontrol.md) -Attributen wie *ishighlightbuttonvisible*, *isstrikepulbuttonvisible* und *isunderlinebuttonvisible* durchgeführt werden.

> [!Note]  
> Die Funktionen der Schriftart, die von den Standardvorlagen und Attributen für Schriftart Steuerelemente verfügbar gemacht werden, erfordern eine benutzerdefinierte Implementierung des Schriftart Steuer Elements, die sich außerhalb des Umfangs dieses Artikels befindet

 

In der folgenden Tabelle sind die Schriftart Steuerelement Vorlagen und der Edit-Steuerelement Typen aufgeführt, an denen jede Vorlage ausgerichtet ist.



| Vorlage      | Unterstützt                                                                 |
|---------------|--------------------------------------------------------------------------|
| Fontonly      | [LogFont-Struktur](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| Fontwithcolor | [Chooonfont-Struktur](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| Richfont      | [CHARFORMAT2-Struktur](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

In der folgenden Tabelle werden die-Steuerelemente aufgelistet, die den einzelnen Vorlagen zugeordnet sind, und die Steuerelemente identifiziert, die für eine zugeordnete Vorlage optional sind.



Steuerelemente

Vorlagen

**Richfont**

**Fontwithcolor**

**Fontonly**

Standard

Optional

Standard

Optional

Standard

Optional

Kombinations Feld " **Schriftgröße** "

Ja

Nein

Ja

Nein

Ja

Nein

Kombinations Feld " **Schriftfamilie** "

Ja

Nein

Ja

Nein

Ja

Nein

Schaltfläche " **vergrößern** "

Ja

Ja

Ja

Ja

\-

\-

Schaltfläche " **verkleinern** "

Ja

Ja

Ja

Ja

\-

\-

**Fett** Schaltfläche

Ja

Nein

Ja

Nein

Ja

Nein

**Kursiv** Schaltfläche

Ja

Nein

Ja

Nein

Ja

Nein

Unter **Streichung**

Ja

Nein

Ja

Ja

Ja

Ja

Schaltfläche " **durch** gestrichen"

Ja

Nein

Ja

Ja

Ja

Ja

**Schaltfläche** "index"

Ja

Nein

\-

\-

\-

\-

**SuperScript** -Schaltfläche

Ja

Nein

\-

\-

\-

\-

**Text** Hervorhebungs Schaltfläche

Ja

Nein

Ja

Ja

\-

\-

**Textfarbe** -Schaltfläche

Ja

Nein

Ja

Nein

\-

\-



 

Wenn das Layoutverhalten eines Schriftart Steuer Elements deklariert wird, bietet das Menüband-Framework eine optionale *sizedefinition* -Layoutvorlage, `OneFontControl` , die zwei unter Steuerungs Konfigurationen auf der Grundlage der Größe des Menübands und des für das Schriftart Steuerelement verfügbaren Speicherplatzes definiert. Weitere Informationen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>Hinzufügen eines FontControl zu einem Menüband

Die folgenden Codebeispiele veranschaulichen die grundlegenden Markup Anforderungen zum Hinzufügen eines Schriftart Steuer Elements zu einem Menüband:

In diesem Code Abschnitt wird das [**FontControl**](windowsribbon-element-fontcontrol.md) -Befehls Deklarations Markup angezeigt, einschließlich der [**Register**](windowsribbon-element-tab.md) Karten-und [**Gruppen**](windowsribbon-element-group.md) Befehle, die für die Anzeige eines Steuer Elements im [**Menüband**](windowsribbon-element-ribbon.md)erforderlich sind.


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



Dieser Code Abschnitt zeigt das Markup, das erforderlich ist, um ein [**FontControl**](windowsribbon-element-fontcontrol.md) -Element mit einem [**Befehl**](windowsribbon-element-command.md) über eine Befehls-ID zu deklarieren und zuzuordnen. Dieses spezielle Beispiel umfasst die [**Register**](windowsribbon-element-tab.md) Karten-und [**Gruppen**](windowsribbon-element-group.md) Deklarationen mit Skalierungs Einstellungen.


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>Hinzufügen eines FontControl zu einem contextpopup

Das Hinzufügen eines Schriftart-Steuer Elements zu einem [Kontext-Popup](windowsribbon-controls-contextpopup.md) erfordert eine ähnliche Vorgehensweise wie das Hinzufügen eines Schriftart-Steuer Elements zum Menüband. Ein Schriftart-Steuerelement in einer [**MiniToolbar**](windowsribbon-element-minitoolbar.md) ist jedoch auf den Satz von Standard untergeordneten Steuerelementen beschränkt, die allen Schriftart Steuerelement Vorlagen gemeinsam sind: **Schriftfamilie**, **Schrift** Grad, **Fett** und **kursiv**.

Die folgenden Codebeispiele veranschaulichen die grundlegenden Markup Anforderungen zum Hinzufügen eines Schriftart Steuer Elements zu einem [Kontext-Popup](windowsribbon-controls-contextpopup.md):

Dieser Code Abschnitt zeigt das [**FontControl**](windowsribbon-element-fontcontrol.md) -Befehls Deklarations Markup, das für die Anzeige eines **FontControl** -Elements im [**contextpopup**](windowsribbon-element-contextpopup.md)erforderlich ist.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



Dieser Code Abschnitt zeigt das Markup, das erforderlich ist, um ein [**FontControl**](windowsribbon-element-fontcontrol.md) -Element mit einem Befehl über eine Befehls-ID zu deklarieren und zuzuordnen.


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a>KeyTips

Auf jedes untergeordnete Steuerelement im Menüband-Schriftart Steuerelement kann über eine Tastenkombination oder KeyTip zugegriffen werden. Dieser KeyTip ist vordefiniert und wird den einzelnen untergeordneten Steuerelementen vom Framework zugewiesen.

Wenn dem [**FontControl**](windowsribbon-element-fontcontrol.md) -Element im Markup ein *KeyTip* -Attribut Wert zugewiesen wird, wird dieser Wert als Präfix zu dem vom Framework definierten KeyTip hinzugefügt.

> [!Note]  
> Die Anwendung sollte eine Einzelzeichen Regel für dieses Präfix erzwingen.

 

In der folgenden Tabelle sind die vom Framework definierten KeyTips aufgeführt. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Unter Kontrolle</th>
<th>KeyTip</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Schriftfamilie</td>
<td>F</td>
</tr>
<tr class="even">
<td>Schriftschnitt</td>
<td>T</td>
</tr>
<tr class="odd">
<td>Schriftgrad</td>
<td>E</td>
</tr>
<tr class="even">
<td>Schriftart vergrößern</td>
<td>G</td>
</tr>
<tr class="odd">
<td>Schriftart verkleinern</td>
<td>K</td>
</tr>
<tr class="even">
<td>Fett</td>
<td>B</td>
</tr>
<tr class="odd">
<td>Kursiv</td>
<td>I</td>
</tr>
<tr class="even">
<td>Underline</td>
<td>U</td>
</tr>
<tr class="odd">
<td>Durchgestrichen</td>
<td>X</td>
</tr>
<tr class="even">
<td>Hochgestellt</td>
<td>Y oder Z
<blockquote>
[!Note]<br />
Wenn das <em>KeyTip</em> -Attribut nicht im Markup deklariert ist, lautet der standardkeytip Y. Andernfalls ist der standardkeytip <em>KeyTip</em> + Z.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Tiefgestellt</td>
<td>A</td>
</tr>
<tr class="even">
<td>Schriftfarbe</td>
<td>C</td>
</tr>
<tr class="odd">
<td>Schriftart Hervorhebung</td>
<td>H</td>
</tr>
</tbody>
</table>



 

Das empfohlene Präfix für eine MUI-Multifunktionsleiste (mehrsprachige Benutzeroberfläche) ist "F", wie im folgenden Beispiel gezeigt.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



Der folgende Screenshot veranschaulicht die Schriftart Steuerelement-KeyTips, wie Sie im vorherigen Beispiel definiert wurden.

![Screenshot der FontControl-KeyTips in WordPad für Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>Die Ressourcen Datei des Menübands

Wenn die Markup Datei kompiliert wird, wird eine Ressourcen Datei generiert, die alle Ressourcen Verweise für die Multifunktionsleistenanwendung enthält.

Beispiel für eine einfache Ressourcen Datei:


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a>Schriftart Steuerelement-Eigenschaften

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Schriftart Steuerelement und die zugehörigen untergeordneten Steuerelemente.

In der Regel wird eine Schriftart-Steuerelement Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Schriftart-Steuerelement zugeordnet sind.



| Eigenschafts Schlüssel                                                                                                                  | Notizen                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI- \_ pkey \_ fontproperties](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | Macht alle Schriftart Steuerelement-untersteuerungseigenschaften als [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekt verfügbar.<br/> Das Framework fragt diese Eigenschaft ab, wenn `UI_INVALIDATIONS_VALUE` als Wert von *Flags* im [**iuiframework:: invalidateuicommand-Befehl**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand)übergeben wird.<br/> |
| [UI \_ pkey \_ fontproperties \_ changedproperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | Macht in Aggregat als [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt nur Eigenschaften der Schriftart Steuerelement-unter Kontrolle verfügbar, die geändert wurden.<br/>                                                                                                                                                                                                        |
| [UI- \_ pkey- \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | Kann nur durch Invalidierung aktualisiert werden.                                                                                                                                                                                                                                                                                                                                                      |
| [UI- \_ pkey \_ aktiviert](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | Unterstützt [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) und [**iuiframework:: abtuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).                                                                                                                                                                  |



 

Zusätzlich zu den Eigenschaften, die vom Schriftart Steuerelement selbst unterstützt werden, definiert das Menüband-Framework auch einen [Eigenschafts Schlüssel](windowsribbon-reference-properties.md) für jedes untergeordnete Steuerelement der Schriftart Steuerung. Diese Eigenschafts Schlüssel und ihre Werte werden vom Framework über eine [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen Implementierung verfügbar gemacht, die die Methoden zum Verwalten einer Auflistung, auch als Eigenschaften Behälter bezeichnet, von Name-Wert-Paaren definiert.

Die Anwendung übersetzt die Schriftart Strukturen in Eigenschaften, auf die über die [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen Methoden zugegriffen werden kann. Dieses Modell hebt den Unterschied zwischen dem Schriftart Steuerelement und den Windows-Graphics Device Interface (GDI)-Text Stapel Komponenten ([LOGFONT-Struktur](/windows/win32/api/wingdi/ns-wingdi-logfonta), [ausgewählter Schriftart Struktur](/windows/win32/api/commdlg/ns-commdlg-choosefonta)und [CHARFORMAT2-Struktur](/windows/win32/api/richedit/ns-richedit-charformat2a)) hervor, die vom Framework unterstützt werden.

In der folgenden Tabelle werden die einzelnen Steuerelemente und die zugehörigen Eigenschafts Schlüssel aufgelistet.



| Steuerelemente                 | Eigenschafts Schlüssel                                                                                                                                                                                                                                                           | Notizen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Schriftgrad**            | [Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Wenn eine Fläche mit Hetero gener Größe hervorgehoben wird, legt das Menüband-Framework das Steuerelement **Schriftart Größe** auf Blank und den Wert von [UI \_ pkey \_ fontproperties \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md) auf 0 (null) fest. Wenn Sie auf die Schaltfläche **Schriftart vergrößern** oder **verkleinern** klicken, wird der gesamte markierte Text angepasst, aber der relative Unterschied in den Textgrößen wird beibehalten.                                                                                                                                                    |
| **Schriftfamilie**          | [UI \_ pkey \_ fontproperties- \_ Familie](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | GDI-Schriftfamilien Namen variieren je nach System Gebiets Schema. Wenn der Wert der [UI \_ pkey \_ fontproperties- \_ Familie](windowsribbon-reference-properties-uipkey-fontproperties-family.md) über Anwendungs Sitzungen hinweg beibehalten wird, sollte dieser Wert in jeder neuen Sitzung abgerufen werden.                                                                                                                                                                                                                                                                            |
| **Schriftart vergrößern**            | [Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Siehe **Schrift** Grad.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Schriftart verkleinern**          | [Größe der Benutzeroberflächen- \_ pkey- \_ fontproperties \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Siehe **Schrift** Grad.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Fett**                 | [UI- \_ pkey \_ fontproperties \_ Fett](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Kursiv**               | [UI \_ pkey \_ fontproperties \_ kursiv](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Streichen**            | [Benutzeroberflächen- \_ pkey \_ fontproperties unter \_ streichen](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Durchgestrichen**        | [UI- \_ pkey- \_ fontproperties \_ durchgestrichen](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Index**            | [Benutzeroberflächen- \_ pkey \_ fontproperties \_ verticalpositionierung](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Wenn die **Schaltfläche** "index" festgelegt ist, kann das **SuperScript** nicht auch festgelegt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Hochgestellt**          | [Benutzeroberflächen- \_ pkey \_ fontproperties \_ verticalpositionierung](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Wenn die Schaltfläche **SuperScript** festgelegt ist, **kann der** Index nicht auch festgelegt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Text Hervorhebungs Farbe** | [Benutzeroberfläche \_ Pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ pkey \_ fontproperties \_ backgroundcolortype](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | Bietet die gleiche Funktionalität wie die `HighlightColors` Vorlage des [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) -Elements.<br/> Es wird dringend empfohlen, dass nur ein ursprünglicher Text Hervorhebungs **Farbwert** von der Anwendung festgelegt wird. Der zuletzt ausgewählte Wert sollte beibehalten und nicht festgelegt werden, wenn der Cursor innerhalb eines Dokuments neu positioniert wird. Dies ermöglicht einen schnellen Zugriff auf die letzte Auswahl des Benutzers, und die Farbauswahl muss nicht erneut geöffnet werden.<br/> Farbsuhren können nicht angepasst werden.<br/> |
| **Textfarbe**           | [Benutzeroberfläche \_ Pkey \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ pkey \_ fontproperties \_ foregroundcolortype](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)           | Bietet die gleiche Funktionalität wie die `StandardColors` Vorlage des [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) -Elements.<br/> Es wird dringend empfohlen, dass nur ein ursprünglicher **textfarbwert** von der Anwendung festgelegt wird. Der zuletzt ausgewählte Wert sollte beibehalten und nicht festgelegt werden, wenn der Cursor innerhalb eines Dokuments neu positioniert wird. Dies ermöglicht einen schnellen Zugriff auf die letzte Auswahl des Benutzers, und die Farbauswahl muss nicht erneut geöffnet werden.<br/> Farbsuhren können nicht angepasst werden.<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>Definieren eines FontControl-Befehls Handlers

In diesem Abschnitt werden die erforderlichen Schritte zum Binden eines Schriftart-Steuer Elements an einen Befehls Handler beschrieben.

> [!WARNING]
> Jeder Versuch, ein Farbmuster aus der Farbauswahl eines Schriftart Steuer Elements auszuwählen, kann zu einer Zugriffsverletzung führen, wenn dem Steuerelement kein Befehls Handler zugeordnet ist.

 

Im folgenden Codebeispiel wird veranschaulicht, wie im Markup deklarierte Befehle an einen Befehls Handler gebunden werden.


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



Im folgenden Codebeispiel wird veranschaulicht, wie die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Methode für ein Schriftart Steuerelement implementiert wird.


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



Im folgenden Codebeispiel wird veranschaulicht, wie die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Methode für ein Schriftart Steuerelement implementiert wird.


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**FontControl-Element**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[FontControl-Beispiel](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

