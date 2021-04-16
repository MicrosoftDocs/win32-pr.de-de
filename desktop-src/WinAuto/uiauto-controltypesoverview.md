---
title: Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung
description: Benutzeroberflächenautomatisierungs-Steuerelement Typen sind Eigenschaften, die als bekannte Bezeichner fungieren, die die Art des Steuer Elements angeben, das ein bestimmtes UI-Element darstellt, z. b. ein Kombinations Feld oder eine Schaltfläche.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- UI-Automatisierung, Übersicht über Steuerelement Typen
- UI-Automatisierung, UIA_LocalizedControlTypePropertyId-Eigenschaft
- Steuerelement Typen, Info
- Steuerelement Typen, Voraussetzungen
- Steuerelement Typen, Voraussetzungen
- Steuerelement Typen, vordefiniert
- Steuerelement Typen, UIA_LocalizedControlTypePropertyId-Eigenschaft
- vordefinierte Steuerelement Typen
- UIA_LocalizedControlTypePropertyId-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516823"
---
# <a name="ui-automation-control-types-overview"></a>Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung

Benutzeroberflächenautomatisierungs-Steuerelement Typen sind Eigenschaften, die als bekannte Bezeichner fungieren, die die Art des Steuer Elements angeben, das ein bestimmtes UI-Element darstellt, z. b. ein Kombinations Feld oder eine Schaltfläche. Client Anwendungen verwenden den-Typ, um die Funktionen eines Steuer Elements zu identifizieren und zu bestimmen, wie mit ihm interagiert werden soll.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen für Steuerelementtypen der Benutzeroberflächenautomatisierung](#ui-automation-control-type-requisites)
-   [Die LocalizedControlType-Eigenschaft](#the-localizedcontroltype-property)
-   [Aktuelle Steuerelementtypen der Benutzeroberflächenautomatisierung](#current-ui-automation-control-types)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>Anforderungen für Steuerelementtypen der Benutzeroberflächenautomatisierung

Jedem Benutzeroberflächenautomatisierungs-Steuerelement ist eine Reihe von Bedingungen zugeordnet. Wenn ein Anbieter einem Steuerelement einen Steuerelement Typen zuweist, muss der Anbieter sicherstellen, dass das Steuerelement alle Bedingungen erfüllt, die diesem Steuerelement zugeordnet sind. Die Bedingungen umfassen Folgendes:

-   Benutzeroberflächenautomatisierungs-Steuerelement Muster: jeder Steuer ungstyp verfügt über eine Reihe von Steuerelement Mustern, die vom Steuerelement unterstützt werden müssen, eine optionale Menge und eine Menge, die vom Steuerelement nicht unterstützt werden darf
-   Eigenschaftswerte für die Benutzeroberflächenautomatisierung: Jeder Steuerelementtyp hat einen Satz von Eigenschaften, die das Steuerelement unterstützen muss.
-   Ereignisse für die Benutzeroberflächenautomatisierung: Jeder Steuerelementtyp hat einen Satz von Ereignissen, die das Steuerelement unterstützen muss.
-   Baumstruktur der Benutzeroberflächenautomatisierung: Jeder Steuerelementtyp definiert, wie das Steuerelement in der Baumstruktur der Benutzeroberflächenautomatisierung dargestellt werden muss.

Wenn ein Steuerelement die Bedingungen für einen bestimmten Steuer Elementtyp erfüllt, gibt der [**iuiautomationelement:: currentcontroltype**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (oder der [**iuiautomationelement:: cachedcontroltype**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype))-Eigenschafts Wert diesen Steuer Elementtyp an.

Wenn das Steuerelement die Spezifikationen für einen bestimmten Steuer Elementtyp nicht erfüllt, verwenden Sie [**UIA \_ customcontroltypeid**](uiauto-controltype-ids.md) als Steuer Elementtyp-ID, und beschreiben Sie das Steuerelement vollständig, indem Sie die entsprechenden Steuerelement Muster und-Eigenschaften verwenden. Sie können auch die [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft auf eine Zeichenfolge festlegen, die den Typ des Steuer Elements am besten beschreibt.

## <a name="the-localizedcontroltype-property"></a>Die LocalizedControlType-Eigenschaft

Wenn Sie ein vordefiniertes Steuerelement für die Beschreibung des Steuer Elements verwenden, verwenden Sie den Standardwert für die [**UIA \_ localizedcontroltypepropertyid**](uiauto-automation-element-propids.md) -Eigenschaft, und lassen Sie die Benutzeroberflächen Automatisierung eine lokalisierte Zeichenfolge bereit, die Anbieter ordnungsgemäß verfügbar machen. Wenn Sie das Steuerelement nicht mithilfe eines vordefinierten Steuerelement Typs beschreiben können, legen Sie die Eigenschaft **UIA \_ localizedcontroltypepropertyid** auf eine lokalisierte Zeichenfolge fest, die den Typ des Steuer Elements exakt beschreibt. Die Zeichenfolge sollte präzise, aber genau genug sein, damit eine Hilfstechnologie wie z. b. eine Sprachausgabe in der Benutzeroberfläche den Benutzer über den Typ des Steuer Elements informieren kann.

## <a name="current-ui-automation-control-types"></a>Aktuelle Steuerelementtypen der Benutzeroberflächenautomatisierung

In den folgenden Themen werden die Steuerelement Typen der Benutzeroberflächen Automatisierung beschrieben. Für jeden Steuerelement Typ enthält die Beschreibung den Satz von Bedingungen, die ein Steuerelement vom angegebenen Typ unterstützen muss:

-   Appbar-Steuerelement Typen
-   [Button-Steuerelement Typen](uiauto-supportbuttoncontroltype.md)
-   [Typ des Kalender Steuer Elements](uiauto-supportcalendarcontroltype.md)
-   [CheckBox-Steuerelement Typen](uiauto-supportcheckboxcontroltype.md)
-   [ComboBox-Steuerelement Typen](uiauto-supportcomboboxcontroltype.md)
-   [DataGrid-Steuerelement Typen](uiauto-supportdatagridcontroltype.md)
-   [DataItem-Steuerelement Typen](uiauto-supportdataitemcontroltype.md)
-   [Dokument Steuerelement-Typ](uiauto-supportdocumentcontroltype.md)
-   [Steuerelement-Typ bearbeiten](uiauto-supporteditcontroltype.md)
-   [Gruppen Steuerungstyp](uiauto-supportgroupcontroltype.md)
-   [Header Steuerelement-Typ](uiauto-supportheadercontroltype.md)
-   [Header Item-Steuer Elementtyp](uiauto-supportheaderitemcontroltype.md)
-   [Hyperlink-Steuerelement Typen](uiauto-supporthyperlinkcontroltype.md)
-   [Bild Steuerelement-Typ](uiauto-supportimagecontroltype.md)
-   [List-Steuerelement Typen](uiauto-supportlistcontroltype.md)
-   [ListItem-Steuer Elementtyp](uiauto-supportlistitemcontroltype.md)
-   [Menu-Steuerelement Typen](uiauto-supportmenucontroltype.md)
-   [MenuBar-Steuer Elementtyp](uiauto-supportmenubarcontroltype.md)
-   [MenuItem-Steuer Elementtyp](uiauto-supportmenuitemcontroltype.md)
-   [Pane-Steuerelement Typen](uiauto-supportpanecontroltype.md)
-   [ProgressBar-Steuerelement Typen](uiauto-supportprogressbarcontroltype.md)
-   [RadioButton-Steuer Elementtyp](uiauto-supportradiobuttoncontroltype.md)
-   [ScrollBar-Steuerelement Typen](uiauto-supportscrollbarcontroltype.md)
-   [Typ des semanticzoom-Steuer Elements](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [Separator-Steuerelement Typen](uiauto-supportseparatorcontroltype.md)
-   [Slider-Steuerelement Typen](uiauto-supportslidercontroltype.md)
-   [Spinner-Steuerelement Typen](uiauto-supportspinnercontroltype.md)
-   [SplitButton-Steuer Elementtyp](uiauto-supportsplitbuttoncontroltype.md)
-   [StatusBar-Steuer Elementtyp](uiauto-supportstatusbarcontroltype.md)
-   [Register Steuerungstyp](uiauto-supporttabcontroltype.md)
-   [TabItem-Steuer Elementtyp](uiauto-supporttabitemcontroltype.md)
-   [Table-Steuerelement Typen](uiauto-supporttablecontroltype.md)
-   [Text Steuerelement-Typ](uiauto-supporttextcontroltype.md)
-   [Thumb-Steuerelement](uiauto-supportthumbcontroltype.md)
-   [TitleBar-Steuerelement Typen](uiauto-supporttitlebarcontroltype.md)
-   [ToolBar-Steuerelement Typen](uiauto-supporttoolbarcontroltype.md)
-   [ToolTip-Steuerelement Typen](uiauto-supporttooltipcontroltype.md)
-   [Struktur Steuerungstyp](uiauto-supporttreecontroltype.md)
-   [TreeItem-Steuerelement Typen](uiauto-supporttreeitemcontroltype.md)
-   [Fenster Steuerelement-Typ](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Steuerelement-Typbezeichner](uiauto-controltype-ids.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Unterstützen der Benutzeroberflächenautomatisierungs](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[Benutzeroberflächenautomatisierungs-Unterstützung für Standardsteuerelemente](uiauto-controlsupport.md)
</dt> <dt>

[Grundlagen der Benutzeroberflächenautomatisierung](entry-uiautocore-overview.md)
</dt> </dl>

 

 