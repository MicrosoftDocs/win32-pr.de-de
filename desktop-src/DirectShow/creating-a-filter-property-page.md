---
description: Erstellen einer Filtereigenschaftenseite
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Erstellen einer Filtereigenschaftenseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d891c42a6cdb2f1c636278a8270fb13a69580697a31fe78f2f3687246f20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108260"
---
# <a name="creating-a-filter-property-page"></a>Erstellen einer Filtereigenschaftenseite

In diesem Abschnitt wird beschrieben, wie Sie mithilfe der [**CBasePropertyPage-Klasse**](cbasepropertypage.md) eine Eigenschaftenseite für einen benutzerdefinierten DirectShow-Filter erstellen. Der Beispielcode in diesem Abschnitt zeigt alle Schritte, die zum Erstellen einer Eigenschaftenseite erforderlich sind. Das Beispiel zeigt eine Eigenschaftenseite für einen hypothetischen Videoeffektfilter, der eine Sättigungseigenschaft unterstützt. Die Eigenschaftenseite verfügt über einen Schieberegler, den der Benutzer verschieben kann, um den Sättigungsgrad des Filters anzupassen.

Dieser Abschnitt enthält die folgenden Themen:

-   [Schritt 1: Definieren eines Mechanismus zum Festlegen der Eigenschaft](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Schritt 2: Implementieren von ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [Schritt 3: Unterstützung von QueryInterface](step-3--support-queryinterface.md)
-   [Schritt 4: Erstellen der Eigenschaftenseite](step-4--create-the-property-page.md)
-   [Schritt 5: Store eines Zeigers auf den Filter](step-5--store-a-pointer-to-the-filter.md)
-   [Schritt 6: Initialisieren des Dialogfelds](step-6--initialize-the-dialog.md)
-   [Schritt 7: Verarbeiten von Fenstermeldungen](step-7--handle-window-messages.md)
-   [Schritt 8: Anwenden von Eigenschaftenänderungen](step-8--apply-property-changes.md)
-   [Schritt 9: Trennen der Eigenschaftenseite](step-9--disconnect-the-property-page.md)
-   [Schritt 10: Unterstützung der COM-Registrierung](step-10--support-com-registration.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



