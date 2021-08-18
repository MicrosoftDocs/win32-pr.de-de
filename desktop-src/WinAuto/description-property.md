---
title: Description-Eigenschaft (Windows Barrierefreiheitsfunktionen)
description: Die Description-Eigenschaft eines Objekts stellt eine Textbeschreibung zur visuellen Darstellung eines Objekts bereit.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c695ae4ed8968620776aa0786358c98372940749be4a1c4335cb89f84b373ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994230"
---
# <a name="description-property-windows-accessibility-features"></a>Description-Eigenschaft (Windows Barrierefreiheitsfunktionen)

> [!Note]  
> Die **Description-Eigenschaft** wird häufig falsch verwendet und wird von Microsoft Benutzeroberflächenautomatisierung nicht unterstützt. Microsoft Active Accessibility Serverentwickler sollten diese Eigenschaft nicht verwenden. Wenn weitere Informationen für Barrierefreiheits- und Automatisierungsszenarien erforderlich sind, verwenden Sie die Eigenschaften, die von Benutzeroberflächenautomatisierung Elementen und Steuerelementmustern unterstützt werden.

 

Die **Description-Eigenschaft** eines Objekts stellt eine Textbeschreibung zur visuellen Darstellung eines Objekts bereit. Die Beschreibung wird in erster Linie verwendet, um einen größeren Kontext für Sehbehinderung oder blinde Benutzer bereitzustellen, wird aber auch für die Kontextsuche oder andere Anwendungen verwendet. Diese Eigenschaft kann Benutzern helfen, ein Symbol oder die allgemeine visuelle Darstellung zu verstehen.

Die **Description-Eigenschaft** wird durch Aufrufen von [**IAccessible::get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)abgerufen.

## <a name="when-to-support-the-description-property"></a>Wann sollte die Description-Eigenschaft unterstützt werden?

Server unterstützen die **Description-Eigenschaft,** wenn die Beschreibung nicht offensichtlich ist oder wenn sie basierend auf den Eigenschaften [**Name,**](name-property.md) [**Rolle,**](role-property.md) [**Status**](state-property.md)und [**Wert**](value-property.md) des Objekts nicht redundant ist. Beispielsweise würde eine Schaltfläche mit der Bezeichnung "OK" keine zusätzlichen Informationen benötigen, während eine Schaltfläche, die ein Bild eines Kaktus zeigt, keine zusätzlichen Informationen benötigt. Die Eigenschaften **Name,** **Rolle** und [**Hilfe**](help-property.md) für eine solche Schaltfläche beschreiben ihren Zweck, aber die **Description-Eigenschaft** übermittelt Weniger greifbare Informationen. Beispiel: "Diese Schaltfläche zeigt ein Bild eines Kaktus."

Ein Microsoft Active Accessibility Server kann Unterstützung für Benutzeroberflächenautomatisierung hinzufügen, indem [er die direkte Anmerkung](direct-annotation.md)verwendet, die [**IAccessibleEx-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) verwendet oder Microsoft Active Accessibility implementiert und Benutzeroberflächenautomatisierung gleichzeitig mit beiden Implementierungen implementiert, die die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der direkten Anmerkung](using-direct-annotation.md)
</dt> <dt>

[IAccessibleEx-Schnittstelle](iaccessibleex.md)
</dt> </dl>

 

 




