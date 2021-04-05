---
description: Beim Ausführen einer VSS-Sicherung oder-Wiederherstellung wird der Windows-Systemstatus als eine Sammlung mehrerer wichtiger Betriebssystem Elemente und der zugehörigen Dateien definiert. Diese Elemente sollten bei Sicherungs-und Wiederherstellungs Vorgängen immer als Einheit behandelt werden.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Sichern und Wiederherstellen des System Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755544"
---
# <a name="backing-up-and-restoring-system-state"></a>Sichern und Wiederherstellen des System Status

> [!Note]  
> Dieses Thema gilt für Windows Vista, Windows Server 2008 und höher. Informationen zu Windows Server 2003 finden Sie unter [Sichern und Wiederherstellen des System Status in Windows Server 2003 R2 und Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md) .

 

Beim Ausführen einer VSS-Sicherung oder-Wiederherstellung wird der Windows-Systemstatus als eine Sammlung mehrerer wichtiger Betriebssystem Elemente und der zugehörigen Dateien definiert. Diese Elemente sollten bei Sicherungs-und Wiederherstellungs Vorgängen immer als Einheit behandelt werden.

> [!Note]  
> Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatus Wiederherstellungen unter Windows (alle Versionen).

 

Wenn Sie den Systemstatus sichern und wiederherstellen, empfiehlt es sich, zusätzlich zu den Dateien, die von den systemstatuswritern aufgelistet werden, die System-und Startvolumes zu sichern und wiederherzustellen. Systemstatuswriter sind Writer, für die das [**VSS \_ Usage \_ Type**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) -Attribut entweder auf VSS- \_ UT \_ bootablesystemstate oder VSS \_ UT \_ Systemservice festgelegt ist.

> [!IMPORTANT]
> Wenn ein VSS-Writer durch seinen [**VSS- \_ \_ Verwendungstyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) als systemstatuswriter identifiziert wird, muss er in eine Systemstatus Sicherung eingeschlossen werden, auch wenn er auswählbar ist.

 

Zusätzlich zu den aufgelisteten Betriebssystem-und Treiber Binärdateien, die vom Systemstatus Schreiber aufgelistet werden, gibt es bestimmte andere Dateien, die als Teil des Systemstatus gesichert werden müssen.

Alle von einem VSS-systemstatuswriter gemeldeten Komponenten sind Teil des Systemstatus, außer denen, für die das VSS \_ CF- \_ Flag "nicht- \_ Systemstatus" \_ festgelegt ist.

Sicherungs Programme sollten auch den **lastrestoreid** -Registrierungsschlüssel festlegen. Weitere Informationen finden Sie unter [Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung](../backup/registry-keys-for-backup-and-restore.md).

> [!Note]  
> In Windows Vista, Windows Server 2008 und höher wurden die Namen und Speicherorte einiger Systemdateien wie folgt geändert.

 

## <a name="system-state"></a>Systemstatus

Für Windows Server 2012 und höher müssen zusätzlich zu den Dateien, die von den verschiedenen VSS-Systemstatus-Writern gemeldet werden, nur die folgenden Lizenzierungs Dateien explizit eingeschlossen werden, und die folgenden DRM-Dateien müssen explizit ausgeschlossen werden.

## <a name="windows-media-digital-rights-management-files"></a>Digitale Rights Management Dateien für Windows Media

In Windows Server 2008 und höher sind die folgenden Dateien, einschließlich aller Unterverzeichnisse unter folgendem Pfad, aus dem Systemstatus ausgeschlossen und dürfen nicht gesichert werden:

-   % Program Data% \\ Microsoft \\ Windows \\ DRM\\

Dies ersetzt die Informationen im Abschnitt Windows Media Digital Rights Management unter [Arbeiten mit Datei System-und Sicherheits Features](working-with-file-system-and-security-features.md).

## <a name="performance-counter-configuration-files"></a>Leistungsindikatationsdateien

Die Leistungsdaten-Konfigurationsdateien befinden sich im Verzeichnis% systemroot% \\ system32 \\ und haben die folgenden Namen:

<dl> Leistung? 00?. Hütte  
Perfc0??. Hütte  
Perfd0??. Hütte  
Perfh0??. Hütte  
Perfi0??. Hütte  
Prfc0???. Hütte  
Prfd0???. Hütte  
Prfh0???. Hütte  
Prfi0???. Hütte  
</dl>

Diese Dateien werden nur während der Anwendungs Installation geändert und sollten während der Sicherung und Wiederherstellung des Systemstatus gesichert und wieder hergestellt werden.

## <a name="iis-configuration-files"></a>IIS-Konfigurationsdateien

> [!Note]  
> In Windows Vista mit Service Pack 1 (SP1) und höher sollten Sie diese Dateien nicht sichern. Verwenden Sie stattdessen den in-Box-IIS-konfigurationswriter. Weitere Informationen zu diesem Writer finden Sie unter [in-Box-VSS-Writer](in-box-vss-writers.md).

 

Die relevanten IIS-Konfigurationsdateien und ihre Speicherorte sind unten aufgeführt:

-   Die .net FX-machine.config Datei befindet sich im Framework Version-Verzeichnis.
-   Die ASP.net-Stamm web.config Datei befindet sich im Framework-Versions Verzeichnis.
    > [!Note]  
    > Die Konfigurationsdateien für .net FX und ASP.net befinden sich im Framework Version-Verzeichnis. Wenn mehrere Versionen des Frameworks auf dem Computer installiert sind, enthält dieses Verzeichnis eine Konfigurationsdatei für jede installierte Version.

     

-   Die IIS-applicationHost.config zentrale Konfigurationsdatei befindet sich im Verzeichnis% windir% \\ system32 \\ inetsrv \\ config. Damit der Server diese Konfigurationsdatei versteht, sind Schema Dateien vorhanden, die die Grammatik und Struktur bestimmen. Diese Dateien befinden sich im Verzeichnis% windir% \\ system32 \\ inetsrv \\ config \\ Schema.

Der Verzeichnispfad der Frameworkversion ist im folgenden Registrierungsschlüssel gespeichert:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ . NETFramework- \\ InstallRoot**

Außerdem müssen die folgenden Kryptografieschlüssel gesichert werden:<dl> % Program Data% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*  
% Systemroot% \\ system32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>Frameworkdateien

Alle Versionen von .NET Framework müssen gesichert werden. Die Dateien befinden sich in einem oder beiden der folgenden Verzeichnisse:

<dl> % windir% \\ Microsoft.net \\ Framework  
% windir% \\ Microsoft.net \\ Framework64  
</dl>

Außerdem müssen die Assemblydateien gesichert werden. Diese Dateien befinden sich im folgenden Verzeichnis:<dl> % windir% \\ Assembly  
</dl>

## <a name="task-scheduler-task-files"></a>Taskplaner von Aufgaben Dateien

Die Aufgaben Dateien des Aufgaben Planers müssen gesichert werden. Die Dateien befinden sich an einem oder beiden der folgenden Speicherorte:

<dl> % windir% \\ system32 \\ Tasks und alle Unterverzeichnisse (rekursiv)  
% windir% \\ Tasks (keine Unterverzeichnisse)  
</dl>

 

 
