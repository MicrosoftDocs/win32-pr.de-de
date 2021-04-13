---
description: In Windows Vista und höher wurden Metadaten als Methode zum Organisieren von Elementen, z. b. Dateien, e-Mails oder Kontakten, als zentrales Element.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementieren von Eigenschaften Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcef615ce1ebb5041d79dd9c6ccf8cf129d189aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217017"
---
# <a name="implementing-property-handlers"></a>Implementieren von Eigenschaften Handlern

In Windows Vista und höher wurden Metadaten als Methode zum Organisieren von Elementen, z. b. Dateien, e-Mails oder Kontakten, als zentrales Element. Um ein System zu aktivieren, in dem Elemente basierend auf Ihren Metadaten durchsucht werden können und Benutzer diese Metadaten lesen oder schreiben können, wurde in Windows Vista ein neues Eigenschaften System eingeführt. Metadaten in diesem System werden durch einen erweiterbaren Satz von Eigenschaften dargestellt. In diesen Themen wird beschrieben, wie Sie einen Handler zum Lesen und Schreiben von Eigenschaften in einen und aus einem Dateistream erstellen können. Diese Handler werden als Eigenschaften Handler bezeichnet und jeweils einem angegebenen Dateitypen zugeordnet, die durch die Dateinamenerweiterung identifiziert werden.

In den folgenden Themen werden die Anforderungen und Strategien erläutert, die beim Definieren von Eigenschaften und Eigenschaften Handlern beteiligt sind.

-   [Grundlegendes zu Eigenschaften Handlern](./building-property-handlers-properties.md)
-   [Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
-   [Verwenden von Eigenschaften Listen](./building-property-handlers-property-lists.md)
-   [Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md)
-   [Registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md)
-   [Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern](./prophand-bestprac-faq.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von benutzerdefinierten Eigenschaften](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Eigenschafts Beschreibungs Schema](./propdesc-schema-entry.md)
</dt> </dl>

 

 
