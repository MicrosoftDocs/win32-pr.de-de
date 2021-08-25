---
description: Liste der geschützten Ressourcen
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Liste der geschützten Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c221068d9185c289d601f53c6b76df9677d8bc213b44f3dc13dbf5b66a0df446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760120"
---
# <a name="protected-resource-list"></a>Liste der geschützten Ressourcen

Die Berechtigung für vollzugriff zum Ändern von WRP-geschützten Ressourcen ist auf TrustedInstaller beschränkt. WRP-geschützte Ressourcen können nur [](supported-file-replacement-mechanisms.md) mithilfe der unterstützten Ressourcenersetzungsmechanismen mit dem Windows Modules Installer-Dienst geändert werden.

WRP schützt Dateien mit den folgenden Erweiterungen, die von Windows Server 2008 oder Windows Vista installiert werden: .dll, .exe, .ocx und .sys.

WRP schützt wichtige Dateien, die von Windows Server 2008 oder Windows Vista installiert werden, mit den folgenden Erweiterungen: .acm, .ade, .adp, .app, .asa, .asp, .aspx, .ax, .bas, .bat, .bin, .cer, .chm, .clb, .cmd, .cnt, .cnv, .com, .cpl, .cpx, .crt, .csh, .dll, .drv, .dtd, .exe, .fxp, .grp, .h1s, .hlp, .hta, .ime, .inf, .ins, .isp, .its, .js, .jse, .ksh, .lnk, .mad, .maf, .mag, .mam, .man, .maq, .mar, .mas, .mat, .mau, .mav, .maw, .mda, .mdb, .mde, .mdt, .mdw, .mdz, .msc, .msi, .msp, .mst, .nls, .ocx, .ops, .pal, .pcd, .pif, .prf, .prg, .pst, .reg, .scf, .vb, .sct, .shb, .shs, .sys, .tlb, .tsp, .url, .vb, .vbe, .vbs, .vsmacros, .vss, .vst, .vsw, .ws, .wsc, .wsf, .wsh,  .xsd und .xsl.

WRP schützt kritische Ordner. Ein Ordner, der nur WRP-geschützte Dateien enthält, kann gesperrt werden, sodass nur das Windows vertrauenswürdige Installationsprogramm Dateien oder Unterordner im Ordner erstellen kann. Ein Ordner ist möglicherweise teilweise gesperrt, damit Administratoren Dateien und Unterordner im Ordner erstellen können.

WRP schützt wichtige Registrierungsschlüssel, die von Windows Server 2008 und Windows Vista installiert wurden. Wenn ein Schlüssel durch WRP geschützt wird, können alle seine Unterschlüssel und Werte geschützt werden.

WRP kopiert Dateien, die zum Neustarten  von Windows im Cacheverzeichnis unter %Windir% \\ winsxs \\ Backup erforderlich sind. Kritische Dateien, die nicht zum Neustarten der Windows werden nicht in das Cacheverzeichnis kopiert. Die Größe des Cacheverzeichnisses und die Liste der in den Cache kopierten Dateien können nicht geändert werden.

**Windows Server 2003 und Windows XP: **

Windows Dateischutz (File Protection, WFP) vor WRP.

WFP schützt Dateien, die von Windows installiert werden, mit den folgenden Erweiterungen: .dll, .exe, .ocx und .sys. Darüber hinaus sind die TrueType-Schriftarten Micross.ttf, Tahoma.ttf und Tahomabd.ttf ebenfalls geschützt.

Am Ende der installation Windows WFP eine Überprüfung aller geschützten Dateien, um sicherzustellen, dass sie nicht von Anwendungen geändert wurden, die durch eine unbeaufsichtigte Installation installiert wurden. WFP kopiert auch überprüfte Versionen dieser Systemdateien in das Cacheverzeichnis. Wenn eine Anwendung versucht, eine geschützte Datei zu ersetzen, kann WFP die ursprüngliche Datei aus dem Cacheverzeichnis wiederherstellen.

Der Standardwert ist %systemroot% \\ system32 \\ dllcache. Um einen anderen Speicherort für den Cache anzugeben, erstellen Sie den folgenden Registrierungswert: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Dies muss ein lokaler Pfad sein. Bei Verwendung eines Netzwerkpfads wird eine einzelne freigegebene Netzwerkquelle für Cachedateien erstellt, vorausgesetzt, alle Clients, die die Freigabe verwenden, führen dieselben Service Packs und Hotfixes aus.

Die Standardgröße des Caches ist unbegrenzt. Um die Größe des Caches zu ändern, verwenden Sie die folgende Registrierungseinstellung: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Wenn der Wert SFC QUOTA ALL FILES ist, werden alle Systemdateien \_ \_ im \_ Cacheverzeichnis zwischengespeichert.

Aus Gründen des Speicherplatzes ist es möglicherweise nicht wünschenswert, zwischengespeicherte Versionen aller Systemdateien im Cacheverzeichnis zu verwalten. Je nach Größe des Caches speichert WFP überprüfte Dateiversionen im Cacheverzeichnis auf der Systemlaufwerke. WFP fügt dem Cache Dateien hinzu, bis die Größe des Cacheverzeichnisses den angegebenen Grenzwert erreicht.

Wenn eine Anwendung versucht, eine geschützte Datei zu ersetzen, die sich nicht im Cache befindet, versucht WFP, die ursprüngliche Datei aus der Installationsquelle wiederherzustellen, und fordert den Benutzer bei Bedarf auf.

 

 



