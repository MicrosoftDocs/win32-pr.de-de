---
description: In diesem Thema werden einige Baustein Szenarien vorgestellt, in denen die Kriterien erläutert werden, die unter entscheiden, wo Sicherheit erzwungen werden soll.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346240"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a>Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen

In diesem Thema werden einige Baustein Szenarien vorgestellt, in denen die Kriterien erläutert werden, die unter [entscheiden, wo Sicherheit](deciding-where-to-enforce-security.md)erzwungen werden soll.

## <a name="trusted-server-scenario"></a>Szenario des vertrauenswürdigen Servers

-   Die-Datenbank vertraut der com+-Anwendung vollständig, um Endbenutzern den Zugriff auf Daten in der Datenbank zu authentifizieren und zu autorisieren.
-   Vorzugsweise ist die Datenbank vor allen Zugriffen geschützt, außer über die Anwendung.
-   Die COM+-Anwendung verwendet rollenbasierte Sicherheit, um Benutzer zu autorisieren.
-   Verbindungen werden unter der com+-Anwendungs Identität geöffnet und können vollständig gebündelt werden.
-   Überwachung und Protokollierung können von der com+-Anwendung ausgeführt werden, oder diese Informationen können von der Anwendung an die Datenbank übermittelt werden.

Dieses Szenario eignet sich am besten für Daten, auf die über vorhersagbare Benutzer Kategorien zugegriffen werden kann, die in Rollen gekapselt werden können. Beispielsweise haben nur "Manager", "Kassierer" und "Buchhaltung" Berechtigungen für den Zugriff auf Konten. Die Geschäftslogik, für die genau jede aktiviert ist, wird in der mittleren Ebene erzwungen.

## <a name="impersonation-scenario"></a>Identitätswechsel Szenario

-   Die Datenbank übernimmt eine eigene Authentifizierung und Autorisierung von Endbenutzern, um den Zugriff auf Daten in der Datenbank einzuschränken.
-   Die COM+-Anwendung nimmt die Identität der Clients an, wenn Sie auf die Datenbank zugreift.
-   Verbindungen werden pro Rückruf hergestellt und können nicht wieder verwendet werden.

Dieses Szenario eignet sich am besten für Daten, die eng an sehr kleine Benutzer Klassen gebunden sind. Beispielsweise kann jeder Mitarbeiter nur auf seine eigene Personal Datei zugreifen, und jeder Manager kann nur auf die Personaldateien der Berichte zugreifen.

## <a name="hybrid-scenario"></a>Hybrid Szenario

Eine Kombination der beiden vorangehenden Szenarien, bei denen der Identitätswechsel nur bei Bedarf verwendet wird.

Dieses Szenario funktioniert am besten in Situationen, in denen Sie über hybride Benutzerdaten Beziehungen verfügen. Sie haben z. b. "Manager", "Kassierer", "Buchhaltung" und Tausende von einzelnen Webclients, die nur auf Ihre eigenen Konten zugreifen können. Sie können Logik Pfade durch die Anwendung, möglicherweise mit separaten Komponenten, trennen, um die letztgenannte Benutzerklasse zu verarbeiten, insbesondere dann, wenn sich die Leistungs Annahmen für diese Benutzer unterscheiden.

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a>Vertrauenswürdiges Szenario mit Microsoft SQL Server Rollen

-   Microsoft SQL Server 7,0 und höher kann den Zugriff auf bestimmte Zeilen mithilfe von Rollen autorisieren, vertraut jedoch der com+-Anwendung, um Benutzer zu authentifizieren und zu autorisieren und Sie den richtigen Rollen in der Datenbank zuzuordnen.
-   Die COM+-Anwendung autorisiert Benutzer mithilfe der rollenbasierten Sicherheit, und die Anwendungs Rollen entsprechen den Daten bankrollen.
-   Verbindungen können für eine bestimmte Daten Bank Rolle geöffnet werden. Diese Verbindungen können wieder verwendet werden, wenn Sie von in einem Pool zusammengefassten Objekten in den COM+-Anwendungen aufbewahrt werden. Weitere Informationen hierzu finden Sie unter [com+-Objekt Pooling](com--object-pooling.md).
-   Überwachung und Protokollierung können von der com+-Anwendung durchgeführt werden, oder diese Informationen können von der Anwendung an die Datenbank übermittelt werden.

Dieses Szenario eignet sich am besten für dieselben Benutzer und Daten wie für das erste vertrauenswürdige Server Szenario, da die COM+-Anwendung immer noch vertrauenswürdig ist, um die Autorisierung ordnungsgemäß zu verarbeiten. Allerdings schützt Sie die Datenbank vor nicht autorisiertem Zugriff und ermöglicht gleichzeitig den Zugriff von mehreren Quellen außerhalb der com+-Anwendung, ohne dass die Skalierungs-und Leistungseinbußen beim Identitätswechsel Szenario anfallen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Erzwingung der Sicherheit](deciding-where-to-enforce-security.md)
</dt> <dt>

[Multi-Tier-Anwendungssicherheit](multi-tier-application-security.md)
</dt> </dl>

 

 



