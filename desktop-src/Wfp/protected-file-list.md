---
description: Liste geschützter Ressourcen
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Liste geschützter Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316a9bf9233283a7c0aba11f0d5fe8a09f38f1e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218320"
---
# <a name="protected-resource-list"></a>Liste geschützter Ressourcen

Die Berechtigung für den Vollzugriff zum Ändern von durch WRP geschützten Ressourcen ist auf Treuhänder beschränkt. Durch WRP geschützte Ressourcen können nur mithilfe der [unterstützten Ressourcenaustausch Mechanismen](supported-file-replacement-mechanisms.md) mit dem Windows-Modul Installations Dienst geändert werden.

WRP schützt Dateien mit den folgenden Erweiterungen, die von Windows Server 2008 oder Windows Vista installiert werden:. dll,. exe,. ocx und. sys.

WRP schützt wichtige Dateien, die von Windows Server 2008 oder Windows Vista installiert werden, mit den folgenden Erweiterungen:. "ACM", ". ade", ". adp", ". app", ". ASA", ". asp", ". aspx", ". ax", ".,. bat", ". bin", ". cer", ". chm", ". CLB", ". cmd", "" csh ",". dll ",". drv ",". DTD ",". exe ",". f ",". grp ",". H1S ",". hlp ",". hta ",". IME ",". inf ",". ins ",". ISP ",.... ,. MAM,. man,. maq,. Mar,. mas,. Mat,. Mau,. MAV,. Maw,. MDA,. mdb,. MDE,. MDT,. mdw,. mdz,. msc,. msi,. msp,. MST,. MUI,. nls,. ocx,. OPS,. PAL,. PCD,. pif,. prf,. PRG,. PST,. reg,. SCF,. scr,. SCT,. SHB,. SHS,. sys,. tlb,. tsp,. URL,. vb,. vbe,. VSB,. VSMacros,. VSS,. VST,. VSW,. WS,. WSC,. wsf,. WSH,. xsd und. Xsl.

WRP schützt wichtige Ordner. Ein Ordner, der nur durch WRP geschützte Dateien enthält, kann gesperrt werden, sodass nur der Windows-vertrauenswürdige Installer Dateien oder Unterordner im Ordner erstellen kann. Ein Ordner kann teilweise gesperrt sein, damit Administratoren Dateien und Unterordner im Ordner erstellen können.

WRP schützt wichtige Registrierungsschlüssel, die von Windows Server 2008 und Windows Vista installiert werden. Wenn ein Schlüssel durch WRP geschützt ist, können alle seine Unterschlüssel und Werte geschützt werden.

WRP kopiert Dateien, die zum Neustart von Windows benötigt werden, im *Cache Verzeichnis* unter% windir% \\ WinSxS \\ Backup. Wichtige Dateien, die zum Neustart von Windows nicht benötigt werden, werden nicht in das Cache Verzeichnis kopiert. Die Größe des Cache Verzeichnisses und die Liste der in den Cache kopierten Dateien können nicht geändert werden.

* * Windows Server 2003 und Windows XP: * *

Der Windows-Datei Schutz (WFP) war mit dem WRP vor.

WFP schützt Dateien, die von Windows installiert werden, mit den folgenden Erweiterungen:. dll,. exe,. ocx und. sys. Außerdem sind die TrueType-Schriftarten micross. ttf, Tahoma. ttf und TahomaBD. ttf ebenfalls geschützt.

Am Ende der Windows-Installation führt WFP eine Überprüfung aller geschützten Dateien durch, um sicherzustellen, dass Sie nicht durch Anwendungen geändert wurden, die durch eine unbeaufsichtigte Installation installiert wurden. WFP kopiert auch überprüfte Versionen dieser Systemdateien in das Cache Verzeichnis. Wenn eine Anwendung versucht, eine geschützte Datei zu ersetzen, kann die ursprüngliche Datei von WFP aus dem Cache Verzeichnis wieder hergestellt werden.

Der Standardwert ist% SystemRoot% \\ system32 \\ Dllcache. Um einen anderen Speicherort für den Cache anzugeben, erstellen Sie den folgenden Registrierungs Wert: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Dies muss ein lokaler Pfad sein. Wenn Sie einen Netzwerkpfad verwenden, wird eine einzelne freigegebene Netzwerkquelle für Cache Dateien erstellt, vorausgesetzt, dass alle Clients, die die Freigabe verwenden, dieselben Service Packs und Hotfixes ausführen.

Die Standardgröße des Caches ist unbegrenzt. Um die Größe des Caches zu ändern, verwenden Sie die folgende Registrierungs Einstellung: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Wenn der Wert SFC- \_ Kontingent \_ alle \_ Dateien ist, werden alle Systemdateien im Cache Verzeichnis zwischengespeichert.

Aufgrund von Speicherplatz Überlegungen ist es möglicherweise nicht wünschenswert, zwischengespeicherte Versionen aller Systemdateien im Cache Verzeichnis beizubehalten. Abhängig von der Größe des Caches speichert WFP überprüfte Dateiversionen im Cache Verzeichnis auf der System Festplatte. WFP fügt dem Cache Dateien hinzu, bis die Größe des Cache Verzeichnisses das angegebene Limit erreicht.

Wenn eine Anwendung versucht, eine geschützte Datei zu ersetzen, die sich nicht im Cache befindet, versucht WFP, die ursprüngliche Datei aus der Installationsquelle wiederherzustellen, wobei der Benutzer ggf. aufgefordert wird.

 

 



