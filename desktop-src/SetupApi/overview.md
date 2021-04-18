---
description: Die Setup-API (Application Programming Interface) bietet eine Reihe von Funktionen, die von der Setup Anwendung aufgerufen werden können, um Installations Vorgänge auszuführen. Diese Setup Funktionen können mit Windows INF-Dateien verwendet werden, um die folgenden Setup Funktionen bereitzustellen.
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358958"
---
# <a name="overview"></a>Übersicht

Die Setup-API (Application Programming Interface) bietet eine Reihe von Funktionen, die von der Setup Anwendung aufgerufen werden können, um Installations Vorgänge auszuführen. Diese Setup Funktionen können mit Windows INF-Dateien verwendet werden, um die folgenden Setup Funktionen bereitzustellen.



| Informationen über                       | Finden Sie unter                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Warteschlangen Dateien                               | [Datei Warteschlangen](file-queues.md)                                                                                                                                              |
| Dateien werden installiert.                            | [Datei Warteschlangen](file-queues.md)<br/> [Setup Anwendungen](setup-applications.md)<br/> [Erstellen von Setup Anwendungen](creating-setup-applications.md)<br/> |
| Behandeln von Fehlern und Eingabeaufforderung für Medien     | [Datenträger Aufforderung und Fehlerbehandlung](disk-prompting-and-error-handling.md)                                                                                                  |
| Aktualisieren von Registrierungs Einträgen                   | [Setup Anwendungen](setup-applications.md)                                                                                                                                |
| Protokollieren installierter Dateien                     | [Datei Protokoll](file-log.md)                                                                                                                                                    |
| Speichern der zuletzt verwendeten Quell Pfade | [MRU-Quell Liste](mru-source-list.md)                                                                                                                                      |



 

Unicode-und ANSI-Versionen sind für die meisten Setup Funktionen verfügbar. Unicode-Textdateien sollten die standardmäßige 0xFEFF-Byte Reihenfolge Markierung enthalten, damit Setup Funktionen die Datei als Unicode-Text identifizieren können.

Die Setup-API unterstützt zwar die Eingabeaufforderung für neue Medien und grundlegende Dialogfelder zur Fehlerbehandlung, aber die Setup-Funktionen bieten keine Assistenten Funktionalität oder eine generische Benutzeroberfläche.

Entwickler sollten berücksichtigen, ob Sie [Windows Installer](/windows/desktop/Msi/windows-installer-portal) verwenden können, um Ihre Anwendungen anstelle der Setup-API zu installieren. Windows Installer senkt die Gesamtbetriebskosten (TCO) für Ihre Kunden, indem es Ihnen ermöglicht, ihre Produkte und Anwendungen effizient zu installieren und zu konfigurieren. Das Installationsprogramm kann Ihrem Produkt auch neue Funktionen zur Verfügung stellen, ohne diese zu installieren, Produkte Bedarfs gesteuert zu installieren und benutzerdefinierte Anpassungen hinzuzufügen.

 

