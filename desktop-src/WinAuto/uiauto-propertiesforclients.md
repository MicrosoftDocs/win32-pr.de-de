---
title: Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elementen
description: Eigenschaften für IUIAutomationElement-Objekte enthalten Informationen über Benutzeroberflächenelemente, in der Regel Steuerelemente.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- Clients,Abrufen Benutzeroberflächenautomatisierung Elementen
- clients,Benutzeroberflächenautomatisierung Elements
- Clients,Eigenschaften
- Clients,Abrufen von Eigenschaften
- Clients,Benutzeroberflächenautomatisierung Eigenschaften
- Benutzeroberflächenautomatisierung,Abrufen von Elementen
- Benutzeroberflächenautomatisierung,Elements
- Benutzeroberflächenautomatisierung,Eigenschaften
- Benutzeroberflächenautomatisierung,Abrufen von Eigenschaften
- Abrufen von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbbe524e6f82f8c7dba018b24895ade54ced3e6a4632e1caefed410753b56fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564371"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Abrufen von Eigenschaften aus Benutzeroberflächenautomatisierung Elementen

Eigenschaften für [**IUIAutomationElement-Objekte**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) enthalten Informationen über Benutzeroberflächenelemente, in der Regel Steuerelemente. Die Eigenschaften eines Elements sind generisch. das heißt, nicht spezifisch für einen Steuerelementtyp. Steuerelementspezifische Eigenschaften eines Elements werden von seinen Steuerelementmusterschnittstellen verfügbar gemacht.

Microsoft Benutzeroberflächenautomatisierung-Eigenschaften sind schreibgeschützt. Um Eigenschaften eines Steuerelements festzulegen, müssen Sie die Methoden des entsprechenden Steuerelementmusters verwenden. Verwenden Sie beispielsweise [**IUIAutomationScrollPattern::Scroll,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) um die Positionswerte eines Scrollfensters zu ändern.

Um die Leistung zu verbessern, können Eigenschaftswerte von Steuerelementen und Steuerelementmustern zwischengespeichert werden, wenn Elemente abgerufen werden. Weitere Informationen finden Sie unter [Caching Benutzeroberflächenautomatisierung Properties and Control Patterns](uiauto-cachingforclients.md).

Dieses Thema enthält folgende Abschnitte:

-   [Eigenschaften-IDs](#property-ids)
-   [Eigenschaftsbedingungen](#property-conditions)
-   [Abrufen von Eigenschaften](#retrieving-properties)
-   [Standardeigenschaftswerte](#default-property-values)
-   [Zugehörige Themen](#related-topics)

## <a name="property-ids"></a>Eigenschaften-IDs

Eigenschaftsbezeichner werden in Uiautomationclient.h definiert. Sie werden verwendet, um Eigenschaften anzugeben, wenn Sie Durch Eigenschaften geänderte Ereignisse abonnieren, Eigenschaftswerte abrufen und Eigenschaftsbedingungen erstellen. Eigenschaftenbezeichner identifizieren auch die Eigenschaft, die sich geändert hat, wenn [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) aufgerufen wird.

Eine Liste der Eigenschaftenbezeichner Benutzeroberflächenautomatisierung Eigenschaftenbezeichner finden Sie unter [Eigenschaftenbezeichner](uiauto-entry-propids.md).

## <a name="property-conditions"></a>Eigenschaftsbedingungen

Die Eigenschaften-IDs werden zum Erstellen von [**IUIAutomationPropertyCondition-Objekten**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) verwendet, die zum Suchen nach Benutzeroberflächenautomatisierung werden. Beispielsweise können Sie ein Element mit einem bestimmten Namen oder alle aktivierten Steuerelemente suchen. Jede Eigenschaftsbedingung gibt einen Eigenschaftenbezeichner und den Wert an, mit dem die Eigenschaft übereinstimmen muss.

Weitere Informationen finden Sie unter den folgenden Referenzthemen:

-   [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**IUIAutomation::CreatePropertyConditionEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**IUIAutomationElement::FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**IUIAutomationElement::FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Abrufen von Eigenschaften

Einige generische Eigenschaften und alle Steuerelementmustereigenschaften sind als Eigenschaften auf der [**IUIAutomationElement-**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) oder Steuerelementmusterschnittstelle verfügbar und können mithilfe eines Accessors wie [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) oder [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition)abgerufen werden.

Darüber hinaus kann jede aktuelle oder zwischengespeicherte Eigenschaft (abgesehen von Steuerelementmustereigenschaften) mit einer der folgenden Methoden abgerufen werden:

-   [**Getcurrentpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**Getcachedpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Diese Methoden bieten eine etwas bessere Leistung und einen etwas besseren Zugriff auf den gesamten Bereich von Eigenschaften. Werte werden jedoch in [**VARIANT-Strukturen**](/windows/win32/api/oaidl/ns-oaidl-variant) zurückgegeben, während die einzelnen Eigenschaftenzugriffstypen den Wert in den entsprechenden Typ umstrukturieren.

## <a name="default-property-values"></a>Standardeigenschaftswerte

Wenn ein Benutzeroberflächenautomatisierung-Anbieter keine -Eigenschaft implementiert, Benutzeroberflächenautomatisierung einen Standardwert festlegen. Wenn der Anbieter für ein Steuerelement beispielsweise die durch [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)identifizierte Eigenschaft nicht unterstützt, gibt Benutzeroberflächenautomatisierung eine leere Zeichenfolge zurück. Wenn der Anbieter die durch [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md)identifizierte Eigenschaft nicht unterstützt, gibt Benutzeroberflächenautomatisierung **FALSE zurück.**

Der Unterschied zwischen [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) und [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (und zwischen ähnlichen Methodenpaaren) ist, dass die "Ex"-Methode angeben kann, dass kein Standardwert zurückgegeben werden soll. In diesem Fall ist der Rückgabewert eine spezielle eindeutige Konstante, die angibt, dass die -Eigenschaft nicht unterstützt wird. Bei Empfang dieses Werts kann die Anwendung einen eigenen Wert liefern oder einfach die -Eigenschaft ignorieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Eigenschaftsbezeichner](uiauto-entry-propids.md)
</dt> </dl>

 

 