---
title: Anhang G Active Accessibility Bridge to Benutzeroberflächenautomatisierung
description: Dieser Anhang enthält Informationen zur Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14991f869706a16c4def8fdaf49ae255e3ddf413eec416cefd1e151ee470cc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052968"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Anhang G: Active Accessibility Bridge to Benutzeroberflächenautomatisierung

Dieser Anhang enthält Informationen zur Microsoft Active Accessibility Bridge. Mit Active Accessibility Bridge können Anwendungen, die Microsoft Active Accessibility implementieren, auf Anwendungen zugreifen, die Microsoft-Benutzeroberflächenautomatisierung. Durch die Überbrückung von Microsoft Active Accessibility und Benutzeroberflächenautomatisierung können Microsoft Active Accessibility-basierte Clients, z. B. ein Bildschirmreader unter Windows XP, programmgesteuert mit Benutzeroberflächenautomatisierung-basierten Anbietern von Benutzeroberflächenautomatisierung interagieren, z. B. mit einer Windows Presentation Foundation-Anwendung (WPF). Sie ist Teil der Benutzeroberflächenautomatisierung Native Core-API (UIAutomationCore.dll).

Die Active Accessibility Bridge ordnet Benutzeroberflächenautomatisierung Eigenschaften und Ereignisse denen der Microsoft Active Accessibility. In den folgenden Tabellen werden die Microsoft Active Accessibility [**IAccessible-Schnittstellenmethoden**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Eigenschaften Benutzeroberflächenautomatisierung. Verwenden Sie diese Tabellen, um geeignete Codierungsmethoden für die Entwicklung Ihres Microsoft Active Accessibility-basierten Clients zu bestimmen.

### <a name="navigation-and-hierarchy-properties"></a>Navigations- und Hierarchieeigenschaften



| IAccessible-Eigenschaft                                                     | Benutzeroberflächenautomatisierung-Eigenschaft          |
|--------------------------------------------------------------------------|---------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Nicht implementiert                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Abgeleitet von Benutzeroberflächenautomatisierung Struktur |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Abgeleitet von Benutzeroberflächenautomatisierung Struktur |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | Nicht implementiert                 |



 

### <a name="descriptive-properties-and-methods"></a>Beschreibende Eigenschaften und Methoden



| Iaccessible                                                                          | Benutzeroberflächenautomatisierung                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Weitere Informationen finden Sie in der Tabelle Control Types and accRole (Steuerelementtypen und accRole).                                                                                                                                                                                                                                                                     |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Weitere Informationen finden Sie in der Tabelle Control Types and accRole (Steuerelementtypen und accRole).                                                                                                                                                                                                                                                                     |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty; Wenn beide vorhanden sind, hat AccessKeyProperty Vorrang.                                                                                                                                                                                                                         |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeProperty. Weitere Informationen finden Sie in der Tabelle Control Types and accRole (Steuerelementtypen und accRole).                                                                                                                                                                                                                                                |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Weitere Informationen finden Sie in der Tabelle Control Types and accRole (Steuerelementtypen und accRole).                                                                                                                                                                                                                                                                     |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty; wird für Steuerelementtypen unterstützt, die das [Steuerelementmuster Value](uiauto-implementingvalue.md) oder [das Steuerelementmuster RangeValue](uiauto-implementingrangevalue.md) unterstützen. RangeValue-Werte sind konsistent mit Microsoft Active Accessibility Verhalten (0 bis 100). Value-Elemente verwenden eine Zeichenfolge. |
| [**put \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty; wird für Steuerelementtypen unterstützt, die das [Value-Steuerelementmuster](uiauto-implementingvalue.md) oder [das RangeValue-Steuerelementmuster](uiauto-implementingrangevalue.md) unterstützen.                                                                                                                                      |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Nicht implementiert                                                                                                                                                                                                                                                                                                          |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | Nicht implementiert                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Steuerelementtypen und accRole

Die Microsoft Active Accessibility ist ROLE [**\_ SYSTEM \_ CLIENT.**](object-roles.md) Wenn keine Standardaktion für einen Steuerelementtyp gefunden wird, verwendet die Active Accessibility Bridge auch die folgenden verfügbaren Steuerelementmuster: [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)und [Toggle](uiauto-implementingtoggle.md). Beispielsweise verfügt ein Groupbox-Steuerelement über keine Standardaktion. Wenn ExpandCollapse unterstützt wird, verwendet die Active Accessibility Bridge diese für die Standardaktion.



| Benutzeroberflächenautomatisierung Steuerelementtyp                              | accRole                                                                     | Standardaktion                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Schaltfläche](uiauto-supportbuttoncontroltype.md)           | [**\_ \_ ROLLENSYSTEM-PUSHBUTTON**](object-roles.md)     | Tastenkombination                                                    |
| [Kalender](uiauto-supportcalendarcontroltype.md)       | [**\_ \_ ROLLENSYSTEMCLIENT**](object-roles.md)             | Keine                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**\_CHECKBUTTON DES \_ ROLLENSYSTEMS**](object-roles.md)   | Check/Uncheck (umschalten)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**KOMBINATIONSFELD \_ \_ "ROLLENSYSTEM"**](object-roles.md)         | Keine                                                     |
| Benutzerdefiniert                                                  | [**\_ \_ ROLLENSYSTEMCLIENT**](object-roles.md)             | Keine                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**\_ \_ ROLLENSYSTEMLISTE**](object-roles.md)                 | Keine                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)         | Keine                                                     |
| [Dokument](uiauto-supportdocumentcontroltype.md)       | [**ROLE \_ SYSTEM DOCUMENT (ROLLENSYSTEMDOKUMENT) \_**](object-roles.md)         | Keine                                                     |
| [Bearbeiten](uiauto-supporteditcontroltype.md)               | [**\_ \_ ROLLENSYSTEMTEXT**](object-roles.md)                 | Keine                                                     |
| [Gruppe](uiauto-supportgroupcontroltype.md)             | [**\_ \_ ROLLENSYSTEMGRUPPEN**](object-roles.md)         | Keine                                                     |
| [Header](uiauto-supportheadercontroltype.md)           | [**\_ \_ ROLLENSYSTEMLISTE**](object-roles.md)                 | Keine                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**ROLE \_ SYSTEM \_ COLUMNHEADER**](object-roles.md) | Klicken Sie auf                                                    |
| [Link](uiauto-supporthyperlinkcontroltype.md)     | [**ROLE \_ SYSTEM \_ LINK**](object-roles.md)                 | Springen (zuordnung zu Invoke)                                    |
| [Bild](uiauto-supportimagecontroltype.md)             | [**GRAFIK \_ ZUM \_ ROLLENSYSTEM**](object-roles.md)           | Keine                                                     |
| [Liste](uiauto-supportlistcontroltype.md)               | [**\_ \_ ROLLENSYSTEMLISTE**](object-roles.md)                 | Keine                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)         | Doppelklicken                                             |
| [Menü](uiauto-supportmenucontroltype.md)               | [**MENÜ \_ \_ "ROLLENSYSTEM"POPUP**](object-roles.md)       | Keine                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**MENÜLEISTE \_ \_ "ROLLENSYSTEM"**](object-roles.md)           | Keine                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**MENÜELEMENT \_ \_ "ROLLENSYSTEM"**](object-roles.md)         | Führen Sie oder Öffnen/Schließen für Menüelemente aus, die über children verfügen. |
| [Bereich](uiauto-supportpanecontroltype.md)               | [**BEREICH \_ \_ "ROLLENSYSTEM"**](object-roles.md)                 | Keine                                                     |
| [Progressbar](uiauto-supportprogressbarcontroltype.md) | [**STATUSLEISTE \_ DES \_ ROLLENSYSTEMS**](object-roles.md)   | Keine                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**\_RADIOBUTTON FÜR \_ ROLLENSYSTEM**](object-roles.md)   | Azure Functions                                                    |
| [Scrollbar](uiauto-supportscrollbarcontroltype.md)     | [**\_ \_ ROLLENSYSTEM-BILDLAUFLEISTE**](object-roles.md)       | Keine                                                     |
| [Schieberegler](uiauto-supportslidercontroltype.md)           | [**\_ \_ ROLLENSYSTEMSCHIEBEREGLER**](object-roles.md)             | Keine                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**ROLE \_ SYSTEM \_ SPINBUTTON**](object-roles.md)     | Keine                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**\_ \_ ROLLENSYSTEM-SPLITBUTTON**](object-roles.md)   | Keine                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**ROLE \_ SYSTEM \_ STATUSBAR**](object-roles.md)       | Keine                                                     |
| [TAB](uiauto-supporttabcontroltype.md)                 | [**SEITE \_ \_ "ROLLENSYSTEM"TABLIST**](object-roles.md)   | Keine                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**SEITE \_ \_ "ROLLENSYSTEM"TAB**](object-roles.md)           | Switch                                                   |
| [Tabelle](uiauto-supporttablecontroltype.md)             | [**ROLE \_ SYSTEM \_ TABLE**](object-roles.md)               | Keine                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**ROLE \_ SYSTEM \_ STATICTEXT**](object-roles.md)     | Keine                                                     |
| [Daumen](uiauto-supportthumbcontroltype.md)             | [**\_ \_ ROLLENSYSTEMINDIKATOR**](object-roles.md)       | Keine                                                     |
| [Titlebar](uiauto-supporttitlebarcontroltype.md)       | [**ROLE \_ SYSTEM \_ TITLEBAR**](object-roles.md)         | Keine                                                     |
| [Symbolleiste](uiauto-supporttoolbarcontroltype.md)         | [**SYMBOLLEISTE \_ DES \_ ROLLENSYSTEMS**](object-roles.md)           | Keine                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**QUICKINFO \_ FÜR \_ ROLLENSYSTEM**](object-roles.md)           | Keine                                                     |
| [Struktur](uiauto-supporttreecontroltype.md)               | [**\_ \_ ROLLENSYSTEMGLIEDERUNG**](object-roles.md)           | Keine                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**GLIEDERUNG \_ DES \_ ROLLENSYSTEMSITEM**](object-roles.md)   | Erweitern oder Reduzieren                                       |
| [Fenster](uiauto-supportwindowcontroltype.md)           | [**FENSTER \_ \_ "ROLLENSYSTEM"**](object-roles.md)             | Keine                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Benutzeroberflächenautomatisierung Eigenschaften und accState



