---
title: Wertsteuermuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IValueProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Value-Steuerelementmusters
- Benutzeroberflächenautomatisierung,Wert-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IValueProvider
- IValueProvider
- Implementieren Benutzeroberflächenautomatisierung Value-Steuerelementmustern
- Wertsteuermuster
- Steuerelementmuster, IValueProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung Value
- Steuerelementmuster, Wert
- interfaces,IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b30d8c84bc5f998d55ee17d7699bb37f33b7e19c52a2694578c3d11ef1d888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997805"
---
# <a name="value-control-pattern"></a>Wertsteuermuster

Beschreibt Richtlinien und Konventionen für die Implementierung [**von IValueProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **Value-Steuerelementmuster** wird verwendet, um Steuerelemente zu unterstützen, die über einen systeminternen Wert verfügen, der keinen Bereich umfasst und als Zeichenfolge dargestellt werden kann.

Die Wertzeichenfolge kann abhängig vom Steuerelement und seinen Einstellungen bearbeitet werden. Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IValueProvider**](#required-members-for-ivalueprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des Value-Steuerelementmusters die folgenden Richtlinien und Konventionen: 

-   Steuerelemente wie ein Listenelement oder Strukturelement müssen das **Value-Steuerelementmuster** unterstützen, wenn der Wert eines der Elemente unabhängig vom aktuellen Bearbeitungsmodus des Steuerelements bearbeitet werden kann. Das übergeordnete Steuerelement muss  auch das Value-Steuerelementmuster unterstützen, wenn die untergeordneten Elemente bearbeitet werden können. Die folgende Abbildung zeigt ein Beispiel für ein bearbeitbares Listenelement.

    ![Abbildung mit bearbeitbarem Listenelement](images/uia-valuepattern-editable-listitem.jpg)

- Ein- und mehrzeilenbasierte Bearbeitungssteuerelemente müssen [**ITextProvider implementieren,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) um ihren schreibgeschützten Inhalt verfügbar zu machen.
- Mehrzeilen-Bearbeitungssteuerelemente müssen [**IValueProvider implementieren,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) wenn ihre Inhalte geändert werden können.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) unterstützt das Abrufen von Formatierungsinformationen oder Teilzeichenfolgenwerten nicht. Implementieren [**Sie ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in diesen Szenarien.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) muss durch Steuerelemente wie das Farbauswahlauswahl-Steuerelement von Microsoft Word implementiert werden (siehe folgende Abbildung), das die Zeichenfolgenzuordnung zwischen einem Farbwert (z. B. "gelb") und einem entsprechenden internen [RGB-Wert](/windows/win32/api/wingdi/nf-wingdi-rgb) unterstützt.

    ![Abbildung, die die Zuordnung von Farbmusterzeichenfolgen zeigt](images/uia-valuepattern-colorpicker.jpg)

- Für ein Steuerelement muss die **IsEnabled-Eigenschaft** auf **TRUE** und die [**ITextProvider::IsReadOnly-Eigenschaft**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) auf **FALSE** festgelegt sein, bevor ein Aufruf von [**ITextProvider::SetValue erlaubt wird.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)

## <a name="required-members-for-ivalueprovider"></a>Erforderliche Member für **IValueProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IValueProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) erforderlich.



| Erforderliche Member                                       | Memberart | Hinweise |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | Eigenschaft    | Keine  |
| [**Wert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | Eigenschaft    | Keine  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und ihre unterstützten Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Text- und TextRange-Steuerelementmuster](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 