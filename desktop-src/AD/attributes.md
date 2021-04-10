---
title: Attribute (AD DS)
description: Jedes-Objekt in Active Directory Domain Services enthält einen Satz von Attributen, die die Eigenschaften des-Objekts definieren.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- Attribute ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038804"
---
# <a name="attributes-ad-ds"></a>Attribute (AD DS)

Jedes-Objekt in Active Directory Domain Services enthält einen Satz von Attributen, die die Eigenschaften des-Objekts definieren. Jedes Attribut wird von einem [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekt im Schema Container beschrieben, das das Attribut definiert. Die Attribut Definition enthält eine Vielzahl von Daten, z. b. die Objekttypen, auf die das Attribut angewendet wird, und den Syntax Typ des Attributs. Weitere Informationen zu Attribut Schema Definitionen finden Sie unter [Merkmale von Attributen](characteristics-of-attributes.md).

In der folgenden Liste sind die Typen der Attribute aufgeführt, die in Active Directory Domain Services gespeichert werden.

<dl> <dt>

<span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Domänen replizierte, gespeicherte Attribute
</dt> <dd>

Einige Attribute werden im Verzeichnis (z. b. " [**CN**](/windows/desktop/ADSchema/a-cn)", " [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)" und " [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)") gespeichert und auf allen Domänen Controllern in einer Domäne repliziert. Eine Teilmenge dieser Attribute wird auch in den globalen Katalog repliziert. Wenn Sie Attribute eines Objekts aus dem globalen Katalog auflisten, werden nur die in den globalen Katalog replizierten Attribute zurückgegeben. Einige Attribute werden ebenfalls indiziert, da durch das Einschließen einer indizierten Eigenschaft in eine Abfrage die Abfrageleistung verbessert wird.

</dd> <dt>

<span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Nicht replizierte lokal gespeicherte Attribute
</dt> <dd>

Nicht replizierte Attribute, wie z. b. [**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**Last-Logon**](/windows/desktop/ADSchema/a-lastlogon)und [**Last-**](/windows/desktop/ADSchema/a-lastlogoff) abmelden, werden auf den einzelnen Domänen Controllern gespeichert, aber nicht repliziert. Die nicht replizierten Attribute sind Attribute, die einen bestimmten Domänen Controller betreffen. Das Attribut für die **Letzte Anmeldung** ist beispielsweise das letzte Datum und die Uhrzeit, zu der die Netzwerk Anmeldung des Benutzers von diesem bestimmten Domänen Controller überprüft wurde, der die Eigenschaft zurückgegeben hat. Diese Attribute können auf die gleiche Weise wie die zuvor beschriebenen Domänen weiten Attribute abgerufen werden. Allerdings speichert jeder Domänen Controller für diese Attribute nur die Werte, die diesen bestimmten Domänen Controller betreffen. Um z. b. den Zeitpunkt der letzten Anmeldung eines Benutzers bei der Domäne abzurufen, rufen Sie das Attribut der **letzten Anmeldung** für den Benutzer von allen Domänen Controllern in der Domäne ab und suchen Sie nach dem aktuellen Datum und der aktuellen Uhrzeit.

</dd> <dt>

<span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Nicht gespeicherte, konstruierte Attribute
</dt> <dd>

Ein Benutzerobjekt verfügt auch über konstruierte Attribute, die nicht im Verzeichnis gespeichert werden, sondern vom Domänen Controller berechnet werden, wie z. b. [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname) und [**zuordnungsdattributes**](/windows/desktop/ADSchema/a-allowedattributes).

</dd> </dl>

 

 