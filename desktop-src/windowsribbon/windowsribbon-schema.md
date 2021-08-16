---
title: Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup
description: Das Windows-Menübandframework verwendet eine Markupsprache, die auf Extensible Application Markup Language (XAML) basiert, um die Darstellung einer Menübandanwendung deklarativ zu implementieren.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows Menüband, Markupstruktur
- Menüband, Markupstruktur
- Windows Menüband, Trennen der Präsentation von der Befehlslogik
- Menüband, Trennen der Präsentation von der Befehlslogik
- Windows Menüband, Komponenten
- Menüband, Komponenten
- Befehlssystem für Windows Menüband
- Steuerelemente für Windows Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ae6c8d62012fac240c6d044c688295d89d8d5899e3673a3b914d8d142111d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201322"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup

Das Windows-Menübandframework verwendet eine Markupsprache, die auf Extensible Application Markup Language (XAML) basiert, um die Darstellung einer Menübandanwendung deklarativ zu implementieren.

-   [Trennen der Präsentation von der Befehlslogik](#separating-presentation-from-command-logic)
-   [Markupstruktur](#markup-structure)
-   [Menübandkomponenten](#ribbon-components)
-   [Zugehörige Themen](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Trennen der Präsentation von der Befehlslogik

Die Trennung von Darstellungs- und visuellen Attributen von der Befehlslogik im Menübandframework erfolgt über zwei unterschiedliche, aber abhängige Entwicklungsplattformen. Steuerelementlayouts, Skalierungsverhalten, Befehlsdeklarationen und Ressourcenspezifikationen sind die Entwurfszeitdomäne einer deklarativen Markupsyntax, die auf der spezifikation Extensible Application Markup Language [(XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) basiert. Funktionen auf niedriger Ebene, Anwendungshooks und Befehlshandler werden in Component Object Model (COM)-basierten Schnittstellenimplementierungen definiert.

Diese Trennung von Präsentation und Logik bietet die folgenden Vorteile:

-   Ein effizienterer Anwendungsentwicklungszyklus, der es Benutzeroberflächenentwicklern und -designern ermöglicht, die GRAFISCHE BENUTZEROBERFLÄCHE der Menübandanwendung unabhängig von der Kernanwendungsfunktionalität zu implementieren. Diese Kernfunktionalität kann dedizierten Softwareentwicklern bleiben.
-   Weniger kostspielige Wartung, da Änderungen an der grafischen Benutzeroberfläche ohne Änderungen an der Kernfunktionalität möglich sind (und umgekehrt).
-   Einfache Angabe von Zeichenfolgen- und Bildressourcen durch Markup.
-   Einfache Prototyperstellung.

## <a name="markup-structure"></a>Markupstruktur

In der Struktur des Menübandframeworkmarkups sind zwei unterschiedliche Verzweigungen vorhanden.

Der erste Branch enthält ein Manifest der Befehls- und Ressourcendeklarationen (Zeichenfolgen und Bilder). Jeder Befehlseintrag wird vom Framework verwendet, um ein Menüband-Steuerelement über eine Befehls-ID an einen im Anwendungscode definierten Befehlshandler zu binden.

Die zweite Verzweigung enthält die tatsächlichen Steuerelementdeklarationen. Jedes Steuerelement wird einem Befehl über ein *CommandName-Attribut* zugeordnet, das einem in jeder Befehlsdeklaration angegebenen *Name-Attribut* zugeordnet ist.

## <a name="ribbon-components"></a>Menübandkomponenten

Die Benutzeroberflächenfunktion des Menübandframework wird über Ansichten [verfügbar gemacht.](windowsribbon-reference-elements-view.md) Eine Ansicht ist im Wesentlichen ein [](windowsribbon-element-ribbon.md) Container, z. B. das Menüband und [**ContextPopup,**](windowsribbon-element-contextpopup.md)der verwendet wird, um Frameworksteuerelemente und die Befehle, an die sie gebunden sind, zu präsentieren.

Die [](windowsribbon-element-ribbon.md) Menübandansicht besteht aus mehreren Komponenten, die ein Anwendungsmenü, die Symbolleiste für den Schnellzugriff [](windowsribbon-controls-tab.md) [(Quick Access Toolbar, QAT)](windowsribbon-controls-quickaccesstoolbar.md) zum Anzeigen häufig verwendeter Befehle über die Menübandbenutzeroberfläche, Kern- und Kontextregisterkarte, die Gruppen von Steuerelementen enthält, und das umfassende Kontextmenüsystem von [**ContextPopup**](windowsribbon-element-contextpopup.md)umfassen. [](windowsribbon-controls-applicationmenu.md) [](windowsribbon-controls-group.md)

Alle Menübandkomponenten werden in einer eigenständigen Markupdatei deklariert, die:

-   Gibt die grundlegenden Eigenschaften für jedes Element an.
-   Zeigt hierarchische Beziehungen eindeutig an.
-   Gibt Layouteinstellungen und Skalierungshinweise an. Weitere Informationen zu Layoutvorlagen für das Menübandframework finden Sie unter Anpassen eines Menübands durch [Größendefinitionen und Skalierungsrichtlinien.](windowsribbon-templates.md)
-   Bietet eine Möglichkeit zum Definieren von Ressourcen wie Bildern und Bezeichnungen. Weitere Informationen zu Bildressourcen finden Sie unter [Angeben von Menübandbildressourcen.](windowsribbon-imageformats.md)

Die folgenden beiden Menübandmarkupbeispiele veranschaulichen, wie ein Satz von Menübandanwendungsmenüelementen jeweils einem Befehlsnamen und einer ID zugeordnet wird.

1.  In diesem Abschnitt werden die Befehlsdeklarationen gezeigt, die für ein Anwendungsmenü mit grundlegenden Befehlen wie Neu, Öffnen und Speichern erforderlich sind.
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  In diesem Abschnitt werden die zugeordneten Steuerelementdeklarationen gezeigt.
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

Wenn das Markup mit dem UICC-Tool (UI Command Compiler) kompiliert wird, werden die Befehlsnamen und -IDs in einer Headerdatei platziert, die von der Menübandhostanwendung verwendet wird.

Im Folgenden finden Sie ein Beispiel für eine Headerdatei, die von UICC generiert wird.


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Kompilieren von Menübandmarkup](windowsribbon-intentcl.md)
</dt> </dl>

 

 