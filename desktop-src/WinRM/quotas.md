---
title: Kontingent Verwaltung für Remote Shells
description: Die Kontingent Verwaltung ermöglicht es Benutzern, Systemressourcen effizienter zu verwalten.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310920"
---
# <a name="quota-management-for-remote-shells"></a>Kontingent Verwaltung für Remote Shells

Die Kontingent Verwaltung ermöglicht es Benutzern, Systemressourcen effizienter zu verwalten. Windows-Remoteverwaltung (WinRM) hat einen bestimmten Satz von Kontingenten hinzugefügt, die eine bessere Dienst Qualität bieten, Denial-of-Service-Probleme verhindern und gleichzeitigen Benutzern Server Ressourcen zuweisen. Das festgelegte WinRM-Kontingent basiert auf der Kontingent Infrastruktur, die für den Internetinformationsdienste (IIS)-Dienst implementiert wird.

Durch das Implementieren von Kontingenten werden Leistungseinbußen und Denial-of-Service-Probleme durch folgende Aktionen verhindert:

-   Begrenzen der Anzahl von Shells und shellprozessen, die ein Benutzer erstellen kann
-   Einschränken der maximalen Anzahl gleichzeitiger Benutzer
-   Verwalten der Menge an Arbeitsspeicher, die einer Shell zugeordnet ist
-   Festlegen eines Timeouts für inaktive Shells

## <a name="quota-settings"></a>Kontingent Einstellungen

Die folgenden Kontingente müssen für die remoteshellverwaltung erzwungen werden. Diese Kontingente können über das WinRM-Hilfsprogramm oder über Gruppenrichtlinie Einstellungen konfiguriert werden. Von einem Gruppenrichtlinie konfigurierte Einstellungen ersetzen die durch das WinRM-Hilfsprogramm festgelegten Kontingente. Weitere Informationen zum Festlegen von Gruppenrichtlinien für WinRM finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Die maximale Zeit in Millisekunden, bevor eine inaktive Remoteshell gelöscht wird. Der Standardwert ist 180000 Millisekunden. Die minimale Zeit beträgt 1000 Millisekunden.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>Maxprocessespershell
</dt> <dd>

Die maximal zulässige Anzahl von Prozessen Pro Shell, einschließlich der untergeordneten Prozesse der Shell. Der Standard ist 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>Maxmemorypershellmb
</dt> <dd>

Die maximale Menge an Arbeitsspeicher, die Pro Shell zugeordnet ist, einschließlich der untergeordneten Prozesse der Shell. Der Standardwert ist 1024 MB.

> [!Note]  
> Das Verhalten wird nicht unterstützt, wenn maxmemorypershellmb auf einen Wert festgelegt ist, der kleiner als der Standardwert ist.

 

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

WinRM 2,0 legt das maxshellruntime-Kontingent auf schreibgeschützt fest. Das Ändern des Werts für dieses Kontingent hat keine Auswirkung auf die Remote Shells.

## <a name="retrieving-quota-configuration-information"></a>Informationen zur Kontingent Konfiguration werden abgerufen.

Um die Einstellungen für die Kontingent Konfiguration zu überprüfen, geben Sie **WinRM Get WinRM/config** ein.

Der folgende Code Ausschnitt ist ein textbasiertes Beispiel für eine WinRM-Konfiguration mit den standardmäßigen Kontingent Einstellungen.

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

## <a name="configuring-shell-quotas"></a>Konfigurieren von shellkontingente

Kontingente können über eine Gruppenrichtlinie Einstellung oder manuell festgelegt werden. Weitere Informationen zu bestimmten Konfigurationseinstellungen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).

**So legen Sie ein Kontingent mit Gruppenrichtlinie fest**

1.  Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.
2.  Geben Sie an der Eingabeaufforderung **gpeer dit. msc** ein. Das **Gruppenrichtlinienobjekt-Editor** Fenster wird geöffnet.
3.  Suchen Sie die **Windows-Remoteverwaltung** und **Windows remotesshell** Gruppenrichtlinie Objects (GPO) unter **Computer Konfiguration \\ Administrative Vorlagen \\ Windows-Komponenten**.
4.  Wählen Sie auf der Registerkarte **erweitert** eine Einstellung aus, um eine Beschreibung anzuzeigen. Doppelklicken Sie auf eine Einstellung, um Sie zu bearbeiten.

**So legen Sie ein Kontingent manuell fest**

1.  Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.
2.  Geben Sie an der Eingabeaufforderung **WinRM Set WinRM/config/Winrs ' @ { ***<Quota>*** = " ***<Value>*** "} "** ein.

Wenn Sie z. b. die maximale Anzahl von Shells pro Benutzer von 5 auf 7 erhöhen möchten, geben Sie **WinRM Set WinRM/config/Winrs ' @ {maxshellsperuser = "7"}**"ein.

 

 




