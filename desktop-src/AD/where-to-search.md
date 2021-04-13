---
title: Bestimmen des Orts für die Suche
description: In diesem Thema werden die verschiedenen Suchvorgänge erläutert, die in Active Directory Domain Services ausgeführt werden können.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Auswählen des Orts für die Suche in AD
- Active Directory AD, suchen und entscheiden, wo gesucht werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314595"
---
# <a name="deciding-where-to-search"></a>Bestimmen des Orts für die Suche

In diesem Thema werden die verschiedenen Suchvorgänge erläutert, die in Active Directory Domain Services ausgeführt werden können.

Alle Suchvorgänge werden in einem der folgenden Namenskontexte ausgeführt:

-   Domäne, einschließlich Anwendungsverzeichnis Partitionen
-   Schema Container
-   Konfigurations Container
-   Globaler Katalog

## <a name="searching-a-domain"></a>Suchen einer Domäne

Domänen enthalten die meisten der stark verwendeten Objekte, wie z. b. Benutzer, Kontakte, Gruppen, Organisationseinheiten, Computer usw. Bei den meisten Abfragen wird eine Domäne durchsucht. Weitere Informationen zum Durchsuchen von Domänen Inhalten finden Sie unter durch [Suchen von Domänen Inhalten](searching-domain-contents.md).

## <a name="searching-the-schema-container"></a>Durchsuchen des Schema Containers

Der Schema Container enthält die [**classSchema**](/windows/desktop/ADSchema/c-classschema) -und [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekte, die die formale Definition aller Klassen und Attribute bereitstellen, die in Active Directory Domain Services vorhanden sein können. Um im Schema Container nach Objekten zu suchen, binden Sie an einen beliebigen Domänen Controller an den Schema Container. Der Schema Container ist auf allen Domänen Controllern verfügbar. Der Distinguished Name des Schema Containers wird aus dem **schemaNamingContext** -Attribut von RootDSE abgerufen. Weitere Informationen zu RootDSE und zum **schemaNamingContext** -Attribut finden Sie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md).

Weitere Informationen zum Lesen aus dem Schema oder dem abstrakten Schema Container finden [Sie unter Richtlinien für die Bindung an das Schema](guidelines-for-binding-to-the-schema.md).

## <a name="searching-the-configuration-container"></a>Durchsuchen des Konfigurations Containers

Der Konfigurations Container enthält Konfigurationsinformationen, z. b. Standorte, Dienste und Anzeige spezifiken, für die gesamte Gesamtstruktur. Um im Konfigurations Container nach Objekten zu suchen, binden Sie an den Konfigurations Container auf einem beliebigen Domänen Controller. Der Konfigurations Container ist auf allen Domänen Controllern verfügbar. Der Distinguished Name des Konfigurations Containers wird aus dem **configurationNamingContext** -Attribut von RootDSE abgerufen. Weitere Informationen zu RootDSE und zum **configurationNamingContext** -Attribut finden Sie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Durchsuchen des globalen Katalogs

Der globale Katalog enthält ein Replikat aller Objekte in Active Directory Domain Services, aber nur mit einer kleinen Anzahl von Attributen. Bei Such Vorgängen werden die Attribute im globalen Katalog häufig verwendet, z. b. die vor-und Nachnamen eines Benutzers, Anmelde Namen usw. Weitere Informationen zum Durchsuchen des globalen Katalogs finden Sie unter durch [Suchen des globalen Katalogs](searching-global-catalog-contents.md).

 

 