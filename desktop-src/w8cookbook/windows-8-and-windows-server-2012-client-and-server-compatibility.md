---
title: Client-und Server Kompatibilität-Windows 8
description: Kompatibilität von Windows 8-und Windows Server 2012-Clients und-Servern
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313968"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a>Kompatibilität von Windows 8-und Windows Server 2012-Clients und-Servern

In diesem Abschnitt werden Änderungen im Betriebssystem beschrieben, auf die Sie besonders achten sollten, wenn Sie sich auf die potenziellen Auswirkungen auf vorhandene apps auswirken, und wie neue apps auf Clients, auf Servern oder auf Clients und Servern entworfen werden sollten. Im folgenden finden Sie eine Liste der Themen, die in diesem Abschnitt gruppiert nach Funktionsbereich behandelt werden:

**AppCompat**

-   Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen
-   Bestimmen des Shim-Status
-   Server-apps müssen ohne die servergrafikshell ausgeführt werden können
-   RDS-Serverkomponenten werden aus Windows 8 entfernt
-   Dateityp-und Protokoll Zuordnungs Modell
-   Desktopaktivitätenmoderator
-   .NET Framework 4,5 ist Standard, und .NET Framework 3,5 ist optional.
-   Desktop-Apps sind nach dem Starten des Standard Webbrowser möglicherweise nicht sichtbar.
-   Modus mit hohem Kontrast
-   App-Manifest (ausführbare Datei)
-   Ein in der Warteschlange vorhandenes Modell ist veraltet.
-   Szenarios für den Programmkompatibilitäts-Assistenten für Windows 8
-   Desktop-Mini Anwendungen entfernt

**Speicher und Datei System**

-   Update der Datenträger Kompatibilität im erweiterten Format (4K)
-   Schlanke Speicherzuweisung logischer Einheiten
-   Erweiterter Speicher ist jetzt optional für Windows Preinstallation Environment (WinPE) und Server-SKU.
-   Der Dienst für virtuelle Datenträger wird in die WMI-basierte Windows-Speicherverwaltungs-API (Windows-Verwaltungsinstrumentation) übertragen.
-   Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.
-   Storahci ersetzt msahci
-   Windows 7-Sicherung und-Wiederherstellung als veraltet markiert
-   Offloaded-Datenübertragungen

**Andere**

-   Desktopfenster-Manager ist immer on.
-   Direct2D bietet keine Unterstützung für das Rendering in "Rich"-Metadateien in Internet Explorer 9.
-   Änderungen in DX9 Legacy Hardwareunterstützung
-   MSAA ist für Windows Store-Apps nicht verfügbar.
-   Port 3 ist für NDIS 6,30-Treiber veraltet

 

 
