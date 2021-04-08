---
title: Richtlinien für die Bindung an das Schema
description: Es gibt zwei Möglichkeiten, eine Bindung an das Active Directory Schema herzustellen, das direkt an den Schema Container oder an ein classSchema-oder attributeSchema-Objekt im Schema Container gebunden ist.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Richtlinien für die Bindung an das Schema-AD
- Schema-AD, binden an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf246a4ea1ded5c7d80c52abb8ac9192182b3b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858145"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Richtlinien für die Bindung an das Schema

Es gibt zwei Möglichkeiten, eine Bindung an das Active Directory-Schema herzustellen:

-   Direkt an den Schema Container oder an ein **classSchema** -oder **attributeSchema** -Objekt im Schema Container binden. Das **classSchema** -Objekt oder das **attributeSchema** -Objekt enthält die kompletten, formalen Definitionen aller Klassen und Attribute, die in einer Active Directory-Domäne Gesamtstruktur vorhanden sein können. Weitere Informationen finden Sie unter [Lesen von attributeSchema-und classSchema-Objekten](reading-attributeschema-and-classschema-objects.md).
-   Binden an das abstrakte Schema oder an einen Klassen-oder Attribut Eintrag im abstrakten Schema. Das abstrakte Schema enthält nur eine Teilmenge der Daten zu den einzelnen Klassen und Attributen, die Daten sind jedoch in einem Format, das leicht abzurufen und zu verwenden ist. Weitere Informationen finden Sie [unter das abstrakte Schema](the-abstract-schema.md) und [Lesen des abstrakten Schemas](reading-the-abstract-schema.md).

Binden Sie das Schema direkt an den Schema Container, um das Schema zu ändern oder zu erweitern. Um die Klassen-und Attribut Definitionen zu lesen, ist es in der Regel einfacher, aus dem abstrakten Schema zu lesen.

Aus den folgenden Gründen ist es einfacher, aus dem abstrakten Schema zu lesen:

-   ADSI bietet spezielle Bindungs Techniken und eine Reihe von Schnittstellen zum Lesen des abstrakten Schemas.
-   Die ADSI-Schnittstellen, die mit dem abstrakten Schema arbeiten, geben Daten in einem für andere ADSI-Schnittstellen geeigneten Format zurück. [**Iadsclass**](/windows/desktop/api/iads/nn-iads-iadsclass) und [**iadsproperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) verwenden z. b. normalerweise **ldapDisplayName** -Zeichen folgen, um Attribut-und Klassennamen zu melden, auch wenn diese Daten im Verzeichnis in Form von Objekt bezeichnerdateien (OIDs) gespeichert sind. Das **ldapDisplayName** -Format ist praktisch, da andere ADSI-Schnittstellen es verwenden, um auf Klassen und Attribute in Suchfiltern und an anderer Stelle zu verweisen.
-   Der abstrakte Schema Eintrag für eine Objektklasse enthält Daten, die aus mehreren **classSchema** -Objekten gesammelt wurden. Mögliche übergeordnete Elemente, obligatorische Attribute und optionale Attribute für eine Objektklasse sind z. b. die Vereinigung dieser Attribute aus den Element-und Hilfsklassen der Klasse. Wenn Sie aus dem eigentlichen Schema Container gelesen haben, müssen Sie Daten aus den verschiedenen **classSchema** -Objekten sammeln, von denen die Klasse abgeleitet wurde. Wenn Sie aus dem abstrakten Schema lesen, befinden sich die Daten an einem Ort.

In den folgenden Fällen sollten Sie direkt an den Schema Container binden, anstatt das abstrakte Schema zu verwenden:

-   Um bestimmte Attribute zu erhalten, die nicht im abstrakten Schema verfügbar gemacht werden. Beispielsweise werden **oMSyntax**, **attributeSchema**, **defaultSecurityDescriptor** und andere Attribute nicht im abstrakten Schema verfügbar gemacht.
-   Zum Abfragen von **attributeSchema** -und **classSchema** -Objekten. Um nach Klassen oder Attributen zu suchen, die einem angegebenen Filter entsprechen, binden Sie an den Schema Container, und führen Sie eine Suche auf einer einzelnen Ebene durch.
-   Zum Hinzufügen oder Ändern von Attributen oder Klassen. Das abstrakte Schema ist schreibgeschützt. Sie können Sie nicht verwenden, um das Schema zu ändern oder zu erweitern. Beachten Sie, dass auf dem Domänen Controller, der der Schema Master ist, Änderungen vorgenommen werden müssen. Weitere Informationen finden Sie unter [Voraussetzungen für das Installieren einer Schema Erweiterung](prerequisites-for-installing-a-schema-extension.md).

 

 