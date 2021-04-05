---
title: Iaccessibleex-Implementierungs Richtlinien
description: Microsoft UI Automation Core kann alle Eigenschaften von Microsoft Active Accessibility für alle zugänglichen Objekte abrufen, die von einem Server über die Schnittstelle "IAccessible" verfügbar gemacht werden.
ms.assetid: d047127c-1be2-4f34-bb97-330b5509ca0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82403a51e4848142a26194a98dce3922619b06f4
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103719994"
---
# <a name="iaccessibleex-implementation-guidelines"></a>Iaccessibleex-Implementierungs Richtlinien

Microsoft UI Automation Core kann alle Eigenschaften von Microsoft Active Accessibility für alle zugänglichen Objekte abrufen, die von einem Server über die Schnittstelle " [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) " verfügbar gemacht werden. Beim Implementieren von [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)müssen Sie nur die Aspekte der UI-Funktionalität verfügbar machen, die andernfalls nicht durch vorhandene Microsoft Active Accessibility-Eigenschaften verfügbar gemacht werden können. In diesem Thema werden die Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster beschrieben, die Benutzeroberflächen Funktionen darstellen, die keine Entsprechung in Microsoft Active Accessibility – Sie sind die Eigenschaften und Steuerelement Muster, die Sie in einer **iaccessibleex** -Implementierung verfügbar machen können.

Dieses Thema enthält folgende Abschnitte:

