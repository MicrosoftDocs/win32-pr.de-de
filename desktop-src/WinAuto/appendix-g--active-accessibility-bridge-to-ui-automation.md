---
title: Anhang G Active Accessibility Bridge zur Automatisierung der Benutzeroberfläche
description: Dieser Anhang enthält Informationen über die Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5fdc1ebc4d6e17781e383463974f78bb9334aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341852"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Anhang G: Active Accessibility Bridge zur Automatisierung der Benutzeroberfläche

Dieser Anhang enthält Informationen über die Microsoft Active Accessibility Bridge. Mit der Active Accessibility Bridge können Anwendungen, die Microsoft Active Accessibility implementieren, auf Anwendungen zugreifen, die die Microsoft-Benutzeroberflächen Automatisierung implementieren. Durch die Kombinieren von Microsoft Active Accessibility und der Benutzeroberflächen Automatisierung können Microsoft Active Accessibility-basierte Clients wie Screenreader unter Windows XP Programm gesteuert mit Benutzeroberflächenautomatisierungs-basierten Anbietern der Benutzeroberflächen Automatisierung interagieren, wie z. b. eine Windows Presentation Foundation Anwendung (WPF). Er ist Teil der systemeigenen Kern-API für die Benutzeroberflächen Automatisierung (UIAutomationCore.dll).

Mit der Active Accessibility Bridge werden Benutzeroberflächenautomatisierungs-Eigenschaften und-Ereignisse den Microsoft-Active Accessibility zugeordnet. In den folgenden Tabellen sind die Methoden und Eigenschaften der Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle der Benutzeroberflächen Automatisierung zugeordnet. Verwenden Sie diese Tabellen, um geeignete Programmierverfahren für die Entwicklung Ihres Microsoft Active Accessibility basierten Clients zu ermitteln.

### <a name="navigation-and-hierarchy-properties"></a>Navigations-und Hierarchie Eigenschaften



| IAccessible-Eigenschaft                                                     | UI-Automatisierungs Eigenschaft          |
|--------------------------------------------------------------------------|---------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Nicht implementiert                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Abgeleitet aus Benutzeroberflächenautomatisierungs-Struktur |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Abgeleitet aus Benutzeroberflächenautomatisierungs-Struktur |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | Nicht implementiert                 |



 

### <a name="descriptive-properties-and-methods"></a>Beschreibende Eigenschaften und Methoden



