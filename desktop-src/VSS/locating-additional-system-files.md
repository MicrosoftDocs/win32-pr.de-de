---
description: Beim Ausführen einer VSS-Sicherung oder -Wiederherstellung wird der Windows Systemstatus als Sammlung mehrerer wichtiger Betriebssystemelemente und deren Dateien definiert. Diese Elemente sollten durch Sicherungs- und Wiederherstellungsvorgänge immer als Einheit behandelt werden.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Sichern und Wiederherstellen des Systemstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b027fa0d1a01f3d4f735494d34d4f2da2d07a0e0d82ecfd189f7a9c7c8537c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056398"
---
# <a name="backing-up-and-restoring-system-state"></a>Sichern und Wiederherstellen des Systemstatus

> [!Note]  
> Dieses Thema gilt für Windows Vista, Windows Server 2008 und höher. Informationen zu Windows Server 2003 finden Sie unter Sichern und Wiederherstellen des [Systemstatus in Windows Server 2003 R2 und Windows Server 2003 SP1.](backing-up-and-restoring-system-state-under-vss.md)

 

Beim Ausführen einer VSS-Sicherung oder -Wiederherstellung wird der Windows Systemstatus als Sammlung mehrerer wichtiger Betriebssystemelemente und deren Dateien definiert. Diese Elemente sollten durch Sicherungs- und Wiederherstellungsvorgänge immer als Einheit behandelt werden.

> [!Note]  
> Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatuswiederherstellungen auf Windows (alle Releases).

 

Beim Sichern und Wiederherstellen des Systemzustands wird empfohlen, die System- und Startvolumes zusätzlich zu den dateien, die von den Systemstatuswritern aufzählt werden, zu sichern und wiederherzustellen. Systemzustandswriter sind Writer, bei denen das [**VSS \_ USAGE \_ TYPE-Attribut**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) entweder auf VSS \_ UT \_ BOOTABLESYSTEMSTATE oder VSS \_ UT SYSTEMSERVICE festgelegt \_ ist.

> [!IMPORTANT]
> Wenn ein VSS Writer durch seinen [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) als Systemzustandswriter identifiziert wird, muss er in eine Systemstatussicherung eingeschlossen werden, auch wenn er auswählbar ist.

 

Zusätzlich zu den enumerationsierten Betriebssystem- und Treiberbinärdateien, die von den Systemstatuswritern aufzählt werden, gibt es bestimmte andere Dateien, die als Teil des Systemzustands gesichert werden müssen.

Alle von einem VSS-Systemstatuswriter gemeldeten Komponenten sind Teil des Systemzustands, mit Ausnahme der Komponenten, für die das VSS \_ CF \_ NOT SYSTEM \_ \_ STATE-Flag festgelegt ist.

Sicherungsprogramme sollten auch den **Registrierungsschlüssel LastRestoreId** festlegen. Weitere Informationen finden Sie unter [Registrierungsschlüssel und -werte für Sicherung und Wiederherstellung.](../backup/registry-keys-for-backup-and-restore.md)

> [!Note]  
> In Windows Vista, Windows Server 2008 und höher wurden die Namen und Speicherorte einiger Systemdateien wie folgt geändert.

 

## <a name="system-state"></a>Systemstatus

Für Windows Server 2012 und höher müssen zusätzlich zu den Dateien, die von den verschiedenen VSS-Systemstatuswritern gemeldet werden, nur die folgenden Lizenzierungsdateien explizit eingeschlossen werden, und die folgenden DRM-Dateien müssen explizit ausgeschlossen werden.

## <a name="windows-media-digital-rights-management-files"></a>Windows Media Digital Rights Management Files

In Windows Server 2008 und höher werden die folgenden Dateien, einschließlich aller Unterverzeichnisse unter dem folgenden Pfad, aus dem Systemstatus ausgeschlossen und dürfen nicht gesichert werden:

-   %ProgramData% \\ Microsoft \\ Windows \\ DRM\\

Dadurch werden die Informationen im Abschnitt Windows Media Digital Rights Management von [Working with File System and Security Features (Arbeiten mit Dateisystem- und Sicherheitsfeatures)](working-with-file-system-and-security-features.md)ersetzt.

## <a name="performance-counter-configuration-files"></a>Konfigurationsdateien für Leistungsindikatoren

Die Konfigurationsdateien des Leistungsindikators befinden sich im Verzeichnis %SystemRoot% \\ System32 \\ und haben die folgenden Namen:

<dl> Perf?00?. Dat  
Perfc0??. Dat  
Perfd0??. Dat  
Perfh0??. Dat  
Perfi0??. Dat  
Prfc0???. Dat  
Prfd0???. Dat  
Prfh0???. Dat  
Prfi0???. Dat  
</dl>

Diese Dateien werden nur während der Anwendungsinstallation geändert und sollten bei Systemstatussicherungen und -wiederherstellungen gesichert und wiederhergestellt werden.

## <a name="iis-configuration-files"></a>IIS-Konfigurationsdateien

> [!Note]  
> In Windows Vista mit Service Pack 1 (SP1) und höher sollten Sie diese Dateien nicht sichern. Verwenden Sie stattdessen den in-box-IIS-Konfigurationswriter. Weitere Informationen zu diesem Writer finden Sie unter [In-Box VSS Writers](in-box-vss-writers.md).

 

Die relevanten IIS-Konfigurationsdateien und deren Speicherorte sind unten aufgeführt:

-   Die .NET FX machine.config-Datei befindet sich im Frameworkversionsverzeichnis.
-   Die ASP.NET Stammdatei web.config befindet sich im Frameworkversionsverzeichnis.
    > [!Note]  
    > Die Konfigurationsdateien für .NET FX und ASP.NET befinden sich im Framework-Versionsverzeichnis. Wenn mehrere Versionen des Frameworks auf dem Computer installiert sind, enthält dieses Verzeichnis eine Konfigurationsdatei für jede installierte Version.

     

-   Die IIS-applicationHost.config zentrale Konfigurationsdatei befindet sich im Verzeichnis %windir% \\ system32 \\ inetsrv \\ config. Damit der Server diese Konfigurationsdatei verstehen kann, gibt es Schemadateien, die die Grammatik und Struktur bestimmen. Diese Dateien befinden sich im Schemaverzeichnis %windir% \\ system32 \\ inetsrv \\ \\ config.

Der Verzeichnispfad der Frameworkversion wird im folgenden Registrierungsschlüssel gespeichert:

**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ . NETFramework \\ InstallRoot**

Darüber hinaus müssen die folgenden Kryptografieschlüssel gesichert werden:<dl> %ProgramData% \\ Microsoft Crypto RSA \\ \\ \\ MachineKeys\\\*  
%SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>Frameworkdateien

Alle Versionen von .NET Framework müssen gesichert werden. Die Dateien befinden sich in einem oder beiden der folgenden Verzeichnisse:

<dl> %windir% \\ Microsoft.Net \\ Framework  
%windir% \\ Microsoft.Net \\ Framework64  
</dl>

Darüber hinaus müssen die Assemblydateien gesichert werden. Diese Dateien befinden sich im folgenden Verzeichnis:<dl> \\%windir%-Assembly  
</dl>

## <a name="task-scheduler-task-files"></a>Taskplaner Taskdateien

Die Taskdateien des Taskplaners müssen gesichert werden. Die Dateien befinden sich an einem oder beiden der folgenden Speicherorte:

<dl> %windir% \\ system32 \\ Tasks und alle Unterverzeichnisse (rekursiv)  
%windir% \\ tasks (keine Unterverzeichnisse)  
</dl>

 

 
