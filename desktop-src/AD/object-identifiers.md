---
title: Objektbezeichner (AD DS)
description: Objektbezeichner (Object Identifiers, OIDs) sind eindeutige numerische Werte, die von verschiedenen ausstellenden Stellen ausgegeben werden, um Datenelemente, Syntaxen und andere Teile verteilter Anwendungen eindeutig zu identifizieren.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- Objektbezeichner AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af458a003c5a5a8586c32449674019fb6b241d52c4300e107898d91c75047214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185511"
---
# <a name="object-identifiers-ad-ds"></a>Objektbezeichner (AD DS)

Objektbezeichner (Object Identifiers, OIDs) sind eindeutige numerische Werte, die von verschiedenen ausstellenden Stellen ausgegeben werden, um Datenelemente, Syntaxen und andere Teile verteilter Anwendungen eindeutig zu identifizieren. OIDs befinden sich in OSI-Anwendungen, X.500-Verzeichnissen, SNMP und anderen Anwendungen, bei denen Eindeutigkeit wichtig ist. OIDs basieren auf einer Struktur, in der eine übergeordnete Ausstellende Stelle, z. B. die ISO, einen Branch der Struktur einer Unterautorität zuordt, die wiederum Unterbranches zuordnen kann.

Das LDAP-Protokoll (RFC 2251) erfordert einen Verzeichnisdienst, um Objektklassen, Attribute und Syntaxen mit OIDs zu identifizieren. Dies ist Teil des LDAP X.500-Legacy.

OIDs in Active Directory Domain Services enthalten einige, die von der ISO für X.500-Klassen und -Attribute ausgestellt wurden, und einige von Microsoft und anderen ausstellenden Stellen. Die OID-Notation ist eine gepunktete Zahlenzeichenfolge, z.B. "1.2.840.113556.1.5.9", die in der folgenden Tabelle beschrieben wird.



| Wert  | Bedeutung          | Beschreibung                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifiziert die Stammzertifizierungsstelle.                           |
| 2      | ANSI             | Durch ISO zugewiesene Gruppenbezeichnung.                       |
| 840    | USA              | Von der Gruppe zugewiesene Länder-/Regionbezeichnung.        |
| 113556 | Microsoft        | Organisationsbezeichnung, die durch das Land bzw. die Region zugewiesen ist. |
| 1      | Active Directory | Wird von der Organisation zugewiesen.                            |
| 5      | Klassen          | Wird von der Organisation zugewiesen.                            |
| 9      | **user-Klasse**   | Wird von der Organisation zugewiesen.                            |



 

Weitere Informationen und eine Erörterung von zwei Verfahren zum Abrufen gültiger OIDs für die Erweiterung des Active Directory-Schemas finden Sie unter [Abrufen eines Objektbezeichners.](obtaining-an-object-identifier.md)

 

 