| IAccessible                                                                          | Benutzeroberflächenautomatisierung                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Ausführliche Informationen finden Sie in den Steuerelement Typen und der accRole-Tabelle.                                                                                                                                                                                                                                                                     |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Ausführliche Informationen finden Sie in den Steuerelement Typen und der accRole-Tabelle.                                                                                                                                                                                                                                                                     |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Accesskeypropertyor AcceleratorKeyProperty; Wenn beide vorhanden sind, hat AccessKeyProperty Vorrang.                                                                                                                                                                                                                         |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeProperty. Ausführliche Informationen finden Sie in den Steuerelement Typen und der accRole-Tabelle.                                                                                                                                                                                                                                                |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Ausführliche Informationen finden Sie in den Steuerelement Typen und der accRole-Tabelle.                                                                                                                                                                                                                                                                     |
| [**\_accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty wird für Steuerelement Typen unterstützt, die das [value](uiauto-implementingvalue.md) -Steuerelement Muster oder das Steuerelement Muster des [RangeValue](uiauto-implementingrangevalue.md) -Steuer Elements RangeValue-Werte entsprechen dem Verhalten von Microsoft Active Accessibility (0 bis 100). Value-Elemente verwenden eine Zeichenfolge. |
| [**Put- \_ Wert**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty Unterstützung für Steuerelement Typen, die das [value](uiauto-implementingvalue.md) -Steuerelement Muster oder das [RangeValue](uiauto-implementingrangevalue.md) -Steuerelement Muster                                                                                                                                      |
| [**\_accHelp erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Nicht implementiert                                                                                                                                                                                                                                                                                                          |
| [**\_accHelpTopic erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | Nicht implementiert                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Steuerelement Typen und Zugriffs Rolle

Die Standard Rolle von Microsoft Active Accessibility ist [**role \_ System \_ Client**](object-roles.md). Wenn für einen Steuer Objekttyp keine Standardaktion gefunden wird, werden von der Active Accessibility Bridge auch die folgenden verfügbaren Steuerelement Muster verwendet: " [aufrufen](uiauto-implementinginvoke.md)", " [ExpandCollapse](uiauto-implementingexpandcollapse.md)" und " [Umschalten](uiauto-implementingtoggle.md)". Beispielsweise verfügt ein GroupBox-Steuerelement nicht über eine Standardaktion. Wenn Sie ExpandCollapse unterstützt, wird diese von der Active Accessibility Bridge für die Standardaktion verwendet.



| Benutzeroberflächenautomatisierungs-Steuerelement                              | accRole                                                                     | Standardaktion                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Schaltfläche](uiauto-supportbuttoncontroltype.md)           | [**\_ \_ Schaltfläche "Rollen System"**](object-roles.md)     | Tastenkombination                                                    |
| [Kalender](uiauto-supportcalendarcontroltype.md)       | [**Rollen \_ System \_ Client**](object-roles.md)             | Keine                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**\_ \_ Kontrollkästchen für Rollen System**](object-roles.md)   | Aktivieren/deaktivieren (Umschalten)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**Kombinations \_ Feld "Rollen System" \_**](object-roles.md)         | Keine                                                     |
| Benutzerdefiniert                                                  | [**Rollen \_ System \_ Client**](object-roles.md)             | Keine                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**Liste der Rollen \_ Systeme \_**](object-roles.md)                 | Keine                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**Rollen \_ System ( \_ ListItem)**](object-roles.md)         | Keine                                                     |
| [Dokument](uiauto-supportdocumentcontroltype.md)       | [**Rollen \_ System \_ Dokument**](object-roles.md)         | Keine                                                     |
| [Bearbeiten](uiauto-supporteditcontroltype.md)               | [**Rollen \_ System \_ Text**](object-roles.md)                 | Keine                                                     |
| [Gruppieren](uiauto-supportgroupcontroltype.md)             | [**Rollen \_ System \_ Gruppierung**](object-roles.md)         | Keine                                                     |
| [Header](uiauto-supportheadercontroltype.md)           | [**Liste der Rollen \_ Systeme \_**](object-roles.md)                 | Keine                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**Rollen \_ System- \_ ColumnHeader**](object-roles.md) | Klicken Sie auf                                                    |
| [Link](uiauto-supporthyperlinkcontroltype.md)     | [**Rollen \_ System \_ Link**](object-roles.md)                 | Springen (Zuordnungen zum Aufrufen)                                    |
| [Image](uiauto-supportimagecontroltype.md)             | [**Grafik zum Rollen \_ System \_**](object-roles.md)           | Keine                                                     |
| [Liste](uiauto-supportlistcontroltype.md)               | [**Liste der Rollen \_ Systeme \_**](object-roles.md)                 | Keine                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**Rollen \_ System ( \_ ListItem)**](object-roles.md)         | Doppelklick                                             |
| [Menü](uiauto-supportmenucontroltype.md)               | [**Rollen \_ System- \_ menupup**](object-roles.md)       | Keine                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**Rollen \_ System- \_ Menüleiste**](object-roles.md)           | Keine                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**Rollen \_ System ( \_ MenuItem)**](object-roles.md)         | Ausführen oder öffnen/schließen für Menü Elemente mit untergeordneten Elementen. |
| [Bereich](uiauto-supportpanecontroltype.md)               | [**Bereich "Rollen \_ System" \_**](object-roles.md)                 | Keine                                                     |
| [ProgressBar](uiauto-supportprogressbarcontroltype.md) | [**Rollen \_ System- \_ ProgressBar**](object-roles.md)   | Keine                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**Optionsfeld "Rollen \_ System" \_**](object-roles.md)   | Azure Functions                                                    |
| [Bild Lauf Leiste](uiauto-supportscrollbarcontroltype.md)     | [**Rollen \_ System- \_ Scrollleiste**](object-roles.md)       | Keine                                                     |
| [Schieberegler](uiauto-supportslidercontroltype.md)           | [**\_ \_ Schieberegler für Rollen System**](object-roles.md)             | Keine                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**\_SpinButton für Rollen System \_**](object-roles.md)     | Keine                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**Rollen \_ System ( \_ SplitButton)**](object-roles.md)   | Keine                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**\_ \_ Statusleiste des Rollen Systems**](object-roles.md)       | Keine                                                     |
| [TAB](uiauto-supporttabcontroltype.md)                 | [**\_ \_ pagetablist für Rollen System**](object-roles.md)   | Keine                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**Rollen \_ System- \_ pgetab**](object-roles.md)           | Schalter                                                   |
| [Table](uiauto-supporttablecontroltype.md)             | [**Rollen \_ System \_ Tabelle**](object-roles.md)               | Keine                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**Rollen \_ System- \_ StaticText**](object-roles.md)     | Keine                                                     |
| [Thumb](uiauto-supportthumbcontroltype.md)             | [**Rollen \_ System \_ Indikator**](object-roles.md)       | Keine                                                     |
| [TitleBar](uiauto-supporttitlebarcontroltype.md)       | [**Rollen \_ System- \_ TitleBar**](object-roles.md)         | Keine                                                     |
| [Suchfeld](uiauto-supporttoolbarcontroltype.md)         | [**Rollen \_ System- \_ Symbolleiste**](object-roles.md)           | Keine                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**Rollen System-QuickInfo \_ \_**](object-roles.md)           | Keine                                                     |
| [Struktur](uiauto-supporttreecontroltype.md)               | [**Rollen \_ System Gliederung \_**](object-roles.md)           | Keine                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**Rollen \_ System \_ outlineitem**](object-roles.md)   | Erweitern oder reduzieren                                       |
| [Fenster](uiauto-supportwindowcontroltype.md)           | [**Rollen \_ System \_ Fenster**](object-roles.md)             | Keine                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Benutzeroberflächenautomatisierungs-Eigenschaften und accState



