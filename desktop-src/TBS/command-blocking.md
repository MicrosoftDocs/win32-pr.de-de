---
title: Befehlsblockierung
description: Um die Integrität von Vorgängen beizubehalten, dürfen bestimmte TPM-Befehle nicht von Software auf der Plattform ausgeführt werden.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a157a3c53c35bb6baba86e416b872887ab0aed14bf200f1ce6a234a2a354e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880740"
---
# <a name="command-blocking"></a>Befehlsblockierung

Um die Integrität von Vorgängen beizubehalten, dürfen bestimmte TPM-Befehle nicht von Software auf der Plattform ausgeführt werden. Einige Befehle werden z. B. nur von Systemsoftware ausgeführt. Wenn der TBS einen Befehl blockiert, wird ggf. ein Fehler zurückgegeben. Standardmäßig blockiert der TBS Befehle, die sich auf den Datenschutz, die Sicherheit und die Stabilität des Systems auswirken können. Der TBS geht auch davon aus, dass andere Teile des Softwarestapels den Zugriff auf bestimmte Befehle auf autorisierte Entitäten einschränken können.

Für TPM-Befehle der Version 1.2 gibt es drei Listen blockierter Befehle: eine Liste, die von einer Gruppenrichtlinie gesteuert wird, eine Liste, die von lokalen Administratoren gesteuert wird, und eine Standardliste. Ein TPM-Befehl wird blockiert, wenn er sich in einer der Listen befindet. Es gibt jedoch Gruppenrichtlinienflags, mit denen tbs die lokale Liste und die Standardliste ignorieren kann. Die Gruppenrichtlinienflags können direkt bearbeitet oder über die Gruppenrichtlinienobjekt-Editor aufgerufen werden.

> [!Note]  
> Die Liste der lokal blockierten Befehle wird nach einem Upgrade auf das Betriebssystem nicht beibehalten. Befehle, die in der liste Gruppenrichtlinie blockiert sind, werden beibehalten.

 

Bei TPM-Befehlen der Version 2.0 wird die Logik für die Blockierung umgekehrt. Es wird eine Liste zulässiger Befehle verwendet. Diese Logik blockiert automatisch Befehle, die beim ersten Erstellen der Liste nicht bekannt waren. Wenn Befehle der TPM-Spezifikation hinzugefügt werden, nachdem eine Version von Windows ausgeliefert wurde, werden diese neuen Befehle automatisch blockiert. Nur ein Update der Registrierung fügt diese neuen Befehle der Liste der zulässigen Befehle hinzu.

Ab Windows 10 1809 (Windows Server 2019) können zulässige TPM 2.0-Befehle nicht mehr über Registrierungseinstellungen bearbeitet werden. Für diese Windows 10 Versionen werden die zulässigen TPM 2.0-Befehle im TPM-Treiber behoben. TPM 1.2-Befehle können weiterhin blockiert und durch Registrierungsänderungen entsperrt werden. 

## <a name="direct-registry-access"></a>Direkter Registrierungszugriff

Die Gruppenrichtlinie Flags befinden sich unter dem Registrierungsschlüssel **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Tpm** \\ **BlockedCommands**.

Um zu bestimmen, welche Listen zum Blockieren von TPM-Befehlen verwendet werden sollen, gibt es zwei **DWORD-Werte,** die als boolesche Flags verwendet werden:

-   "IgnoreDefaultList"

    Wenn festgelegt (der Wert ist vorhanden und ungleich 0 (null) ist, ignoriert der TBS die Standardliste blockierter Befehle.

-   "IgnoreLocalList"

    Wenn festgelegt ist (der Wert ist vorhanden und ungleich 0 (null) ist, ignoriert der TBS die Lokale Liste blockierter Befehle.

## <a name="group-policy-object-editor"></a>Gruppenrichtlinienobjekt-Editor

**So greifen Sie auf den Gruppenrichtlinie Objekt-Editor zu**

1.  Klicken Sie auf **Start**.
2.  Klicken Sie auf **Ausführen**.
3.  Geben Sie **gpedit.msc** im Feld **Öffnen** ein. Klicken Sie auf **OK**. Der Gruppenrichtlinie Objekt-Editor wird geöffnet.
4.  Erweitern Sie **Computerkonfiguration.**
5.  Erweitern Sie **Administrative Vorlagen**.
6.  Erweitern Sie **System**.
7.  Erweitern Sie **Trusted Platform Module Services**.

Die Listen mit bestimmten blockierten TPM1.2-Befehlen können direkt an den folgenden Stellen bearbeitet werden.

-   Gruppenrichtlinienliste:

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

Unter jedem dieser Registrierungsschlüssel befindet sich eine Liste mit Registrierungswerten vom Typ REG \_ SZ. Jeder Wert stellt einen blockierten TPM-Befehl dar. Jeder Registrierungsschlüssel verfügt über das Feld "Wertname" und das Feld "Wertdaten". Beide Felder ("Wertname" und "Wertdaten") sollten genau mit dem Dezimalwert der zu blockierenden TPM-Befehls-Ordnungszahl übereinstimmen.

Die Liste der spezifischen zulässigen TPM 2.0-Befehle kann direkt am folgenden Speicherort bearbeitet werden. Unter dem Registrierungsschlüssel befindet sich eine Liste der Registrierungswerte vom Typ REG \_ DWORD. Jeder Wert stellt einen zulässigen TPM 2.0-Befehl dar. Jeder Registrierungswert verfügt über einen **Namen** und ein **Wertfeld.** Der **Name** entspricht der hexadezimalen TPM 2.0-Befehls-Ordnungszahl, die zugelassen werden soll. Der **Wert** hat den Wert 1, wenn der Befehl zulässig ist. Wenn eine Befehls-Ordnungszahl nicht vorhanden ist oder den Wert 0 hat, wird der Befehl blockiert.

-   Standardliste:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

Für Windows 8 Windows Server 2012 und höher bestimmen die Registrierungsschlüssel **BlockedCommands** bzw. **AllowedW8Commands** die blockierten oder zulässigen TPM-Befehle für Administratorkonten. Benutzerkonten verfügen über eine Liste blockierter oder zulässiger TPM-Befehle in den **Registrierungsschlüsseln BlockedUserCommands** bzw. **AllowedW8UserCommands.** In Windows 10 Version 1607 wurden neue Registrierungsschlüssel für AppContainer-Anwendungen eingeführt: **BlockedAppContainerCommands** und **AllowedW8AppContainerCommands**.

 

 




