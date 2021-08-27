---
title: Kontingentverwaltung für Remoteshells
description: Mit der Kontingentverwaltung können Benutzer Systemressourcen effizienter verwalten.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8cfa177d6f09552238471ff29d81d0ac0b7351
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883219"
---
# <a name="quota-management-for-remote-shells"></a>Kontingentverwaltung für Remoteshells

Mit der Kontingentverwaltung können Benutzer Systemressourcen effizienter verwalten. Windows Die Remoteverwaltung (WinRM) hat einen bestimmten Satz von Kontingenten hinzugefügt, die eine bessere Dienstqualität bieten, Denial-of-Service-Probleme verhindern und gleichzeitigen Benutzern Serverressourcen zuweisen. Der WinRM-Kontingentsatz basiert auf der Kontingentinfrastruktur, die für den Internetinformationsdienste (IIS)-Dienst implementiert ist.

Die Implementierung von Kontingenten hilft, Leistungseinbußen und Denial-of-Service-Probleme zu verhindern, indem Folgendes erreicht wird:

-   Beschränken der Anzahl von Shells und Shellprozessen, die ein Benutzer erstellen kann
-   Beschränken der maximalen Anzahl gleichzeitiger Benutzer
-   Verwalten der Arbeitsspeichermenge, die einer Shell zugeordnet ist
-   Festlegen eines Time out für inaktive Shells

## <a name="quota-settings"></a>Kontingente Einstellungen

Die folgenden Kontingente müssen für die Remoteshellverwaltung erzwungen werden. Diese Kontingente können über das Hilfsprogramm winrm oder über Gruppenrichtlinie konfiguriert werden. Einstellungen von einem -Gruppenrichtlinie die vom Hilfsprogramm winrm festgelegten Kontingente ab. Weitere Informationen zum Festlegen von Gruppenrichtlinien für WinRM finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md)

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>Idletimeout
</dt> <dd>

Die maximale Zeit in Millisekunden, bevor eine inaktive Remoteshell gelöscht wird. Der Standardwert ist 180.000 Millisekunden. Die Mindestzeit beträgt 1.000 Millisekunden.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

Die maximale Anzahl von Prozessen, die pro Shell zulässig sind, einschließlich der untergeordneten Prozesse der Shell. Der Standard ist 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

Die maximale Arbeitsspeichermenge, die pro Shell zugeordnet ist, einschließlich der untergeordneten Prozesse der Shell. Der Standardwert ist 1024 MB.

> [!Note]  
> Das Verhalten wird nicht unterstützt, wenn MaxMemoryPerShellMB auf einen Wert festgelegt ist, der kleiner als der Standardwert ist.

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

Die maximale Anzahl von Shells pro Benutzer. Der Standardwert ist 30.

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

Die maximale Anzahl gleichzeitiger Benutzer, die Shells öffnen können. Der Standardwert ist 10.

</dd> </dl>

## <a name="deprecated-quotas"></a>Veraltete Kontingente

WinRM 2.0 legt das MaxShellRunTime-Kontingent auf schreibgeschützt fest. Das Ändern des Werts für dieses Kontingent hat keine Auswirkungen auf die Remoteshells.

## <a name="retrieving-quota-configuration-information"></a>Abrufen von Kontingentkonfigurationsinformationen

Geben Sie **winrm get winrm/config** ein, um die Kontingentkonfigurationseinstellungen zu überprüfen.

Der folgende Codeausschnitt ist ein textbasiertes Beispiel für eine WinRM-Konfiguration mit den Standardkontingenteinstellungen.

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a>Konfigurieren von Shellkontingenten

Kontingente können über eine Gruppenrichtlinie oder manuell festgelegt werden. Weitere Informationen zu bestimmten Konfigurationseinstellungen finden Sie unter [Installation und Konfiguration für Windows Remoteverwaltung.](installation-and-configuration-for-windows-remote-management.md)

**So legen Sie ein Kontingent mit Gruppenrichtlinie**

1.  Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.
2.  Geben Sie an der Eingabeaufforderung **gpedit.msc ein.** Das **Gruppenrichtlinienobjekt-Editor** wird geöffnet.
3.  Suchen Sie **Windows remote management** and Windows Remote **Shell** Gruppenrichtlinie Objects (GPO) unter Computer configuration Administrative Vorlagen **Windows \\ \\ Components**(Computerkonfigurationskomponenten).
4.  Wählen Sie **auf der** Registerkarte Erweitert eine Einstellung aus, um eine Beschreibung zu sehen. Doppelklicken Sie auf eine Einstellung, um sie zu bearbeiten.

**So legen Sie ein Kontingent manuell fest**

1.  Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.
2.  Geben Sie an der Eingabeaufforderung **winrm set winrm/config/winrs '@{**_&lt; Quota &gt;_="_&lt; Value &gt;_*_"}" ein._* **

Um beispielsweise die maximale Anzahl von Shells pro Benutzer von 5 auf 7 zu erhöhen, geben Sie **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}' ein.**

 

 