| accState                                                                                      | UI-Automatisierungs Eigenschaft                                                                                                                                                        | Löst Statusänderungen aus. |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**Zustands \_ System \_ aktiviert**](object-state-constants.md)                 | Verwenden Sie für ControlType = "CheckBox" den Befehl "degglestate. on". Verwenden Sie für "RadioButton" [ **SelectionItemPattern:: issgewählt**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Ja                   |
| [**Zustands \_ System- \_ Fokus verwendbar**](object-state-constants.md)             | Iskeyboardfoc. ableproperty                                                                                                                                                   | Nein                    |
| [**Zustands \_ System mit \_ Fokus**](object-state-constants.md)                 | Haskeyboardfocusproperty                                                                                                                                                      | Nein                    |
| [**Zustands \_ System \_ geschützt**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | Nein                    |
| [**Zustands \_ System schreibgeschützt \_**](object-state-constants.md)               | Isread onlyproperty (Value-Steuerelement Muster und RangeValue-Steuerelement Muster)                                                                                                     | Nein                    |
| [**Zustands \_ System nicht \_ verfügbar**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Ja                   |
| [**\_ \_ verknüpftes Zustands System**](object-state-constants.md)                   | ControlTypeProperty = "Hyperlink"                                                                                                                                             | Nein                    |
| [**\_auswählbares Zustands System \_**](object-state-constants.md)           | SelectionItemPattern wird unterstützt.                                                                                                                                             | Nein                    |
| [**Zustands \_ System \_ ausgewählt**](object-state-constants.md)               | IsSelectedProperty (SelectionItem-Steuerelement Muster)                                                                                                                            | Nein                    |
| [**Zustands \_ System \_ reduziert**](object-state-constants.md)             | Expandredusinstate = reduziert                                                                                                                                               | Ja                   |
| [**Zustands \_ System \_ erweitert**](object-state-constants.md)               | Expandreduzstate = erweitert oder partiallyexpanded                                                                                                                           | Ja                   |
| [**\_haspopup des Zustands Systems \_**](object-state-constants.md)               | Menü Elemente, die erweitern/reduzieren unterstützen                                                                                                                                       | Nein                    |
| [**Zustands \_ System \_ gemischt**](object-state-constants.md)                     | "Zu" wechseln                                                                                                                                                   | Nein                    |
| [**\_beträchtliche Zustands System \_**](object-state-constants.md)               | [**Iuiautomationtransformpattern:: CanResize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | Nein                    |
| [**Zustands \_ System kann nicht aktualisiert werden \_**](object-state-constants.md)               | [**Iuiautomationtransformpattern:: CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | Nein                    |
| [**\_ \_ mehr wählbares Zustands System**](object-state-constants.md) | [**Iuiautomationselectionpattern:: CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | Nein                    |



 

### <a name="selection-and-focus"></a>Auswahl und Fokus



| IAccessible                                                            | Benutzeroberflächenautomatisierung                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**Iuiautomation:: focucements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Weitere Informationen finden Sie in den Eigenschaften der Benutzeroberflächenautomatisierungs-Eigenschaft und der accSelect-Tabelle             |
| [**\_Zugriffs Auswahl**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern:: GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Benutzeroberflächenautomatisierungs-Eigenschaften und accSelect-selflags



| Auswählen von selflags                                                  | UI-Automatisierungs Eigenschaft                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**selflag " \_ None"**](selflag.md)                       | Nicht verfügbar                                                                                                                  |
| selflag " \_ takfocus"                                                   | [**Iuiautomationelement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**selflag \_ TakeSelection**](selflag.md)     | [**Iuiautomationselectionitempattern:: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**selflag \_ AddSelection**](selflag.md)       | [**Iuiautomationselectionitempattern:: addopselection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| selflag \_ takeremoveselection                                        | [**Iuiautomationselectionitempattern:: RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**selflag- \_ ExtendSelection**](selflag.md) | Nicht verfügbar                                                                                                                  |



 

### <a name="spatial-mapping"></a>Räumliche Zuordnung



| IAccessible                                                 | Benutzeroberflächenautomatisierung                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | Boundingrechgleproperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot:: elementproviderfrompoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Ereignisse



| System-Level von Ereignis Konstanten                                                             | Benutzeroberflächenautomatisierung                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ menupopupstart für das Ereignis System**](event-constants.md)     | [**UIA \_ Menuopenedeventid**](uiauto-event-ids.md) (Hinweis: muss überprüfen, ob es sich um ein Popup Fenster handelt.) |
| [**\_ \_ menupopupend für das Ereignis System**](event-constants.md)         | [**UIA \_ menuclosedebug**](uiauto-event-ids.md)                                                |
| [**MenuStart für das Ereignis \_ System \_**](event-constants.md)               | [**UIA \_ menumodestarteventid**](uiauto-event-ids.md)                                          |
| [**MenuEnd für das Ereignis \_ System \_**](event-constants.md)                   | [**UIA \_ menumodeendeventid**](uiauto-event-ids.md)                                              |
| [**Sound des Ereignis \_ Systems \_**](event-constants.md)                       |                                                                                                                         |
| [**Ereignis \_ System \_ Warnung**](event-constants.md)                       |                                                                                                                         |
| [**Event \_ System- \_ capturestart**](event-constants.md)         |                                                                                                                         |
| [**Ereignis \_ System- \_ captureend**](event-constants.md)             |                                                                                                                         |
| [**\_ \_ dialogstart des Ereignis Systems**](event-constants.md)           |                                                                                                                         |
| [**dialogend für das Ereignis \_ System \_**](event-constants.md)               |                                                                                                                         |
| [**Ereignis \_ System " \_ muvesizestart"**](event-constants.md)       |                                                                                                                         |
| [**Ereignis \_ System-" \_ muvesizeend"**](event-constants.md)           |                                                                                                                         |
| [**Ereignis \_ System \_ contexthelpstart**](event-constants.md) |                                                                                                                         |
| [**Ereignis \_ System \_ contexthelpend**](event-constants.md)     | Nicht relevant                                                                                                            |
| [**Ereignis \_ System \_ dragdropstart**](event-constants.md)       |                                                                                                                         |
| [**Ereignis \_ System \_ dragdropend**](event-constants.md)           |                                                                                                                         |
| [**\_Neustarts des Ereignis Systems \_**](event-constants.md)           | Nicht relevant                                                                                                            |
| [**Umschaltung des Ereignis \_ Systems \_**](event-constants.md)               | Nicht relevant                                                                                                            |
| [**Ereignis \_ System \_ minimizestart**](event-constants.md)       |                                                                                                                         |
| [**Ereignis \_ System \_ minimizeend**](event-constants.md)           |                                                                                                                         |
| [**\_ \_ Vordergrund des Ereignis Systems**](event-constants.md)             |                                                                                                                         |
| [**Ereignis \_ System- \_ scrollingstart**](event-constants.md)     | Nicht verfügbar                                                                                                           |
| [**\_ \_ ereignissystemscrollingend**](event-constants.md)         | Nicht verfügbar                                                                                                           |



 



| Object-Level von Ereignis Konstanten                                                           | Benutzeroberflächenautomatisierung                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**Ereignis \_ Objekt \_ Fokus**](event-constants.md)                     | Automationfocuschangede Vent                                                            |
| [**\_ValueChange für das Ereignis Objekt \_**](event-constants.md)         | ValueProperty (Value-Steuerelement Muster und RangeValue-Steuerelement Muster)                   |
| [**Ereignis \_ Objekt \_ Auswahl**](event-constants.md)             | ElementSelectedEvent (SelectionItem-Steuerelement Muster)                                   |
| [**Ereignis \_ Objekt \_ selectionadd**](event-constants.md)       | ElementAddedToSelectionEvent (SelectionItem-Steuerelement Muster)                           |
| [**Ereignis \_ Objekt \_ SelectionRemove**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**\_ \_ ereignisobjektselectionwithin**](event-constants.md) | Eventsselectioninvalidatedevent                                                        |
| [**Ereignis \_ Objekt \_ StateChange**](event-constants.md)         | Zustände, die eine Statusänderung auslöst, finden Sie unter Benutzeroberflächenautomatisierungs-Eigenschaften und accState-Tabelle |



 

 

 




