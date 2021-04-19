---
description: Erstellen einer Filter Eigenschaften Seite
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Erstellen einer Filter Eigenschaften Seite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346397"
---
# <a name="creating-a-filter-property-page"></a>Erstellen einer Filter Eigenschaften Seite

In diesem Abschnitt wird beschrieben, wie eine Eigenschaften Seite für einen benutzerdefinierten DirectShow-Filter mithilfe der [**cbasepropertypage**](cbasepropertypage.md) -Klasse erstellt wird. Der Beispielcode in diesem Abschnitt zeigt alle Schritte, die erforderlich sind, um eine Eigenschaften Seite zu erstellen. Das Beispiel zeigt eine Eigenschaften Seite für einen hypothetischen Videoeffekt Filter, der eine Sättigung-Eigenschaft unterstützt. Die Eigenschaften Seite verfügt über einen Schieberegler, den der Benutzer verschieben kann, um den Sättigungsgrad des Filters anzupassen.

Dieser Abschnitt enthält die folgenden Themen:

-   [Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Schritt 2: Implementieren von ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [Schritt 3. QueryInterface-Unterstützung](step-3--support-queryinterface.md)
-   [Schritt 4: Erstellen der Eigenschaften Seite](step-4--create-the-property-page.md)
-   [Schritt 5: Speichern eines Zeigers auf den Filter](step-5--store-a-pointer-to-the-filter.md)
-   [Schritt 6: Initialisieren des Dialog Felds](step-6--initialize-the-dialog.md)
-   [Schritt 7: Fenster Meldungen behandeln](step-7--handle-window-messages.md)
-   [Schritt 8. Anwenden von Eigenschafts Änderungen](step-8--apply-property-changes.md)
-   [Schritt 9: Trennen der Eigenschaften Seite](step-9--disconnect-the-property-page.md)
-   [Schritt 10. COM-Registrierung unterstützen](step-10--support-com-registration.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



