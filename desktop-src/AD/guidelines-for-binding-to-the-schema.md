---
title: Richtlinien für die Bindung an das Schema
description: Es gibt zwei Möglichkeiten, eine Bindung an das Active Directory-Schema Direkt an den Schemacontainer oder an ein classSchema- oder attributeSchema-Objekt im Schemacontainer zu binden.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Richtlinien für die Bindung an das Schema-AD
- Schema AD , Bindung an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1492814bbce4b359a16c10f1d92340ae06d0f3c58177cd125a0b0c861f32f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188684"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Richtlinien für die Bindung an das Schema

Es gibt zwei Möglichkeiten, eine Bindung an das Active Directory-Schema zu erstellen:

-   Direktes Binden an den Schemacontainer oder an ein **classSchema-** oder **attributeSchema-Objekt** im Schemacontainer. Die **classSchema-** oder **attributeSchema-Objekte** enthalten vollständige, formale Definitionen jeder Klasse und jedes Attributs, die in einer Active Directory-Domäne sein können. Weitere Informationen finden Sie unter [Lesen von attributeSchema und classSchema Objects](reading-attributeschema-and-classschema-objects.md).
-   Binden an das abstrakte Schema oder an einen Klassen- oder Attributeintrag im abstrakten Schema. Das abstrakte Schema enthält nur eine Teilmenge der Daten zu jeder Klasse und jedem Attribut, aber die Daten haben ein Format, das leicht abzurufen und zu verwenden ist. Weitere Informationen finden Sie unter [Das abstrakte Schema](the-abstract-schema.md) und Lesen des [abstrakten Schemas.](reading-the-abstract-schema.md)

Um das Schema zu ändern oder zu erweitern, binden Sie direkt an den Schemacontainer. Um die Klassen- und Attributdefinitionen zu lesen, ist es in der Regel einfacher, aus dem abstrakten Schema zu lesen.

Aus den folgenden Gründen ist es einfacher, aus dem abstrakten Schema zu lesen:

-   ADSI bietet spezielle Bindungstechniken und eine Reihe von Schnittstellen zum Lesen des abstrakten Schemas.
-   Die ADSI-Schnittstellen, die mit dem abstrakten Schema arbeiten, geben Daten in einem Format zurück, das für die Verwendung in anderen ADSI-Schnittstellen geeignet ist. Beispielsweise verwenden [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) und [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) in der Regel **lDAPDisplayName-Zeichenfolgen,** um Attribut- und Klassennamen zu melden, obwohl diese Daten im Verzeichnis in Form von Objektbezeichnern (OIDs) gespeichert werden. Das **Format lDAPDisplayName** ist praktisch, da es von anderen ADSI-Schnittstellen verwendet wird, um in Suchfiltern und an anderer Stelle auf Klassen und Attribute zu verweisen.
-   Der abstrakte Schemaeintrag für eine Objektklasse enthält Daten, die von mehreren **classSchema-Objekten gesammelt** wurden. Beispielsweise sind die möglichen übergeordneten Attribute, obligatorischen Attribute und optionalen Attribute für eine Objektklasse die Vereinigung dieser Attribute aus den Übergeordneten und Hilfsklassen der Klasse. Wenn Sie daten aus dem eigentlichen Schemacontainer lesen, müssen Sie Daten aus den verschiedenen **classSchema-Objekten** sammeln, von denen die Klasse abgeleitet wurde. Wenn Sie aus dem abstrakten Schema lesen, sind die Daten an einer Stelle gespeichert.

Sie sollten eine direkte Bindung an den Schemacontainer erstellen, anstatt in den folgenden Fällen das abstrakte Schema zu verwenden:

-   Um bestimmte Attribute zu erhalten, die nicht im abstrakten Schema verfügbar gemacht werden. **oMSyntax,** **attributeSchema,** **defaultSecurityDescriptor** und andere Attribute werden beispielsweise nicht im abstrakten Schema verfügbar gemacht.
-   So fragen Sie **attributeSchema-** und **classSchema-Objekte** ab. Um nach Klassen oder Attributen zu suchen, die mit einem angegebenen Filter übereinstimmen, binden Sie eine Bindung an den Schemacontainer, und führen Sie eine Suche auf einer Ebene aus.
-   So fügen Sie Attribute oder Klassen hinzu oder ändern sie. Das abstrakte Schema ist schreibgeschützt. Sie können es nicht verwenden, um das Schema zu ändern oder zu erweitern. Beachten Sie, dass Änderungen auf dem Domänencontroller vorgenommen werden müssen, der der Schemamaster ist. Weitere Informationen finden Sie unter [Voraussetzungen für die Installation einer Schemaerweiterung.](prerequisites-for-installing-a-schema-extension.md)

 

 