-   [Eigenschaften](#properties)
-   [Steuerelement Muster](#control-patterns)
-   [Ereignisse für geänderte Benutzeroberflächenautomatisierungs-Eigenschaften](#winevents-for-ui-automation-property-changed-events)
-   [Zugehörige Themen](#related-topics)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften der Benutzeroberflächen Automatisierung überlappen sich nicht mit der Microsoft Active Accessibility-Funktionalität. Sie können in einer [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung verwendet werden:

-   Ariaproperties
-   Ariarole
-   AutomationID
-   ClassName
-   Clickablepoint
-   Controllerfor
-   Kultur
-   DescribedBy
-   Flowsto
-   FrameworkId
-   IsContentElement
-   IsControlElement
-   Isdatavalidforform
-   Isrequirements dforform
-   ItemStatus
-   ItemType
-   LabeledBy
-   LocalizedControlType
-   Orientation

Obwohl sich die Eigenschaften der Benutzeroberflächen Automatisierung von AcceleratorKey und Accesskey mit der Eigenschaft accKeyboardShortcut Microsoft Active Accessibility überschneiden, können Sie Sie in einer [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung für Steuerelemente verwenden, die über eine Zugriffstaste und eine Zugriffstaste verfügen. Ebenso überlappt die ControlType-Benutzeroberflächenautomatisierungs-Eigenschaft mit der Microsoft Active Accessibility accRole-Eigenschaft, aber Sie können Sie in einer **iaccessibleex** -Implementierung weiterhin verwenden, um eine spezifischere Rolle für ein Steuerelement zu definieren.

Da die folgenden Eigenschaften des Benutzeroberflächenautomatisierungs-Elements bereits von den Eigenschaften von Microsoft Active Accessibility abgedeckt werden, ist es nicht erforderlich, Sie in einer [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung zu verwenden.



| Benutzeroberflächenautomatisierungs-Eigenschaft | Microsoft Active Accessibility-Entsprechung                                                                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boundingrechteck      | accLocation                                                                                                                                                                   |
| HasKeyboardFocus       | accState, [ **Zustands \_ System \_ fokussiert**](object-state-constants.md)                                                                                       |
| isEnabled              | accState, [ **Zustands \_ System nicht \_ verfügbar**](object-state-constants.md)                                                                               |
| Iskeyboardfocverwendbar    | accState, [ **Zustands \_ \_ Systemfokus verwendbar**](object-state-constants.md)                                                                                   |
| IsPassword             | accState, [ **Zustands \_ System \_ geschützt**](object-state-constants.md)                                                                                   |
| HelpText               | accHelp                                                                                                                                                                       |
| Name                   | accName                                                                                                                                                                       |
| Nativewindowhandle     | [**Windowfromaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)                                                                                                              |
| IsOffscreen            | accState, [**Status \_ System \_ unsichtbar**](object-state-constants.md)Status / [**\_ System \_ Offscreen**](object-state-constants.md) |
| ProcessId              | Bereitgestellt von UI Automation Core                                                                                                                                                |



 

Für jede nicht unterstützte Benutzeroberflächenautomatisierungs-Eigenschaft sollte Ihre Implementierung der [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) -Methode den *pRetVal* -Parameter auf VT \_ Empty festlegen und S OK zurückgeben \_ . Die Rückgabe von [**UIA \_ E \_ NotSupported**](uiauto-error-codes.md) kann dazu führen, dass der MSAA-to-UIA-Proxy die Standard Zuordnung für die entsprechende Eigenschaft entfernt.

## <a name="control-patterns"></a>Steuerelement Muster

Die folgenden Benutzeroberflächenautomatisierungs-Steuerelement Muster überlappen sich nicht mit der Microsoft Active Accessibility-Funktionalität Sie können in einer [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung verwendet werden:

-   Andocken
-   Erweitern_Reduzieren
-   Raster
-   GridItem
-   MultipleView
-   RangeValue
-   Scroll
-   ScrollItem
-   SynchronizedInput
-   Tabelle
-   TableItem
-   Transformieren

Für die RangeValue-und Transformations-Steuerelement Muster überlappen sich einige Methoden zwischen dem Benutzeroberflächenautomatisierungs-Steuerelement Muster und den Microsoft Active Accessibility-Methoden In diesen Fällen müssen beide implementiert werden. Beispielsweise müssen sowohl die [**IAccessible:: get- \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) -als auch die [**IAccessible::p UT- \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue) -Methode von Microsoft Active Accessibility implementiert werden. Dies gilt auch für die Benutzeroberflächenautomatisierungs-Methode [**IRangeValueProvider:: Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) und [**IRangeValueProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue) . Intern kann eine Implementierung Code für diese freigeben. Diese Anforderung, beide Sätze zu implementieren, vermeidet eine partielle Implementierung einer Muster Schnittstelle, während die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle beibehalten wird, die von vorhandenen Microsoft Active Accessibility-Clients verwendet werden kann.

Die folgenden Steuerelement Muster für die Benutzeroberflächen Automatisierung sind nicht erforderlich, wenn das-Steuerelement eine der unten aufgeführten Rollen aufweist. Andernfalls sollten Sie explizit unterstützt werden, wenn Sie relevant sind.



| Steuerelement Muster für Benutzeroberflächen Automatisierung | Microsoft Active Accessibility-Rolle                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvokePattern                 | [**Rolle \_ System \_ PUSHBUTTON**](object-roles.md), [**Rollen \_ System- \_ MenuItem**](object-roles.md), [**\_ \_ ButtonDropDown-Dropdown**](object-roles.md)Liste, [**Rollen \_ System \_**](object-roles.md)und eine beliebige andere Rolle, bei der der Wert der accdefaultaction-Eigenschaft nicht **null** ist. |
| "SelectionItemPattern"          | [**Rolle \_ Optionsfeld "System \_ ListItem**](object-roles.md)", " [ **Rollen \_ System \_** "](object-roles.md)                                                                                                                                                                                                                                                 |
| SelectionPattern              | [**Liste der Rollen \_ Systeme \_**](object-roles.md)                                                                                                                                                                                                                                                                                                                                    |
| TogglePattern                 | [**\_ \_ Kontrollkästchen für Rollen System**](object-roles.md)                                                                                                                                                                                                                                                                                                                      |
| ValuePattern                  | [**Rolle \_ System \_ Text**](object-roles.md) (wenn er nicht schreibgeschützt ist), [**role \_ System \_ ProgressBar**](object-roles.md), [**\_ \_ ComboBox für das Rollensystem**](object-roles.md)und jede andere Rolle, wenn der Wert der accValue-Eigenschaft nicht **null** ist.                                                                            |
| WindowPattern                 | Wird automatisch auf den Microsoft-Win32- **HWND**-s der obersten Ebene unterstützt.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="winevents-for-ui-automation-property-changed-events"></a>Ereignisse für geänderte Benutzeroberflächenautomatisierungs-Eigenschaften

Zusätzlich zu den Ereignissen, die für [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)definiert sind, werden auch die folgenden Ereignis Bezeichner definiert, die mit einer [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung als geänderte Ereignisse für die Benutzeroberflächen Automatisierung verwendet werden können. Diese verwenden denselben Mechanismus wie die für **IAccessible** definierten Ereignisse. Weitere Informationen finden Sie unter [WinEvents](winevents-infrastructure.md).



| WinEvent-ID für iaccessibleex-Implementierungen                                                                                              | Zugehörige WinEvent-ID von Microsoft Active Accessibility                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**UIA \_ ariapropertiespropertyid**](uiauto-automation-element-propids.md)                                    | Keine                                                                                   |
| [**UIA \_ ariarolepropertyid**](uiauto-automation-element-propids.md)                                                | Keine                                                                                   |
| [**UIA \_ controllerforpropertyid**](uiauto-automation-element-propids.md)                                      | Keine                                                                                   |
| [**UIA \_ describedbypropertyid**](uiauto-automation-element-propids.md)                                          | Keine                                                                                   |
| [**UIA \_ expandredu-expandredutstatepropertyid**](uiauto-control-pattern-propids.md) | [**Ereignis \_ Objekt \_ StateChange**](event-constants.md)         |
| [**UIA \_ flowstopropertyid**](uiauto-automation-element-propids.md)                                                  | Keine                                                                                   |
| [**UIA \_ inputverwerdde ventid**](uiauto-event-ids.md)                                                           | Keine                                                                                   |
| [**UIA \_ inputreachedotherelementeventid**](uiauto-event-ids.md)                                       | Keine                                                                                   |
| [**UIA \_ inputreachedtargeteventid**](uiauto-event-ids.md)                                                   | Keine                                                                                   |
| [**UIA \_ isdatavalidforformpropertyid**](uiauto-automation-element-propids.md)                            | Keine                                                                                   |
| [**UIA \_ isenabledpropertyid**](uiauto-automation-element-propids.md)                                              | [**Ereignis \_ Objekt \_ StateChange**](event-constants.md)         |
| [**UIA \_ itemstatuspropertyid**](uiauto-automation-element-propids.md)                                            | Keine                                                                                   |
| [**UIA \_ multipleviewcurrentviewpropertyid**](uiauto-control-pattern-propids.md)                     | Keine                                                                                   |
| [**UIA \_ scrollhorizontallyscrollablepropertyid**](uiauto-control-pattern-propids.md)           | Keine                                                                                   |
| [**UIA \_ scrollhorizontalscrollprozpropertyid**](uiauto-control-pattern-propids.md)         | [**Ereignis \_ Objekt- \_ contentscrollt**](event-constants.md) |
| [**UIA \_ scrollhorizontalviewsizepropertyid**](uiauto-control-pattern-propids.md)                   | Keine                                                                                   |
| [**UIA \_ scrollverticallyscrollablepropertyid**](uiauto-control-pattern-propids.md)               | Keine                                                                                   |
| [**UIA \_ scrollverticalscrollprozpropertyid**](uiauto-control-pattern-propids.md)             | [**Ereignis \_ Objekt- \_ contentscrollt**](event-constants.md) |
| [**UIA \_ scrollverticalviewsizepropertyid**](uiauto-control-pattern-propids.md)                       | Keine                                                                                   |
| [**UIA \_ toggletogglestatepropertyid**](uiauto-control-pattern-propids.md)                                 | [**Ereignis \_ Objekt \_ StateChange**](event-constants.md)         |



 

Für die oben aufgeführten Ereignisse, bei denen ein Ereignis \_ Objekt \_ Wert angezeigt wird, sollte die [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Implementierung dieses Ereignis zusätzlich zum aufgelisteten geänderten Ereignis auslösen. Dadurch kann vorhandener **iaccessibleex** -Client Code weiter ausgeführt werden, während gleichzeitig präzisetere Ereignis Informationen an interessierte Clients übermittelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Die iaccessibleex-Schnittstelle](iaccessibleex.md)
</dt> </dl>

 

 




