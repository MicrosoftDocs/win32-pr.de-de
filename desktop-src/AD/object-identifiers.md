---
title: Objekt Bezeichner (AD DS)
description: Objekt-IDs (OIDs) sind eindeutige numerische Werte, die von verschiedenen ausstellenden Behörden ausgegeben werden, um Datenelemente, Syntaxen und andere Teile verteilter Anwendungen eindeutig zu identifizieren.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- Objekt Bezeichner AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "106339036"
---
# <a name="object-identifiers-ad-ds"></a>Objekt Bezeichner (AD DS)

Objekt-IDs (OIDs) sind eindeutige numerische Werte, die von verschiedenen ausstellenden Behörden ausgegeben werden, um Datenelemente, Syntaxen und andere Teile verteilter Anwendungen eindeutig zu identifizieren. OIDs finden Sie in OSI-Anwendungen, X. 500-Verzeichnissen, SNMP und anderen Anwendungen, in denen die Eindeutigkeit wichtig ist. OIDs basieren auf einer Baumstruktur, in der eine übergeordnete ausstellende Zertifizierungsstelle, wie z. b. das ISO, eine Verzweigung der Struktur einer untergeordneten Zertifizierungsstelle zuordnet, die wiederum untergeordnete branches zuordnen kann.

Das LDAP-Protokoll (RFC 2251) erfordert einen Verzeichnisdienst, um Objektklassen, Attribute und Syntaxen mit OIDs zu identifizieren. Dies ist Teil der LDAP X. 500-Legacy-Version.

OIDs in Active Directory Domain Services enthalten einige von der ISO-Ausgabe für X. 500-Klassen und-Attribute sowie einige von Microsoft und anderen ausstellenden Behörden ausgestellten. Die OID-Notation ist eine gepunktete Zeichenfolge von Zahlen, z. b. "1.2.840.113556.1.5.9", die in der folgenden Tabelle beschrieben wird.



| Wert  | Bedeutung          | BESCHREIBUNG                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifiziert die Stamm Zertifizierungsstelle.                           |
| 2      | ANSI             | Von ISO zugewiesene Gruppen Bezeichnung.                       |
| 840    | USA              | Die von der Gruppe zugewiesene Bezeichnung für Land/Region.        |
| 113556 | Microsoft        | Organisations Bezeichnung, die vom Land/der Region zugewiesen wird. |
| 1      | Active Directory | Wird von der Organisation zugewiesen.                            |
| 5      | Klassen          | Wird von der Organisation zugewiesen.                            |
| 9      | **Benutzer** Klasse   | Wird von der Organisation zugewiesen.                            |



 

Weitere Informationen und eine Erörterung zweier Prozeduren, mit denen gültige OIDs zum Erweitern des Active Directory Schemas abgerufen werden, finden Sie unter Abrufen [eines Objekt Bezeichners](obtaining-an-object-identifier.md).

 

 




