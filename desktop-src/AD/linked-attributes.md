---
title: Verknüpfte Attribute (AD DS)
description: Verknüpfte Attribute sind Attributpaare, in denen das System die Werte eines Attributs (des Backlinks) basierend auf den Werten berechnet, die für das andere Attribut (den Vorwärtslink) in der gesamtstruktur festgelegt sind.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- Verknüpfte Attribute AD
- Attribute AD , verknüpft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2167169d6a9d2f8eabe69323054767ae66823d8e1fe954a232ed63fd31a9b845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186993"
---
# <a name="linked-attributes-ad-ds"></a>Verknüpfte Attribute (AD DS)

Verknüpfte Attribute sind Attributpaare, in denen das System die Werte eines Attributs (des Backlinks) basierend auf den Werten berechnet, die für das andere Attribut (den Vorwärtslink) in der gesamtstruktur festgelegt sind. Ein Backlinkwert für jede Objektinstanz besteht aus den DNs aller Objekte, für die der DN des Objekts im entsprechenden Vorwärtslink festgelegt ist. Beispielsweise sind "Manager" und "Berichte" ein Paar verknüpfter Attribute, wobei "Manager" der Vorwärtslink und "Berichte" der Rücklink ist. Angenommen, Bill ist Joes Manager. Wenn Sie den DN des Benutzerobjekts von Bill im Attribut "Manager" des Benutzerobjekts von Joe speichern, wird der DN des Benutzerobjekts von Joe im Attribut "Reports" des Benutzerobjekts von Bill angezeigt.

Ein ForwardLink/Back-Link-Paar wird durch die [**linkID-Werte**](/windows/desktop/ADSchema/a-linkid) von zwei [**attributeSchema-Definitionen**](/windows/desktop/ADSchema/c-attributeschema) identifiziert. Die **linkID des** Vorwärtslinks ist ein gleichmäßiger, positiver Wert ungleich null, und die **linkID** des zugeordneten Backlinks ist die Forward **linkID** plus one. Beispielsweise ist die **linkID** für "Manager" 42 und die **linkID** für "Reports" 43.

Im Folgenden finden Sie eine Liste mit Richtlinien zum Definieren eines neuen Paars verknüpfter Attribute:

-   Die [**linkID-Werte**](/windows/desktop/ADSchema/a-linkid) müssen für alle [**attributeSchema-Objekte eindeutig**](/windows/desktop/ADSchema/c-attributeschema) sein. Um Konflikte zu vermeiden, sollten Sie die **linkID** automatisch generieren, indem Sie die Anweisungen im Thema [Abrufen einer Link-ID befolgen.](obtaining-a-link-id.md)
-   Ein Backlink muss über einen entsprechenden Vorwärtslink verfügen, d.&a0;b. der Forward-Link muss vorhanden sein, bevor ein entsprechendes Backlinkattribut erstellt werden kann.
-   Ein Backlink ist immer ein mehrwertiges Attribut. Ein Vorwärtslink kann einwertige oder mehrwertige Verknüpfungen sein. Verwenden Sie einen mehrwertigen Vorwärtslink, wenn eine n:n-Beziehung besteht.
-   Der [**attributSchema-Wert**](/windows/desktop/ADSchema/c-attributeschema) eines Forward-Links muss 2.5.5.1, 2.5.5.7 oder 2.5.5.14 sein. Diese Werte entsprechen Syntaxen, die einen Distinguished Name enthalten, z. B. die [**Object(DS-DN)-Syntax.**](/windows/desktop/ADSchema/s-object-ds-dn)
-   Der [**attributeSchema-Wert**](/windows/desktop/ADSchema/c-attributeschema) eines Backlinks muss 2.5.5.1 sein. Dies ist die [**Object(DS-DN)-Syntax.**](/windows/desktop/ADSchema/s-object-ds-dn)
-   Standardmäßig werden Backlinkattribute dem [**mayContain-Wert**](/windows/desktop/ADSchema/a-maycontain) der obersten [**abstrakten Klasse**](/windows/desktop/ADSchema/c-top) hinzugefügt. Dadurch kann das Backlinkattribut aus Objekten einer beliebigen Klasse gelesen werden, da sie nicht tatsächlich mit dem -Objekt gespeichert, sondern basierend auf den Vorwärtslinkwerten berechnet werden.

 

 