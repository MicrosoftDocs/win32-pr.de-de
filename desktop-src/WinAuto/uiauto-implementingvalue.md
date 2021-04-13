---
title: Value-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IValueProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Value-Steuerelement Musters
- UI-Automatisierung, wertsteuer Element Muster
- UI-Automatisierung, IValueProvider
- IValueProvider
- Implementieren von Wert Steuerungs Mustern für Benutzeroberflächen Automatisierung
- Wertsteuer Element Muster
- Steuerelement Muster, IValueProvider
- Steuerelement Muster, Implementieren des Benutzeroberflächenautomatisierungs-Werts
- Steuerelement Muster, Wert
- Schnittstellen, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390656"
---
# <a name="value-control-pattern"></a>Value-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **value** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die einen systeminternen Wert aufweisen, der nicht einen Bereich umfasst und als Zeichenfolge dargestellt werden kann.

Die Wert Zeichenfolge kann je nach Steuerelement und den zugehörigen Einstellungen bearbeitet werden können. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IValueProvider**](#required-members-for-ivalueprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **value** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Steuerelemente wie ein Listenelement oder Strukturelement müssen das **value** -Steuerelement Muster unterstützen, wenn der Wert eines der Elemente unabhängig vom aktuellen Bearbeitungsmodus des Steuer Elements bearbeitet werden kann. Das übergeordnete Steuerelement muss auch das **value** -Steuerelement Muster unterstützen, wenn die untergeordneten Elemente bearbeitet werden können. Die folgende Abbildung zeigt ein Beispiel für ein bearbeitbares Listenelement.

    ![Darstellung des bearbeitbaren Listen Elements](images/uia-valuepattern-editable-listitem.jpg)

- Ein-und mehrzeilige Bearbeitungs Steuerelemente müssen [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) implementieren, um Ihren schreibgeschützten Inhalt verfügbar zu machen.
- Mehrzeilige Bearbeitungs Steuerelemente müssen [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) implementieren, wenn deren Inhalt geändert werden kann.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) unterstützt nicht das Abrufen von Formatierungsinformationen oder Teil Zeichenfolgen-Werten. Implementieren Sie [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in diesen Szenarien.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) muss von Steuerelementen wie dem Auswahl Steuerelement für die Farbauswahl von Microsoft Word (siehe folgende Abbildung) implementiert werden, das die Zeichen folgen Zuordnung zwischen einem Farbwert (z. b. "gelb") und einem entsprechenden internen [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) -Wert unterstützt.

    ![Abbildung zur Darstellung der Zeichen folgen Zuordnung von Farbmustern](images/uia-valuepattern-colorpicker.jpg)

- Für ein Steuerelement sollte dessen **isaktivierte** Eigenschaft auf **true** festgelegt sein, und die [**ITextProvider:: isread only**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) -Eigenschaft muss auf **false** festgelegt werden, bevor ein Aufrufen von [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)zugelassen wird.

## <a name="required-members-for-ivalueprovider"></a>Erforderliche Member für **IValueProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                       | Memberart | Hinweise |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | Eigenschaft    | Keine  |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | Eigenschaft    | Keine  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Text-und TextRange-Steuerelement Muster](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 