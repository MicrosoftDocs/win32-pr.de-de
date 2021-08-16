---
description: In diesem Thema werden einige Bausteinszenarien vorgestellt, in denen die Kriterien veranschaulicht werden, die unter Entscheidung, wo Sicherheit erzwungen werden soll beschrieben werden.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c4bafb0334bb9e5f124eb184f6ebf2d17f4f0dc40ef04421162dc6604f531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308742"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen

In diesem Thema werden einige Bausteinszenarien vorgestellt, in denen die Kriterien veranschaulicht werden, die unter [Entscheidung, wo Sicherheit erzwungen werden soll](deciding-where-to-enforce-security.md)beschrieben werden.

## <a name="trusted-server-scenario"></a>Szenario für vertrauenswürdige Server

-   Die Datenbank vertraut der COM+-Anwendung vollständig, um Endbenutzer für den Zugriff auf Daten in der Datenbank zu authentifizieren und zu autorisieren.
-   Vorzugsweise ist die Datenbank gegen jeglichen Zugriff mit Ausnahme der Anwendung geschützt.
-   Die COM+-Anwendung verwendet rollenbasierte Sicherheit, um Benutzer zu autorisieren.
-   Verbindungen werden unter der Identität der COM+-Anwendung geöffnet und sind vollständig poolfähig.
-   Die Überwachung und Protokollierung kann von der COM+-Anwendung durchgeführt werden, oder diese Informationen können von der Anwendung an die Datenbank übergeben werden.

Dieses Szenario funktioniert am besten für Daten, auf die von vorhersagbaren Kategorien von Benutzern zugegriffen werden kann, die in Rollen gekapselt werden können. Beispielsweise verfügen nur "Manager", "Kassierer" und "Schrifthalter" über die Berechtigung für den Zugriff auf Konten. Die Geschäftslogik der einzelnen Funktionen wird auf der mittleren Ebene erzwungen.

## <a name="impersonation-scenario"></a>Identitätswechselszenario

-   Die Datenbank führt eine eigene Authentifizierung und Autorisierung von Endbenutzern durch, um den Zugriff auf Daten in der Datenbank einzuschränken.
-   Die COM+-Anwendung nimmt bei jedem Zugriff auf die Datenbank die Identität von Clients an.
-   Verbindungen werden pro Aufruf hergestellt und können nicht wiederverwendet werden.

Dieses Szenario eignet sich am besten für Daten, die eng an sehr kleine Benutzerklassen gebunden sind. Beispielsweise kann jeder Mitarbeiter nur auf seine eigene Personaldatei zugreifen, und jeder Vorgesetzte kann nur auf die Personaldateien ihrer Berichte zugreifen.

## <a name="hybrid-scenario"></a>Hybridszenario

Eine Kombination der beiden vorherigen Szenarien, in denen der Identitätswechsel nur verwendet wird, wenn er benötigt wird.

Dieses Szenario funktioniert am besten in Situationen, in denen Sie über hybride Benutzerdatenbeziehungen verfügen. Sie verfügen z. B. über "Manager", "Banker", "Verwalter" und Tausende einzelner Webclients, die nur auf ihre eigenen Konten zugreifen können. Sie können Logikpfade durch die Anwendung , möglicherweise mit separaten Komponenten, trennen, um die letztere Benutzerklasse zu verarbeiten, insbesondere dann, wenn sich die Leistungsannahmen für diese Benutzer unterscheiden.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>Vertrauenswürdiges Szenario mit Microsoft SQL Server Rollen

-   Microsoft SQL Server 7.0 und höher kann den Zugriff auf bestimmte Zeilen mithilfe von Rollen autorisieren, vertraut jedoch der COM+-Anwendung, um Benutzer zu authentifizieren und zu autorisieren und sie den richtigen Rollen in der Datenbank zuzuordnen.
-   Die COM+-Anwendung autorisiert Benutzer mit rollenbasierter Sicherheit, und die Anwendungsrollen entsprechen gut den Datenbankrollen.
-   Verbindungen können geöffnet werden, die für eine bestimmte Datenbankrolle spezifisch sind. Diese Verbindungen können wiederverwendet werden, wenn sie von in einem Pool zusammengefassten Objekten in den COM+-Anwendungen gespeichert werden. Ausführliche Informationen hierzu finden Sie unter [COM+ Object Pooling](com--object-pooling.md).
-   Die Überwachung und Protokollierung kann von der COM+-Anwendung durchgeführt werden, oder diese Informationen können von der Anwendung an die Datenbank übergeben werden.

Dieses Szenario eignet sich am besten für die gleichen Arten von Benutzern und Daten wie im ersten Szenario mit vertrauenswürdigen Servern, da die COM+-Anwendung weiterhin weitgehend vertrauenswürdig ist, um die Autorisierung ordnungsgemäß zu verarbeiten. Sie trägt jedoch dazu bei, die Datenbank vor nicht autorisiertem Zugriff zu schützen und gleichzeitig den Zugriff von mehreren Quellen außerhalb der COM+-Anwendung zuzulassen, ohne dass dies zu Skalierungs- und Leistungseinbußen im Identitätswechselszenario führt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entscheidung, wo Sicherheit erzwungen werden soll](deciding-where-to-enforce-security.md)
</dt> <dt>

[Anwendungssicherheit mit mehreren Ebenen](multi-tier-application-security.md)
</dt> </dl>

 

 



