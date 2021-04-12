---
title: Verknüpfte Attribute (AD DS)
description: Verknüpfte Attribute sind Paare von Attributen, in denen das System die Werte eines Attributs (der Rücklink) basierend auf den Werten berechnet, die für das andere Attribut in der Gesamtstruktur festgelegt sind.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- Verknüpfte Attribute ad
- Attribute ad, verknüpft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0e3f6706c797497fb1bb25ea82805385f9897e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104390123"
---
# <a name="linked-attributes-ad-ds"></a>Verknüpfte Attribute (AD DS)

Verknüpfte Attribute sind Paare von Attributen, in denen das System die Werte eines Attributs (der Rücklink) basierend auf den Werten berechnet, die für das andere Attribut in der Gesamtstruktur festgelegt sind. Ein backlinkwert für eine beliebige Objektinstanz besteht aus dem DNS aller Objekte, für die der DN des Objekts im entsprechenden Forward-Link festgelegt ist. "Manager" und "Reports" sind z. b. ein Paar verknüpfter Attribute, wobei "Manager" der Forward-Link und "Reports" der Rücklink ist. Nehmen wir nun an, dass Bill Joe der Manager ist. Wenn Sie den DN des Benutzer Objekts der Rechnung im "Manager"-Attribut des Benutzer Objekts von Joe speichern, wird der DN des Benutzer Objekts von Joe im "Reports"-Attribut des Benutzer Objekts der Rechnung angezeigt.

Ein Forward-Link-/backlinkpaar wird durch die [**linkid**](/windows/desktop/ADSchema/a-linkid) -Werte von zwei [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Definitionen identifiziert. Das **linkid** der vorwärts Verknüpfung ist ein gerade, positiver Wert ungleich 0 (null), und das **linkid** der zugeordneten backverknüpfung ist das Forward- **linkid** plus eins. Beispielsweise ist das **linkid** für "Manager" 42, und das **linkid** für "Reports" ist 43.

Im folgenden finden Sie eine Liste der Richtlinien zum Definieren eines neuen Paars verknüpfter Attribute:

-   Die [**linkid**](/windows/desktop/ADSchema/a-linkid) -Werte müssen bei allen [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekten eindeutig sein. Um Konflikte zu vermeiden, sollten Sie den **linkid** automatisch generieren, indem Sie die Anweisungen im Thema Abrufen [einer Link-ID](obtaining-a-link-id.md)befolgen.
-   Ein Backlink muss über einen entsprechenden vorwärts Link verfügen, d. h., der Forward-Link muss vorhanden sein, bevor ein entsprechendes Backlinkattribut erstellt werden kann.
-   Ein Backlink ist immer ein mehr wertiges Attribut. Ein vorwärts Link kann einwertig oder mehr wertig sein. Verwenden Sie einen mehrwertigen Forward-Link, wenn eine m:n-Beziehung besteht.
-   Der [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Wert eines vorwärts Links muss 2.5.5.1, 2.5.5.7 oder 2.5.5.14 sein. Diese Werte entsprechen Syntaxen, die einen Distinguished Name enthalten, wie z. b. die [**Objekt Syntax (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   Der [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Wert eines Backlinks muss 2.5.5.1 lauten, d. h. die [**Objekt Syntax (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   Gemäß der Konvention werden backlinkattribute dem Wert " [**mayare**](/windows/desktop/ADSchema/a-maycontain) " der [**obersten**](/windows/desktop/ADSchema/c-top) abstrakten Klasse hinzugefügt. Dadurch kann das Attribut für die Rück Verknüpfung aus Objekten jeder Klasse gelesen werden, da Sie nicht tatsächlich mit dem Objekt gespeichert werden, sondern basierend auf den Forward-Link Werten berechnet werden.

 

 