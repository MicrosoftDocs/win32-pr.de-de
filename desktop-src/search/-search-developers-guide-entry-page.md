---
description: Drittanbieter können Anwendungen erstellen, die den Index für Daten Programm gesteuert Abfragen und Windows Search so erweitern, dass Daten aus benutzerdefinierten Dateiformaten und Daten speichern indiziert werden.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Entwicklerhandbuch für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484443"
---
# <a name="windows-search-developers-guide"></a>Entwicklerhandbuch für Windows Search

Drittanbieter können Anwendungen erstellen, die den Index für Daten Programm gesteuert Abfragen und Windows Search so erweitern, dass Daten aus benutzerdefinierten Dateiformaten und Daten speichern indiziert werden. Um Windows Search-Anwendungen zu erstellen, müssen Entwickler von Drittanbietern zuerst einen Shell-Datenspeicher implementieren, um eine sinnvolle Benutzer Leistung zu erzielen. Weitere Informationen finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Sie müssen auch die [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) für die Windows Search-Bibliotheken herunterladen. Die [Beispiele für Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) enthalten nützliche Codebeispiele und eine Interoperabilität-Assembly für die Entwicklung mit verwaltetem Code. Weitere Informationen zur Verwendung der Codebeispiele finden Sie unter [Codebeispiele für Windows-Suche](-search-3x-wds-sampleentry.md).

Dieser Abschnitt ist wie folgt organisiert:

- [Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)
- [Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
- [Erweitern des Indexes](-search-3x-wds-extidx-overview.md)
- [Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Weitere Ressourcen

- Informationen zu den von der Community unterstützten Frage-und Diskussions Nachrichten für Suchtechnologien finden Sie im [MSDN-Forum: Entwicklung von Windows-Desktop-suchen](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- So laden Sie die Such Code Beispiele herunter:
  - [Beispiele für Windows-Suche](-search-samples-ovw.md)
- So laden Sie die Windows SDK herunter:
  - Für Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Für Windows 7: [Windows SDK für Windows 7 und .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Zugehörige Themen

[Übersicht über Windows Search](-search-3x-wds-overview.md)

[Referenz zur Windows-Suche](-search-reference-entry-page.md)

[Code Beispiele für Windows Search](-search-samples-ovw.md)

[Verbundsuche in Windows 10](-search-federated-search-overview.md)

[Verwandte Suchtechnologien](-search-3x-wds-sampleentry.md)

[Glossar für Windows-Suche](search-glossary.md)
