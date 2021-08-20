---
description: Die Windows Kennwortfilter-DLL, Passfilt.dll, wird im Sicherheitskontext des lokalen Systemkontos ausgeführt und unterstützt Sie beim Filtern von Domänen- oder lokalen Kontokennwörtern.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installieren und Registrieren einer Kennwortfilter-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3cb74571748c38bdfe5a80282e640c13595806c6b7b87b33d9608e420576d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969316"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Installieren und Registrieren einer Kennwortfilter-DLL

Sie können den Windows Kennwortfilter verwenden, um Domänen- oder lokale Kontokennwörter zu filtern. Um den Kennwortfilter für Domänenkonten zu verwenden, installieren und registrieren Sie die DLL auf jedem Domänencontroller in der Domäne.

Führen Sie die folgenden Schritte aus, um Ihren Kennwortfilter zu installieren. Sie können diese Schritte manuell ausführen, oder Sie können ein Installationsprogramm schreiben, um diese Schritte auszuführen. Sie müssen Administrator sein oder der Administratorgruppe angehören, um diese Schritte ausführen zu können.

**So installieren und registrieren Sie eine Windows Kennwortfilter-DLL**

1.  Kopieren Sie die DLL in das Windows Installationsverzeichnis auf dem Domänencontroller oder dem lokalen Computer. Bei Standardinstallationen ist der Standardordner \\ Windows \\ System32. Stellen Sie sicher, dass Sie eine 32-Bit-Kennwortfilter-DLL für 32-Bit-Computer und eine 64-Bit-Kennwortfilter-DLL für 64-Bit-Computer erstellen und sie dann an den entsprechenden Speicherort kopieren.
2.  Aktualisieren Sie den folgenden Systemregistrierungsschlüssel, um den Kennwortfilter zu registrieren:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Wenn der Wert **Benachrichtigungspakete** vom Typ *REG_MULTI_SZ* vorhanden ist, fügen Sie den vorhandenen Wertdaten den Namen Ihrer DLL hinzu. Überschreiben Sie die vorhandenen Werte nicht, und schließen Sie die erweiterung .dll nicht ein.

    Wenn der Wert **Benachrichtigungspakete** nicht vorhanden ist, erstellen Sie ihn, geben Sie ihm den *REG_MULTI_SZ* Typ an, und geben Sie dann den Namen der DLL für die Wertdaten an. Schließen Sie die erweiterung .dll nicht ein.

    Der Wert **Benachrichtigungspakete** kann mehrere Pakete hinzufügen.

3.  Suchen Sie nach der Einstellung für die Kennwortkomplexität.

    Klicken Sie in Systemsteuerung auf **Leistung und Wartung**, klicken Sie auf **Verwaltung**, doppelklicken Sie auf **Lokale Sicherheitsrichtlinie**, doppelklicken Sie auf **Kontorichtlinien**, und doppelklicken Sie dann auf **Kennwortrichtlinie**.

4.  Um sowohl den Standard-Windows Kennwortfilter als auch den benutzerdefinierten Kennwortfilter zu erzwingen, stellen Sie sicher, dass die Richtlinieneinstellung **Kennwörter muss Komplexitätsanforderungen erfüllen** aktiviert ist. Deaktivieren Sie andernfalls die Richtlinieneinstellung **Kennwörter müssen Komplexitätsanforderungen erfüllen.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen zur Programmierung von Kennwortfiltern](password-filter-programming-considerations.md)
</dt> <dt>

[Sichere Kennworterzwingung und Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Kennwortfilterfunktionen](management-functions.md)
</dt> </dl>

 

 



