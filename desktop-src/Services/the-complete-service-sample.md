---
description: Weitere Informationen zu finden Sie unter dem Beispiel für ein umfassendes Dienst
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Das Complete Service-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350384"
---
# <a name="the-complete-service-sample"></a>Das Complete Service-Beispiel

Die Themen in diesem Abschnitt bilden eine umfassende Dienst Stichprobe:

-   [Sample.MC](sample-mc.md) (enthält Fehlermeldungen)
-   [Svc. cpp](svc-cpp.md) (enthält den Dienst Code)
-   [Svcconfig. cpp](svcconfig-cpp.md) (enthält Dienst Konfigurations Code)
-   [Svccontrol. cpp](svccontrol-cpp.md) (enthält Dienst Steuerungs Code)

## <a name="building-the-service"></a>Erstellen des Dienstes

Im folgenden Verfahren wird beschrieben, wie der Dienst erstellt und die Ereignis Nachrichten-DLL registriert wird.

**So erstellen Sie den Dienst und registrieren die Ereignis Nachrichten-dll**

1.  Erstellen Sie die Nachrichten-dll aus Sample.MC, indem Sie die folgenden Schritte ausführen:
    1.  **MC-U Sample.MC**
    2.  **RC-r-Beispiel. RC**
    3.  **Link-dll-NOENTRY -out:sample.dll Sample. res**
2.  Erstellen Sie Svc.exe, SvcConfig.exe und SvcControl.exe aus "svc. cpp", "svcconfig. cpp" und "svccontrol. cpp".
3.  Erstellen Sie den Registrierungsschlüssel **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** , und fügen Sie diesem Schlüssel die folgenden Registrierungs Werte hinzu.

    | Wert                              | type       | BESCHREIBUNG                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *dll- \_ Pfad* | REG- \_ SZ    | Der Pfad zur reinen Ressourcen-DLL, die Zeichen folgen enthält, die der Dienst in das Ereignisprotokoll schreiben kann.               |
    | **Typessupported** = 0x00000007    | REG \_ DWORD | Eine Bitmaske, die die unterstützten Ereignis Typen angibt. Der Wert 0x000000007 gibt an, dass alle Typen unterstützt werden. |

    

     

## <a name="testing-the-service"></a>Testen des Diensts

Im folgenden Verfahren wird beschrieben, wie der-Dienst getestet wird.

**So testen Sie den Dienst**

1.  Starten Sie in der Systemsteuerung die **Dienst** Anwendung. (Verwenden Sie in den folgenden Schritten die Taste F5, um die Anzeige zu aktualisieren, nachdem Sie einen Befehl ausgeführt haben, der die Informationen in der **Dienste** -Anwendung ändert.)
2.  Führen Sie den folgenden Befehl aus, um den Dienst zu installieren:

    **SVC-Installation**

    Der Dienst schreibt "der Dienst wurde erfolgreich installiert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.

    Wenn die Dienst Installation erfolgreich ist, wird der Dienst in der **Dienst** Anwendung angezeigt. Beachten Sie, dass **Name** auf "SvcName" festgelegt ist, **Beschreibung** und **Status** leer sind und **Starttyp** auf "manuell" festgelegt ist.

3.  Führen Sie den folgenden Befehl aus, um den Dienst zu starten:

    **svccontrol-Start SvcName**

    Wenn der Vorgang erfolgreich ist, schreibt das Dienst Steuerungsprogramm "Dienst Start steht aus...". und dann "der Dienst wurde erfolgreich gestartet" in der Konsole. Andernfalls schreibt das Programm eine Fehlermeldung in die Konsole.

    Wenn der Dienst erfolgreich gestartet wird, wird der **Status** auf "gestartet" festgelegt. Der Code in der [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion wird vom SCM ausgeführt. Wenn ein Fehler auftritt, schreibt der Dienst eine Fehlermeldung in das Ereignisprotokoll. Diese Meldung enthält den Namen der Funktion, die fehlgeschlagen ist, und den Fehlercode, der bei einem Fehler zurückgegeben wurde.

4.  Führen Sie den folgenden Befehl aus, um die Dienst Beschreibung zu aktualisieren:

    **svcconfig beschreiben SvcName**

    Das Dienst Konfigurationsprogramm schreibt die "Dienst Beschreibung wurde erfolgreich aktualisiert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.

    Wenn das Update erfolgreich ist, wird die **Beschreibung** auf "This is a Test Description" festgelegt.

5.  Führen Sie den folgenden Befehl aus, um die Dienst Konfiguration abzufragen:

    **svcconfig-Abfrage SvcName**

    Das Dienst Konfigurationsprogramm schreibt die Dienst Konfigurationsinformationen in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.

6.  Führen Sie den folgenden Befehl aus, um die Dienst-DACL zu ändern:

    **svccontrol DACL SvcName**

    Das Dienst Konfigurationsprogramm schreibt die "Dienst-DACL wurde erfolgreich aktualisiert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.

7.  Führen Sie den folgenden Befehl aus, um den Dienst zu deaktivieren:

    **svcconfig "SvcName deaktivieren"**

    Das Dienst Konfigurationsprogramm schreibt "der Dienst wurde erfolgreich deaktiviert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.

    Wenn der Dienst erfolgreich deaktiviert wurde, wird der **Starttyp** auf "deaktiviert" festgelegt.

8.  Führen Sie den folgenden Befehl aus, um den Dienst zu aktivieren:

    **svcconfig SvcName aktivieren**

    Das Dienst Konfigurationsprogramm schreibt "der Dienst wurde erfolgreich aktiviert" in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.

    Wenn der Dienst erfolgreich aktiviert wurde, wird der **Starttyp** auf "manuell" festgelegt.

9.  Führen Sie den folgenden Befehl aus, um den Dienst zu unterbinden:

    **svccontrol stoppt SvcName.**

    Wenn der Vorgang erfolgreich ausgeführt wird, schreibt das Dienst Steuerungsprogramm "Dienst Ende steht aus...". und dann "der Dienst wurde erfolgreich beendet" in der Konsole. Andernfalls schreibt das Programm eine Fehlermeldung in die Konsole.

    Wenn der Dienst erfolgreich beendet wird, ist der **Status** leer.

    Wenn der Dienst nicht beendet werden kann, schreibt das Dienst Steuerungsprogramm eine Fehlermeldung in das Ereignisprotokoll, das den Namen der fehlgeschlagenen Funktion und den Fehlercode enthält, der bei einem Fehler zurückgegeben wurde.

10. Führen Sie den folgenden Befehl aus, um den Dienst zu löschen:

    **svcconfig DELETE SvcName**

    Das Dienst Konfigurationsprogramm schreibt "der Dienst wurde erfolgreich gelöscht" in die Konsole, wenn der Vorgang erfolgreich abgeschlossen wurde, andernfalls wird eine Fehlermeldung angezeigt.

    Wenn der Dienst erfolgreich gelöscht wurde, wird er nicht mehr in der **Dienst** Anwendung angezeigt. (Beachten Sie Folgendes: Wenn Sie versuchen, einen Dienst zu löschen, der nicht beendet wurde, ist der Vorgang erfolgreich, aber der **Starttyp** ist auf "deaktiviert" festgelegt, und der Dienst Eintrag wird beim Neustart des Systems oder beim Beenden des Dienstanbieter mithilfe des Task-Managers gelöscht.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Diensten](using-services.md)
</dt> </dl>

 

 
