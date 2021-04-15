---
title: Description-Eigenschaft (Windows-Barrierefreiheits Funktionen)
description: Die Description-Eigenschaft eines Objekts stellt eine Textbeschreibung zur visuellen Darstellung eines Objekts bereit.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474979"
---
# <a name="description-property-windows-accessibility-features"></a>Description-Eigenschaft (Windows-Barrierefreiheits Funktionen)

> [!Note]  
> Die **Description** -Eigenschaft wird häufig falsch verwendet und wird nicht von der Microsoft-Benutzeroberflächen Automatisierung unterstützt. Microsoft Active Accessibility Server-Entwickler sollten diese Eigenschaft nicht verwenden. Wenn weitere Informationen für Barrierefreiheits-und Automatisierungs Szenarien erforderlich sind, verwenden Sie die Eigenschaften, die von Benutzeroberflächenautomatisierungs-Elementen und Steuerelement Mustern unterstützt

 

Die **Description** -Eigenschaft eines Objekts stellt eine Textbeschreibung zur visuellen Darstellung eines Objekts bereit. Die Beschreibung wird hauptsächlich verwendet, um einen größeren Kontext für sehorientierte oder Blind Benutzer bereitzustellen, wird jedoch auch für die Kontextsuche oder andere Anwendungen verwendet. Mit dieser Eigenschaft können Benutzer ein Symbol oder die visuelle Darstellung in der Gesamtdarstellung verstehen.

Die **Description** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)abgerufen.

## <a name="when-to-support-the-description-property"></a>Unterstützung der Description-Eigenschaft

Server unterstützen die **Description** -Eigenschaft, wenn die Beschreibung nicht offensichtlich ist, oder wenn Sie auf der Grundlage der [**Eigenschaften Name**](name-property.md), [**Rolle**](role-property.md), [**Zustand**](state-property.md)und [**Wert**](value-property.md) des Objekts nicht redundant ist. Eine Schaltfläche mit der Bezeichnung "OK" benötigt z. b. keine zusätzlichen Informationen, wohingegen eine Schaltfläche, die ein Bild eines Kakteen anzeigt, wäre. Die Eigenschaften " **Name**", " **Role**" und " [**Help**](help-property.md) " für eine solche Schaltfläche beschreiben den Zweck, aber die **Description** -Eigenschaft vermittelt weniger spürbare Informationen. Beispiel: "diese Schaltfläche zeigt ein Bild eines Kakteen an."

Ein Microsoft Active Accessibility Server kann die Unterstützung für die Benutzeroberflächen Automatisierung mithilfe der [direkten Anmerkung](direct-annotation.md), mithilfe der [**iaccessibleex**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) -Schnittstelle oder durch die parallele Implementierung von Microsoft Active Accessibility und UI-Automatisierung mit beiden Implementierungen hinzufügen, die die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der direkten Anmerkung](using-direct-annotation.md)
</dt> <dt>

[Die iaccessibleex-Schnittstelle](iaccessibleex.md)
</dt> </dl>

 

 




