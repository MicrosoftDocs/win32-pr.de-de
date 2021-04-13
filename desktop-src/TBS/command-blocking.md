---
title: Befehls Blockierung
description: Um die Integrität von Vorgängen aufrechtzuerhalten, dürfen bestimmte TPM-Befehle von Software auf der Plattform nicht ausgeführt werden.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104390101"
---
# <a name="command-blocking"></a>Befehls Blockierung

Um die Integrität von Vorgängen aufrechtzuerhalten, dürfen bestimmte TPM-Befehle von Software auf der Plattform nicht ausgeführt werden. Beispielsweise werden einige Befehle nur von der Systemsoftware ausgeführt. Wenn die TSB einen Befehl blockiert, wird nach Bedarf ein Fehler zurückgegeben. Standardmäßig blockiert TSB Befehle, die Auswirkungen auf den System Datenschutz, die Sicherheit und die Stabilität haben können. Der TSB geht auch davon aus, dass andere Teile des Software Stapels den Zugriff auf bestimmte Befehle auf autorisierte Entitäten einschränken können.

Für TPM-Befehle der Version 1,2 gibt es drei Listen mit blockierten Befehlen: eine Liste, die von der Gruppenrichtlinie gesteuert wird, eine Liste, die von lokalen Administratoren gesteuert wird, und eine Standardliste. Ein TPM-Befehl wird blockiert, wenn er in einer der Listen vorhanden ist. Es gibt jedoch Gruppenrichtlinien Flags, mit denen die TSB die lokale Liste und die Standardliste ignorieren kann. Die Gruppen Richtlinienflags können direkt bearbeitet oder über den Gruppenrichtlinienobjekt-Editor auf Sie zugegriffen werden.

> [!Note]  
> Die Liste der lokal blockierten Befehle wird nach einem Upgrade auf das Betriebssystem nicht beibehalten. Befehle, die in der Gruppenrichtlinie Liste blockiert werden, werden beibehalten.

 

Bei TPM-Befehlen der Version 2,0 wird die Logik für die Blockierung invertiert. Es wird eine Liste zulässiger Befehle verwendet. Diese Logik blockiert automatisch Befehle, die nicht bekannt waren, als die Liste erstmalig erstellt wurde. Wenn der TPM-Spezifikation Befehle hinzugefügt werden, nachdem eine Version von Windows ausgeliefert wurde, werden diese neuen Befehle automatisch blockiert. Nur ein Update der Registrierung fügt diese neuen Befehle der Liste der zulässigen Befehle hinzu.

Ab Windows 10 1809 (Windows Server 2019) können zulässige TPM 2,0-Befehle nicht mehr über Registrierungs Einstellungen manipuliert werden. Für diese Windows 10-Versionen werden die zulässigen TPM 2,0-Befehle im TPM-Treiber korrigiert. TPM 1,2-Befehle können weiterhin blockiert und durch Registrierungs Änderungen aufgehoben werden. 

## <a name="direct-registry-access"></a>Direkter Registrierungs Zugriff

Die Gruppenrichtlinie-Flags befinden sich unter dem Registrierungsschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **blockedcommands**.

Um zu ermitteln, welche Listen zum Blockieren von TPM-Befehlen verwendet werden sollen, gibt es zwei **DWORD** -Werte, die als boolesche Flags verwendet werden:

-   "Ignoredefaultlist"

    Wenn festgelegt ist (der Wert ist vorhanden und ungleich null), ignoriert TSB die Liste der blockierten Standard Befehle.

-   "Ignorelocallist"

    Wenn festgelegt ist (der Wert ist vorhanden und nicht null), ignoriert TSB die Liste der lokalen blockierten Befehle.

## <a name="group-policy-object-editor"></a>Gruppenrichtlinienobjekt-Editor

**So greifen Sie auf den Gruppenrichtlinie Objekt-Editor zu**

1.  Klicken Sie auf **Start**.
2.  Klicken Sie auf **Ausführen**.
3.  Geben Sie **gpedit.msc** im Feld **Öffnen** ein. Klicken Sie auf **OK**. Der Gruppenrichtlinie Objekt-Editor wird geöffnet.
4.  Erweitern Sie **Computer Konfiguration**.
5.  Erweitern Sie **Administrative Vorlagen**.
6.  Erweitern Sie **System**.
7.  Erweitern Sie **Trusted Platform Module Dienste**.

Die Listen bestimmter Blockierter TPM 1.2-Befehle können direkt an den folgenden Speicherorten bearbeitet werden.

-   Gruppenrichtlinien Liste:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   Lokale Liste:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   Standardliste:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

Unter jedem dieser Registrierungsschlüssel gibt es eine Liste von Registrierungs Werten des REG SZ- \_ Typs. Jeder Wert stellt einen gesperrten TPM-Befehl dar. Jeder Registrierungsschlüssel weist das Feld "Wertname" und das Feld "Wertdaten" auf. Beide Felder ("Wertname" und "Wertdaten") sollten genau mit dem Dezimalwert der zu blockierenden TPM-Befehls Ordinalzahl übereinstimmen.

Die Liste der spezifischen zulässigen TPM 2,0-Befehle kann direkt an folgendem Speicherort bearbeitet werden. Unter dem Registrierungsschlüssel befindet sich eine Liste mit Registrierungs Werten des reg \_ DWORD-Typs. Jeder Wert stellt einen zulässigen TPM 2,0-Befehl dar. Jeder Registrierungs Wert verfügt über einen **Namen** und ein **Wertfeld** . Der **Name** entspricht der hexadezimalen TPM 2,0-Befehls Ordinalzahl, die zulässig sein soll. Der **Wert** hat den Wert 1, wenn der Befehl zulässig ist. Wenn eine Befehls Ordinalzahl nicht vorhanden ist oder den Wert 0 hat, wird der Befehl blockiert.

-   Standardliste:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

Für Windows 8, Windows Server 2012 und höher, bestimmen die Registrierungsschlüssel **blockedcommands** und **AllowedW8Commands** die gesperrten oder zulässigen TPM-Befehle für Administrator Konten. Benutzerkonten enthalten eine Liste der blockierten oder zulässigen TPM-Befehle in den Registrierungs Schlüsseln **blockedusercommands** bzw. **AllowedW8UserCommands** . In Windows 10, Version 1607, wurden neue Registrierungsschlüssel für appcontainer-Anwendungen eingeführt: **blockedappcontainercommands** und **AllowedW8AppContainerCommands**.

 

 




