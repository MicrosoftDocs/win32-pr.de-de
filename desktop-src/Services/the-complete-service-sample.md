---
description: 'Weitere Informationen zu: Beispiel für den vollständigen Dienst'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Beispiel für den vollständigen Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1f3f5fc0fb59342841a9d1f1280475ace12c54998d59e5f36a19557f0ccc5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888331"
---
# <a name="the-complete-service-sample"></a>Beispiel für den vollständigen Dienst

Die Themen in diesem Abschnitt bilden ein vollständiges Dienstbeispiel:

-   [Sample.mc](sample-mc.md) (enthält Fehlermeldungen)
-   [Svc.cpp](svc-cpp.md) (enthält den Dienstcode)
-   [SvcConfig.cpp](svcconfig-cpp.md) (enthält Dienstkonfigurationscode)
-   [SvcControl.cpp](svccontrol-cpp.md) (enthält Dienststeuerungscode)

## <a name="building-the-service"></a>Erstellen des Dienstes

Im folgenden Verfahren wird beschrieben, wie der Dienst erstellt und die Ereignismeldungs-DLL registriert wird.

**So erstellen Sie den Dienst und registrieren die Ereignismeldungs-DLL**

1.  Erstellen Sie die Nachrichten-DLL aus Sample.mc, indem Sie die folgenden Schritte ausführen:
    1.  **mc -U sample.mc**
    2.  **rc -r sample.rc**
    3.  **link -dll -noentry -out:sample.dll sample.res**
2.  Erstellen Sie Svc.exe, SvcConfig.exe und SvcControl.exe aus Svc.cpp, SvcConfig.cpp bzw. SvcControl.cpp.
3.  Erstellen Sie den Registrierungsschlüssel **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services \\ EventLog Application \\ \\ SvcName,** und fügen Sie diesem Schlüssel die folgenden Registrierungswerte hinzu.

    | Wert                              | type       | BESCHREIBUNG                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *\_ DLL-Pfad* | REG \_ SZ    | Der Pfad zur reinen Ressourcen-DLL, die Zeichenfolgen enthält, die der Dienst in das Ereignisprotokoll schreiben kann.               |
    | **TypesSupported** = 0x00000007    | REG \_ DWORD | Eine Bitmaske, die die unterstützten Ereignistypen angibt. Der Wert 0x000000007 gibt an, dass alle Typen unterstützt werden. |

    

     

## <a name="testing-the-service"></a>Testen des Diensts

Im folgenden Verfahren wird beschrieben, wie der Dienst getestet wird.

**So testen Sie den Dienst**

1.  Starten Sie in Systemsteuerung die **Anwendung Dienste.** (Verwenden Sie in den folgenden Schritten die F5-Taste, um die Anzeige zu aktualisieren, nachdem Sie einen Befehl ausgeführt haben, der die Informationen in der **Dienstanwendung** ändert.)
2.  Führen Sie den folgenden Befehl aus, um den Dienst zu installieren:

    **svc install**

    Der Dienst schreibt "Dienst erfolgreich installiert" in die Konsole, wenn der Vorgang erfolgreich war, oder andernfalls eine Fehlermeldung.

    Wenn die Dienstinstallation erfolgreich ist, wird der Dienst in der **Anwendung Dienste** angezeigt. Beachten Sie, dass **Name** auf "SvcName", **Beschreibung** und **Status** leer und **Starttyp** auf "Manuell" festgelegt ist.

3.  Führen Sie den folgenden Befehl aus, um den Dienst zu starten:

    **svccontrol start SvcName**

    Wenn der Vorgang erfolgreich ist, schreibt das Dienststeuerungsprogramm "Dienststart ausstehend..." und dann "Dienst wurde erfolgreich gestartet" zur Konsole. Andernfalls schreibt das Programm eine Fehlermeldung in die Konsole.

    Wenn der Dienst erfolgreich gestartet wird, wird **der Status** auf "Gestartet" festgelegt. Der Code in der [*ServiceMain-Funktion*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) wird vom SCM ausgeführt. Wenn ein Fehler auftritt, schreibt der Dienst eine Fehlermeldung in das Ereignisprotokoll. Diese Meldung enthält den Namen der fehlerhaften Funktion und den Fehlercode, der bei einem Fehler zurückgegeben wurde.

