---
title: Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen
description: Eigenschaften für iuiautomationelement-Objekte enthalten Informationen über Benutzeroberflächen Elemente, in der Regel Steuerelemente.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- Clients, Abrufen von Benutzeroberflächenautomatisierungs-Elementen
- Clients, Benutzeroberflächenautomatisierungs-Elemente
- Clients, Eigenschaften
- Clients, Abrufen von Eigenschaften
- Clients, Benutzeroberflächenautomatisierungs-Eigenschaften
- Benutzeroberflächen Automatisierung, Abrufen von Elementen
- Benutzeroberflächen Automatisierung, Elemente
- Benutzeroberflächen Automatisierung, Eigenschaften
- Benutzeroberflächen Automatisierung, Abrufen von Eigenschaften
- Abrufen von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337863"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierungs-Elementen

Eigenschaften für [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Objekte enthalten Informationen über Benutzeroberflächen Elemente, in der Regel Steuerelemente. Die Eigenschaften eines Elements sind generisch. Das heißt, nicht spezifisch für einen Steuer ungstyp. Steuerelement spezifische Eigenschaften eines Elements werden von seinen Steuerelement Muster-Schnittstellen verfügbar gemacht.

Microsoft UI Automation-Eigenschaften sind schreibgeschützt. Um Eigenschaften eines Steuerelements festzulegen, müssen Sie die Methoden des entsprechenden Steuerelementmusters verwenden. Verwenden Sie z. b. [**iuiautomationscrollpattern:: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) , um die Positionswerte eines scrollfensters zu ändern.

Um die Leistung zu verbessern, können Eigenschaftswerte von Steuerelementen und Steuerelement Mustern zwischengespeichert werden, wenn Elemente abgerufen werden. Weitere Informationen finden Sie unter zwischen [Speichern von Eigenschaften der Benutzeroberflächen Automatisierung und Steuerelement Mustern](uiauto-cachingforclients.md).

Dieses Thema enthält folgende Abschnitte:

-   [Eigenschaften-IDs](#property-ids)
-   [Eigenschaftsbedingungen](#property-conditions)
-   [Abrufen von Eigenschaften](#retrieving-properties)
-   [Standardeigenschaftswerte](#default-property-values)
-   [Zugehörige Themen](#related-topics)

## <a name="property-ids"></a>Eigenschaften-IDs

Eigenschafts Bezeichner werden in "UIAutomationClient. h" definiert. Sie werden verwendet, um Eigenschaften anzugeben, wenn Sie Eigenschaften geänderte Ereignisse abonnieren, Eigenschaftswerte abrufen und Eigenschafts Bedingungen erstellen. Eigenschafts Bezeichner identifizieren auch die Eigenschaft, die sich geändert hat, wenn [**iuiautomationpropertychangedebug:: shandpropertychangedebug**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) aufgerufen wird.

Eine Liste der Benutzeroberflächenautomatisierungs-Eigenschaften Bezeichner finden Sie unter [Property Identifiers](uiauto-entry-propids.md).

## <a name="property-conditions"></a>Eigenschaftsbedingungen

Die Eigenschaften-IDs werden zum Erstellen von [**iuiautomationpropertycondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) -Objekten verwendet, die für die Suche nach Benutzeroberflächenautomatisierungs-Elementen verwendet werden. Angenommen, Sie möchten ein Element mit einem bestimmten Namen oder alle aktivierten Steuerelemente suchen. Jede Eigenschafts Bedingung gibt einen Eigenschafts Bezeichner und den Wert an, dem die Eigenschaft entsprechen muss.

Weitere Informationen finden Sie unter den folgenden Referenzthemen:

-   [**Iuiautomation:: kreatepropertycondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**Iuiautomation:: kreatepropertyconditionex**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**Iuiautomationelement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**Iuiautomationelement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Abrufen von Eigenschaften

Einige generische Eigenschaften und alle Steuerelement Muster Eigenschaften sind als Eigenschaften in der [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -oder Steuerelement Muster-Schnittstelle verfügbar und können mithilfe eines Accessors, wie z. b. [**iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) oder [**cacheddockposition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition), abgerufen werden.

Darüber hinaus können alle aktuellen oder zwischengespeicherten Eigenschaften (mit Ausnahme der Eigenschaften von Steuerelement Mustern) mithilfe einer der folgenden Methoden abgerufen werden:

-   [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**Getcurrentpropertyvalueex**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**Getcachedpropertyvalueex**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Diese Methoden bieten eine etwas bessere Leistung und Zugriff auf den vollständigen Bereich von Eigenschaften. Werte werden jedoch in [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) -Strukturen zurückgegeben, während die einzelnen Eigenschaftenaccessoren den Wert in den entsprechenden Typ umwandeln.

## <a name="default-property-values"></a>Standardeigenschaftswerte

Wenn ein Benutzeroberflächenautomatisierungs-Anbieter eine Eigenschaft nicht implementiert, kann die Benutzeroberflächen Automatisierung einen Standardwert bereitstellen. Wenn z. b. der Anbieter für ein Steuerelement die von [**UIA \_ helptextpropertyid**](uiauto-automation-element-propids.md)identifizierte Eigenschaft nicht unterstützt, gibt die Benutzeroberflächen Automatisierung eine leere Zeichenfolge zurück. Wenn der Anbieter die durch [**UIA \_ isdockpatternavailablepropertyid**](uiauto-control-pattern-availability-propids.md)identifizierte Eigenschaft nicht unterstützt, gibt die Benutzeroberflächen Automatisierung auf ähnliche Weise **false** zurück.

Der Unterschied zwischen [**iuiautomationelement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) und [**getcurrentpropertyvalueex**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (und zwischen ähnlichen Methoden Paaren) besteht darin, dass die "ex"-Methode angeben kann, dass kein Standardwert zurückgegeben werden soll. In diesem Fall ist der Rückgabewert eine besondere eindeutige Konstante, die angibt, dass die Eigenschaft nicht unterstützt wird. Beim Empfang dieses Werts kann die Anwendung einen eigenen Wert bereitstellen oder die-Eigenschaft einfach ignorieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Eigenschaftsbezeichner](uiauto-entry-propids.md)
</dt> </dl>

 

 