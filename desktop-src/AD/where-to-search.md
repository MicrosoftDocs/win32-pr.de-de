---
title: Entscheidung, wo gesucht werden soll
description: In diesem Thema werden die verschiedenen Suchvorgänge erläutert, die in der Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Entscheidung, wo AD durchsucht werden soll
- Active Directory AD , Suchen, Entscheidung, wo gesucht werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6984a79bb761c1926b6735a91209c9f387ac45619ffc752daef253a74f5e587a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024318"
---
# <a name="deciding-where-to-search"></a>Entscheidung, wo gesucht werden soll

In diesem Thema werden die verschiedenen Suchvorgänge erläutert, die in der Active Directory Domain Services.

Alle Suchvorgänge werden in einem der folgenden Namenskontexte ausgeführt:

-   Domäne, einschließlich Anwendungsverzeichnispartitionen
-   Schemacontainer
-   Konfigurationscontainer
-   Globaler Katalog

## <a name="searching-a-domain"></a>Durchsuchen einer Domäne

Domänen enthalten die meisten der häufig verwendeten Objekte wie Benutzer, Kontakte, Gruppen, Organisationseinheiten, Computer und so weiter. Die meisten Abfragen durchsuchen eine Domäne. Weitere Informationen zum Durchsuchen einer Domäne finden Sie unter [Suchen von Domäneninhalten.](searching-domain-contents.md)

## <a name="searching-the-schema-container"></a>Durchsuchen des Schemacontainers

Der Schemacontainer enthält die [**Objekte classSchema**](/windows/desktop/ADSchema/c-classschema) und [**attributeSchema,**](/windows/desktop/ADSchema/c-attributeschema) die die formale Definition jeder Klasse und jedes Attributs bereitstellen, die in einem Active Directory Domain Services. Um nach Objekten im Schemacontainer zu suchen, binden Sie an den Schemacontainer auf einem beliebigen Domänencontroller. Der Schemacontainer ist auf allen Domänencontrollern verfügbar. Der Distinguished Name des Schemacontainers wird aus dem **schemaNamingContext-Attribut** von rootDSE ermittelt. Weitere Informationen zu rootDSE und dem **schemaNamingContext-Attribut** finden Sie unter [Serverlose Bindung und RootDSE](serverless-binding-and-rootdse.md).

Weitere Informationen zum Lesen aus dem Schema oder dem abstrakten Schemacontainer finden Sie unter [Richtlinien für die Bindung an das Schema.](guidelines-for-binding-to-the-schema.md)

## <a name="searching-the-configuration-container"></a>Durchsuchen des Konfigurationscontainers

Der Konfigurationscontainer enthält Konfigurationsinformationen wie Standorte, Dienste und Anzeigespezifizierer für die gesamte Gesamtstruktur. Um nach Objekten im Konfigurationscontainer zu suchen, binden Sie an den Konfigurationscontainer auf einem beliebigen Domänencontroller. Der Konfigurationscontainer ist auf allen Domänencontrollern verfügbar. Der Distinguished Name des Konfigurationscontainers wird aus dem **configurationNamingContext-Attribut** von rootDSE ermittelt. Weitere Informationen zu rootDSE und dem **configurationNamingContext-Attribut** finden Sie unter [Serverlose Bindung und RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Durchsuchen des globalen Katalogs

Der globale Katalog enthält ein Replikat jedes Objekts in Active Directory Domain Services, jedoch nur mit einer kleinen Anzahl von Attributen. Die Attribute im globalen Katalog werden am häufigsten in Suchvorgängen verwendet, z. B. vor- und nachname eines Benutzers, Anmeldenamen und so weiter. Weitere Informationen zum Durchsuchen des globalen Katalogs finden Sie unter [Suchen des globalen Katalogs.](searching-global-catalog-contents.md)

 

 