4.  Führen Sie den folgenden Befehl aus, um die Dienstbeschreibung zu aktualisieren:

    **svcconfig describe SvcName**

    Das Dienstkonfigurationsprogramm schreibt "Dienstbeschreibung wurde erfolgreich aktualisiert" in die Konsole, wenn der Vorgang erfolgreich war, oder andernfalls eine Fehlermeldung.

    Wenn das Update erfolgreich ist, wird **Description** auf "This is a test description" (Dies ist eine Testbeschreibung) festgelegt.

5.  Führen Sie den folgenden Befehl aus, um die Dienstkonfiguration abzufragen:

    **svcconfig query SvcName**

    Das Dienstkonfigurationsprogramm schreibt die Dienstkonfigurationsinformationen in die Konsole, wenn der Vorgang erfolgreich ist, oder andernfalls eine Fehlermeldung.

6.  Führen Sie den folgenden Befehl aus, um die Dienst-DACL zu ändern:

    **svccontrol dacl SvcName**

    Das Dienstkonfigurationsprogramm schreibt "Service DACL updated successfully" (Dienst-DACL wurde erfolgreich aktualisiert) in die Konsole, wenn der Vorgang erfolgreich war, oder andernfalls eine Fehlermeldung.

7.  Führen Sie den folgenden Befehl aus, um den Dienst zu deaktivieren:

    **svcconfig disable SvcName**

    Das Dienstkonfigurationsprogramm schreibt "Dienst erfolgreich deaktiviert" in die Konsole, wenn der Vorgang erfolgreich war, oder andernfalls eine Fehlermeldung.

    Wenn der Dienst erfolgreich deaktiviert wurde, wird **der Starttyp** auf "Deaktiviert" festgelegt.

8.  Führen Sie den folgenden Befehl aus, um den Dienst zu aktivieren:

    **svcconfig enable SvcName**

    Das Dienstkonfigurationsprogramm schreibt "Dienst erfolgreich aktiviert" in die Konsole, wenn der Vorgang erfolgreich war, oder andernfalls eine Fehlermeldung.

    Wenn der Dienst erfolgreich aktiviert wurde, wird **der Starttyp** auf "Manuell" festgelegt.

9.  Führen Sie den folgenden Befehl aus, um den Dienst zu beenden:

    **svccontrol stop SvcName**

    Wenn der Vorgang erfolgreich ist, schreibt das Dienststeuerungsprogramm "Service stop pending..." (Dienst beendet ausstehend...) und dann "Dienst wurde erfolgreich beendet" an die Konsole. Andernfalls schreibt das Programm eine Fehlermeldung in die Konsole.

    Wenn der Dienst erfolgreich beendet wird, ist **der Status** leer.

    Wenn der Dienst nicht beendet werden kann, schreibt das Dienststeuerungsprogramm eine Fehlermeldung in das Ereignisprotokoll, die den Namen der fehlerhaften Funktion und den Fehlercode enthält, der bei einem Fehler zurückgegeben wurde.

10. Führen Sie den folgenden Befehl aus, um den Dienst zu löschen:

    **svcconfig delete SvcName**

    Das Dienstkonfigurationsprogramm schreibt "Dienst wurde erfolgreich gelöscht" in die Konsole, wenn der Vorgang erfolgreich war, oder andernfalls eine Fehlermeldung.

    Wenn der Dienst erfolgreich gelöscht wurde, wird er nicht mehr in der **Anwendung Dienste** angezeigt. (Beachten Sie Folgendes: Wenn Sie versuchen, einen Dienst zu löschen, der nicht beendet wurde, ist der Vorgang erfolgreich, der **Starttyp** ist jedoch auf "Deaktiviert" festgelegt, und der Diensteintrag wird beim Systemneustart oder beim Beenden des Diensts mithilfe von Task-Manager gelöscht.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Diensten](using-services.md)
</dt> </dl>

 

 
