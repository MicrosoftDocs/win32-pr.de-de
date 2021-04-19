---
description: Installiert Gerätetreiber aus Programmen mit einem Setup Skript und INF-Dateien. Schreiben Sie ein Setup Programm für Geräte Einrichtung und Treiberinstallation. Diese API wird nicht mehr zum Zweck der Installation von Softwareanwendungen empfohlen.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: Setup-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360595"
---
# <a name="setup-api"></a>Setup-API

## <a name="purpose"></a>Zweck

Die Setup-API bietet eine Reihe von Funktionen, die von einer Setup Anwendung zum Ausführen von Installations Vorgängen aufgerufen werden.

## <a name="where-applicable"></a>Anwendungsbereich

Diese Setup Funktionen sind zum Entwickeln einer Setup Anwendung verfügbar. Die Setup-API sollte nicht mehr zum Installieren von Anwendungen verwendet werden. Verwenden Sie stattdessen die [Windows Installer](/windows/desktop/Msi/windows-installer-portal)zum Entwickeln von anwendungsinstallern. Die Setup-API wird weiterhin zum Installieren von Gerätetreibern verwendet.

Die Setup-API ist für die Entwicklung von Anwendungen im Desktop Stil vorgesehen.

## <a name="developer-audience"></a>Entwicklergruppe

Ein Entwickler kann die Setup-API verwenden, wenn die Setup Anwendung die folgenden Funktionen erfordert:

-   Dateien werden in die Warteschlange gestellt.
-   Installation von Dateien.
-   Behandlung von Installationsfehlern und Eingabeaufforderung für Medien.
-   Registrierungseinträge werden aktualisiert.
-   Protokollierung von Dateien, während Sie installiert werden.
-   Speicherung der zuletzt verwendeten Quell Pfade.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für die Funktion.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                 | BESCHREIBUNG                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [Übersicht](overview.md)<br/>   | Allgemeine Informationen zur Setup-API.<br/>                                             |
| [Verweis](reference.md)<br/> | Dokumentation der Setup-API-Datentypen,-Strukturen,-Funktionen und-Benachrichtigungen.<br/> |



 

 

