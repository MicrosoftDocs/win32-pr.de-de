---
title: Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup
description: Das Windows-Menü Band Framework verwendet eine Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um die Darstellung einer Menü Bandanwendung deklarativ zu implementieren.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows-Menüband, Markup Struktur
- Menüband, Markup Struktur
- Windows-Menüband, Trennen der Präsentation von der Befehls Logik
- Multifunktionsleiste, Trennen der Präsentation von der Befehls Logik
- Windows-Menüband, Komponenten
- Multifunktionsleiste, Komponenten
- Befehlssystem für Windows-Menüband
- Steuerelemente für Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390739"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup

Das Windows-Menü Band Framework verwendet eine Markup Sprache, die auf Extensible Application Markup Language (XAML) basiert, um die Darstellung einer Menü Bandanwendung deklarativ zu implementieren.

-   [Trennen der Präsentation von der Befehls Logik](#separating-presentation-from-command-logic)
-   [Markup Struktur](#markup-structure)
-   [Menü Band Komponenten](#ribbon-components)
-   [Zugehörige Themen](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Trennen der Präsentation von der Befehls Logik

Die Trennung von Präsentations-und visuellen Attributen von der Befehls Logik im Menüband-Framework erfolgt über zwei unterschiedliche, aber abhängige Entwicklungsplattformen. Steuerelement Layouts, Skalierungs Verhalten, Befehls Deklarationen und Ressourcen Spezifikationen sind die Entwurfszeit Domäne einer deklarativen Markup Syntax, die auf der [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) -Spezifikation basiert. Funktionen auf niedriger Ebene, Anwendungs Hooks und Befehls Handler werden in Component Object Model (com)-basierten Schnittstellen Implementierungen definiert.

Diese Trennung von Präsentation und Logik bietet die folgenden Vorteile:

-   Ein effizienterer Anwendungs Entwicklungs Cycle, mit dem Benutzeroberflächen Entwickler und Designer die GUI der Menüband-Anwendung unabhängig von der Kern Anwendungs Funktionalität implementieren können. Diese Kernfunktionen können dedizierten Softwareentwicklern überlassen werden.
-   Kostengünstigere Wartung, da Änderungen an der GUI ohne Änderungen an der Kernfunktionalität (und umgekehrt) möglich sind.
-   Einfache Angabe von Zeichen folgen-und Bild Ressourcen durch Markup.
-   Einfache Prototyperstellung.

## <a name="markup-structure"></a>Markup Struktur

Innerhalb der Struktur von Multifunktionsleisten-Frameworks sind zwei unterschiedliche Verzweigungen vorhanden.

Der erste Branch enthält ein Manifest von Befehls-und Ressourcen Deklarationen (Zeichen folgen und Bilder). Jeder Befehls Eintrag wird vom Framework verwendet, um ein Menüband-Steuerelement über eine Befehls-ID an einen Befehls Handler zu binden, der im Anwendungscode definiert ist.

Die zweite Verzweigung enthält die tatsächlichen Steuerelement Deklarationen. Jedes Steuerelement ist einem Befehl über ein *CommandName* -Attribut zugeordnet, das einem *namens* Attribut zugeordnet ist, das in jeder Befehls Deklaration angegeben ist.

## <a name="ribbon-components"></a>Menü Band Komponenten

Die Benutzeroberfläche des Multifunktionsleisten-Frameworks wird durch [Ansichten](windowsribbon-reference-elements-view.md)verfügbar gemacht Eine Sicht ist im Wesentlichen ein Container, z. b. das [**Menüband**](windowsribbon-element-ribbon.md) und [**contextpopup**](windowsribbon-element-contextpopup.md), das verwendet wird, um frameworksteuerelemente und die Befehle darzustellen, an die Sie gebunden sind.

Die Ansicht " [**Menüband**](windowsribbon-element-ribbon.md) " besteht aus mehreren Komponenten, die ein [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)enthalten, der [Symbolleiste für den schnell Zugriff (QAT)](windowsribbon-controls-quickaccesstoolbar.md) zum Anzeigen häufig verwendeter Befehle von der Multifunktionsleisten-Benutzeroberfläche, von Kern-und Kontext [Registerkarten](windowsribbon-controls-tab.md) , die [Gruppen](windowsribbon-controls-group.md) von Steuerelementen enthalten, und vom umfangreichen Kontextmenü System von [**contextpopup**](windowsribbon-element-contextpopup.md).

Alle Multifunktionsleistenkomponenten werden in einer eigenständigen Markup Datei deklariert:

-   Gibt die grundlegenden Eigenschaften für jedes Element an.
-   Zeigt hierarchische Beziehungen eindeutig an.
-   Liefert Layouteinstellungen und Skalierungs Hinweise. Weitere Informationen zu Menüband-frameworklayoutvorlagen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).
-   Bietet eine Möglichkeit, Ressourcen wie Bilder und Bezeichnungen zu definieren. Weitere Informationen zu Bild Ressourcen finden Sie unter [Angeben von Menüband-Bild Ressourcen](windowsribbon-imageformats.md).

Die beiden folgenden Beispiele für Menü Band Markierungen veranschaulichen, wie ein Satz von Menü Elementen der Menü Bandanwendung jeweils mit einem Befehlsnamen und einer ID verknüpft ist.

1.  In diesem Abschnitt werden die für ein Anwendungsmenü erforderlichen Befehls Deklarationen mit grundlegenden Befehlen wie "New", "Open" und "Save" angezeigt.
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

    

2.  Dieser Abschnitt zeigt die zugeordneten Steuerelement Deklarationen.
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

    

Wenn das Markup mit dem UI-Befehls Compiler (UICC) kompiliert wird, werden die Befehlsnamen und IDs in einer von der Menüband-Host Anwendung verwendeten Header Datei abgelegt.

Im folgenden finden Sie ein Beispiel für eine Header Datei, die von UICC generiert wurde.


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

[Kompilieren von Menü Band Markup](windowsribbon-intentcl.md)
</dt> </dl>

 

 