| accState                                                                                      | Benutzeroberflächenautomatisierung-Eigenschaft                                                                                                                                                        | Triggerstatusänderung |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**STATE \_ SYSTEM \_ CHECKED**](object-state-constants.md)                 | Verwenden Sie für ControlType = "checkbox" ToggleState.On. Verwenden Sie für "radiobutton" [ **SelectionItemPattern::IsSelected.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Ja                   |
| [**STATUSSYSTEM \_ \_ FOKUSFÄHIG**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | Nein                    |
| [**\_ \_ ZUSTANDSSYSTEMORIENTIERTES**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | Nein                    |
| [**STATE \_ SYSTEM \_ PROTECTED**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | Nein                    |
| [**STATE \_ SYSTEM \_ READONLY**](object-state-constants.md)               | IsReadOnlyProperty (Value-Steuerelementmuster und RangeValue-Steuerelementmuster)                                                                                                     | Nein                    |
| [**ZUSTANDSSYSTEM \_ \_ NICHT VERFÜGBAR**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Ja                   |
| [**STATE \_ SYSTEM \_ LINKED**](object-state-constants.md)                   | ControlTypeProperty = "hyperlink"                                                                                                                                             | Nein                    |
| [**STATE \_ SYSTEM \_ SELECTABLE**](object-state-constants.md)           | SelectionItemPattern wird unterstützt.                                                                                                                                             | Nein                    |
| [**STATUSSYSTEM \_ \_ AUSGEWÄHLT**](object-state-constants.md)               | IsSelectedProperty (SelectionItem-Steuerelementmuster)                                                                                                                            | Nein                    |
| [**ZUSTANDSSYSTEM \_ \_ REDUZIERT**](object-state-constants.md)             | ExpandCollapseState = Collapsed                                                                                                                                               | Ja                   |
| [**ERWEITERTES \_ \_ ZUSTANDSSYSTEM**](object-state-constants.md)               | ExpandCollapseState = Expanded oder PartiallyExpanded                                                                                                                           | Ja                   |
| [**STATE \_ SYSTEM \_ HASPOPUP**](object-state-constants.md)               | Menüelemente, die Erweitern/Reduzieren unterstützen                                                                                                                                       | Nein                    |
| [**STATE \_ SYSTEM \_ MIXED**](object-state-constants.md)                     | ToggleState = Unbestimmt                                                                                                                                                   | Nein                    |
| [**STATE \_ SYSTEM \_ SIZEABLE**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanResize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | Nein                    |
| [**STATE \_ SYSTEM \_ MOVEABLE**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | Nein                    |
| [**STATE \_ SYSTEM \_ MULTISELECTABLE**](object-state-constants.md) | [**IUIAutomationSelectionPattern::CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | Nein                    |



 

### <a name="selection-and-focus"></a>Auswahl und Fokus



| Iaccessible                                                            | Benutzeroberflächenautomatisierung                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation::FocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Weitere Informationen finden Benutzeroberflächenautomatisierung Tabelle Eigenschaften und accSelect SELFLAGs.             |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern::GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Benutzeroberflächenautomatisierung Eigenschaften und accSelect SELFLAGs



| accSelect SELFLAGs                                                  | Benutzeroberflächenautomatisierung-Eigenschaft                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFLAG \_ NONE**](selflag.md)                       | Nicht verfügbar                                                                                                                  |
| SELFLAG \_ TAKFOCUS                                                   | [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**SELFLAG \_ TAKESELECTION**](selflag.md)     | [**IUIAutomationSelectionItemPattern::Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**SELFLAG \_ ADDSELECTION**](selflag.md)       | [**IUIAutomationSelectionItemPattern::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| SELFLAG \_ TAKEREMOVESELECTION                                        | [**IUIAutomationSelectionItemPattern::RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**SELFLAG \_ EXTENDSELECTION**](selflag.md) | Nicht verfügbar                                                                                                                  |



 

### <a name="spatial-mapping"></a>Räumliche Zuordnung



| Iaccessible                                                 | Benutzeroberflächenautomatisierung                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot::ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Ereignisse



| System-Level-Ereigniskonst constants                                                             | Benutzeroberflächenautomatisierung                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ EREIGNISSYSTEMMENÜPOPUPSTART**](event-constants.md)     | [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) (Hinweis: Muss überprüfen, ob es sich um ein Popupfenster handelt.) |
| [**\_ \_ EREIGNISSYSTEMMENÜPOPUPEND**](event-constants.md)         | [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                |
| [**\_ \_ EREIGNISSYSTEMMENÜSTART**](event-constants.md)               | [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md)                                          |
| [**\_ \_ EREIGNISSYSTEMMENÜEND**](event-constants.md)                   | [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)                                              |
| [**EVENT \_ SYSTEM \_ SOUND**](event-constants.md)                       |                                                                                                                         |
| [**\_ \_ EREIGNISSYSTEMWARNUNG**](event-constants.md)                       |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ CAPTURESTART**](event-constants.md)         |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ CAPTUREEND**](event-constants.md)             |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ DIALOGSTART**](event-constants.md)           |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ DIALOGEND**](event-constants.md)               |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ MOVESIZESTART**](event-constants.md)       |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ MOVESIZEEND**](event-constants.md)           |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ CONTEXTHELPSTART**](event-constants.md) |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ CONTEXTHELPEND**](event-constants.md)     | Nicht relevant                                                                                                            |
| [**EVENT \_ SYSTEM \_ DRAGDROPSTART**](event-constants.md)       |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ DRAGDROPEND**](event-constants.md)           |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ SWITCHSTART**](event-constants.md)           | Nicht relevant                                                                                                            |
| [**EVENT \_ SYSTEM \_ SWITCHEND**](event-constants.md)               | Nicht relevant                                                                                                            |
| [**EVENT \_ SYSTEM \_ MINIMIZESTART**](event-constants.md)       |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ MINIMIZEEND**](event-constants.md)           |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ FOREGROUND**](event-constants.md)             |                                                                                                                         |
| [**SCROLLEN \_ DES \_ EREIGNISSYSTEMSSTART**](event-constants.md)     | Nicht verfügbar                                                                                                           |
| [**EVENT \_ SYSTEM \_ SCROLLINGEND**](event-constants.md)         | Nicht verfügbar                                                                                                           |



 



| Object-Level-Ereigniskonst constants                                                           | Benutzeroberflächenautomatisierung                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_ \_ EREIGNISOBJEKTFOKUS**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**EVENT \_ OBJECT \_ VALUECHANGE**](event-constants.md)         | ValueProperty (Value-Steuerelementmuster und RangeValue-Steuerelementmuster)                   |
| [**\_ \_ EREIGNISOBJEKTAUSWAHL**](event-constants.md)             | ElementSelectedEvent (SelectionItem-Steuerelementmuster)                                   |
| [**\_ \_ EREIGNISOBJEKTAUSWAHLADD**](event-constants.md)       | ElementAddedToSelectionEvent (SelectionItem-Steuerelementmuster)                           |
| [**EVENT \_ OBJECT \_ SELECTIONREMOVE**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**EVENT \_ OBJECT \_ SELECTIONWITHIN**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**EVENT \_ OBJECT \_ STATECHANGE**](event-constants.md)         | Unter Benutzeroberflächenautomatisierung Eigenschaften und accState finden Sie Status, die eine Zustandsänderung auslösen. |



 

 

 




