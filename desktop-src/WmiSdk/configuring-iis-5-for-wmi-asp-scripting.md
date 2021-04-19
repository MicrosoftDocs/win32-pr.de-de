---
description: Alle Authentifizierungs Einstellungen werden über den Internetdienste-Manager vorgenommen.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Konfigurieren von IIS 5,0 und höher für die WMI-ASP-Skripterstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355640"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a>Konfigurieren von IIS 5,0 und höher für die WMI-ASP-Skripterstellung

Alle Authentifizierungs Einstellungen werden über den Internetdienste-Manager vorgenommen.

Beachten Sie beim Konfigurieren von Internet Information Server (IIS) 5,0 und IIS 6,0 Security für WMI ASP-Skripts die folgenden Punkte:

-   [Authentifizierungsebene](#authentication-level)

    Sie können auf Server-, Verzeichnis-oder Dateiebene konfigurieren.

-   [Authentifizierungs Einstellung](#authentication-setting)

    Sie können die Authentifizierung auf anonyme, integrierte Fenster oder beides festlegen.

-   [Schutz](#protection)

    Sie können festlegen, dass der ASP-Prozess in-Process (niedriger Schutz) oder außerhalb des Prozesses ausgeführt wird, indem Sie Dllhost.exe (mittlerer oder hoher Schutz) verwenden.

## <a name="authentication-level"></a>Authentifizierungs Ebene

Zur zusätzlichen Sicherheit können Sie die Authentifizierung auf Verzeichnis-oder Dateiebene konfigurieren.

Wenn die Authentifizierung auf Serverebene festgelegt ist, werden alle nachfolgenden Verzeichnisse und Dateien der Server Authentifizierung entsprechen, sofern Sie nicht explizit auf Verzeichnis-oder Dateiebene geändert werden. Sie können eine Verzeichnisstruktur erstellen, die alle WMI-ASP-Skripts enthält, in denen HTML-Seiten und für WMI spezifische-spezifische Informationen unabhängig vom Rest des Servers konfiguriert werden können. Führen Sie das folgende Verfahren aus, um die Authentifizierungs Ebene eines Servers, Verzeichnisses oder einer Datei zu ändern.

**So legen Sie die Authentifizierung auf einer beliebigen Ebene fest**

1.  Doppelklicken Sie in der Systemsteuerung auf **Verwaltung**, und doppelklicken Sie dann auf das IIS-Snap-in.

2.  Suchen Sie das ASP-Seiten Symbol, und öffnen Sie dann die Eigenschaften für die festzulegende Ebene (Server, Verzeichnis oder Datei).

    > [!Note]  
    > Die Authentifizierungs Einstellungen befinden sich auf der Registerkarte **Verzeichnis Sicherheit** oder **Datei Sicherheit** des **Eigenschaften** Blatts.

     

## <a name="authentication-setting"></a>Authentifizierungs Einstellung

Bei WMI-ASP-Skripts bietet die Kombination aus aktivierter anonymer Authentifizierung (deaktiviert) und integrierter Windows-Authentifizierung (aktiviert) mehr Möglichkeiten zum Festlegen der Sicherheit. Um die IIS-Authentifizierungs Einstellungen von NT LAN Manager (NTLM), Passport oder Digest verwenden zu können, müssen Sie die Remote Aktivierungs Berechtigungen aktivieren, da der Benutzer als Netzwerk Identität behandelt und Remote protokolliert wird. Die Einstellung für die Remote Aktivierung ist für die anonyme Authentifizierung und die Standard Authentifizierung nicht erforderlich. Das System ist jedoch viel weniger sicher, wenn Sie die anonyme Authentifizierung und die Standard Authentifizierung verwenden.

Wenn die anonyme Authentifizierung mit oder ohne integrierte Windows-Authentifizierung verwendet wird, besteht der sicherste Ansatz darin, eine Anmeldung zu verwenden, bei der ein Benutzer einen Benutzernamen und ein Kennwort eingeben muss. Die Standardanmeldung ist die IIS-Identität, aber eine Anmeldung kann erstellt werden, indem bestimmte Berechtigungen verwendet werden, die für die WMI-ASP-Skripts geeignet sind und als Konto für die anonymen oder Gast Verbindungen verwendet werden können.

Wenn Sie eine Anmelde-ID auswählen, bei der es sich nicht um eine IIS-Identität handelt, deaktivieren Sie das Kontrollkästchen **IIS-Kennwort steuern** , und geben Sie das richtige Kennwort ein. Dadurch werden alle anonymen oder Gast Verbindungen gezwungen, den Anmelde Bezeichner zu verwenden. Durch das Erstellen einer Anmeldung getrennt von der IIS-Identität können die Berechtigungen eines Kontos, das auf WMI zugreift, ohne Auswirkung auf die anderen Verzeichnisse oder Dateien auf dem IIS-Server gesteuert werden – es sei denn, die Authentifizierung ist auf Serverebene festgelegt.

Führen Sie das folgende Verfahren aus, um die Authentifizierungsanforderungen für die ASP-Seite mithilfe des IIS-Snap-Ins in der Systemsteuerung festzulegen.

**So gelangen Sie zur Konto Einstellung**

1.  Doppelklicken Sie in der Systemsteuerung auf das Symbol **Verwaltung** , öffnen Sie das IIS-Snap-in, suchen Sie die ASP-Seite, und öffnen Sie die Eigenschaften der festzulegenden Ebene (Server, Verzeichnis oder Datei).

    Die Authentifizierungs Einstellungen befinden sich auf der Registerkarte **Verzeichnis Sicherheit** oder **Datei Sicherheit** des **Eigenschaften** Blatts.

2.  Klicken Sie im Bereich anonyme Authentifizierung auf **Bearbeiten**.

3.  Wenn ein anderer Anmelde-ID als die IIS-Identität ausgewählt ist, deaktivieren Sie das Kontrollkästchen zum **Steuern des Kennworts für IIS zulassen**, und geben Sie das richtige Kennwort ein. Dadurch werden alle anonymen oder Gast Verbindungen gezwungen, den Anmelde Bezeichner zu verwenden.

Durch die Verwendung einer anderen Anmeldung als der IIS-Identität können die Berechtigungen des Kontos, das auf WMI zugreift, ohne Auswirkung auf die anderen Verzeichnisse oder Dateien auf dem IIS-Server gesteuert werden – es sei denn, die Authentifizierung ist auf Serverebene festgelegt.

Die vorherige Konfiguration ermöglicht dem IIS-Server die Verwendung der anonymen Authentifizierung in einigen Bereichen, der integrierten Windows-Authentifizierung oder der gemischten Authentifizierung in anderen.

## <a name="protection"></a>Schutz

Beim Konfigurieren des IIS-Servers sollte bei der letzten Überlegung der Schutz beim Ausführen eines ASP verwendet werden.

Sie können einen ASP festlegen, um Folgendes auszuführen:

-   Prozess interne zu IIS (niedriger Schutz).

-   Extern zu IIS mit Dllhost.exe als Pool oder außerhalb des Prozesses (gepoolter mittlerer Schutz).

-   Out-of-Process-Self-Host (hoher Schutz).

> [!Note]  
> Verwenden Sie in einem Pool zusammengefasste Hosts, um die Sicherheit und Leistung am besten auszugleichen.

 

 

 



