---
description: Erfahren Sie, wie Sie einen Eigenschaftenhandler erstellen, der Eigenschaften in einen und aus einem Dateistream liest und schreibt. Jeder Handler ist einem bestimmten Dateityp zugeordnet.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implementieren von Eigenschaftenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf37ae37e43ce14cf69bec44e7f210b32373d38e
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989265"
---
# <a name="implementing-property-handlers"></a>Implementieren von Eigenschaftenhandlern

In Windows Vista und höher wurden Metadaten als Methode zum Organisieren von Elementen wie Dateien, E-Mails oder Kontakten zentral. Um ein System zu aktivieren, in dem Elemente basierend auf ihren Metadaten durchsucht werden können und in dem Benutzer diese Metadaten lesen oder schreiben können, hat Windows Vista ein neues Eigenschaftensystem eingeführt. Metadaten in diesem System werden durch einen erweiterbaren Satz von Eigenschaften dargestellt. In diesem Satz von Themen wird beschrieben, wie Sie einen Handler erstellen können, der Eigenschaften in einen und aus einem Dateistream liest und schreibt. Diese Handler werden als Eigenschaftenhandler bezeichnet und sind jeweils einem bestimmten Dateityp zugeordnet, der durch die Dateinamenerweiterung identifiziert wird.

In den folgenden Themen werden die Anforderungen und Strategien zum Definieren Ihrer Eigenschaften und Eigenschaftenhandler erörtert.

-   [Grundlegendes zu Eigenschaftenhandlern](./building-property-handlers-properties.md)
-   [Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
-   [Verwenden von Eigenschaftenlisten](./building-property-handlers-property-lists.md)
-   [Initialisieren von Eigenschaftenhandlern](./building-property-handlers-property-handlers.md)
-   [Registrieren und Verteilen von Eigenschaftenhandlern](./prophand-reg-dist.md)
-   [Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern](./prophand-bestprac-faq.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von benutzerdefinierten Eigenschaften](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Eigenschaftenbeschreibungsschema](./propdesc-schema-entry.md)
</dt> </dl>

 

 
