---
description: Die Windows-Kennwortfilter-DLL Passfilt.dll wird im Sicherheitskontext des lokalen Systemkontos ausgeführt und unterstützt Sie beim Filtern von Domänen- oder lokalen Kontokennwörtern.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installieren und Registrieren einer Kennwortfilter-DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327165"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Installieren und Registrieren einer Kennwortfilter-DLL

Sie können den Windows-Kennwortfilter verwenden, um Domänen- oder lokale Kontokennwörter zu filtern. Um den Kennwortfilter für Domänenkonten zu verwenden, installieren und registrieren Sie die DLL auf jedem Domänencontroller in der Domäne.

Führen Sie die folgenden Schritte aus, um Ihren Kennwortfilter zu installieren. Sie können diese Schritte manuell ausführen oder ein Installationsprogramm schreiben, um diese Schritte auszuführen. Sie müssen Administrator sein oder der Administratorgruppe angehören, um diese Schritte ausführen zu können.

**So installieren und registrieren Sie eine Windows-Kennwortfilter-DLL**

1.  Kopieren Sie die DLL in das Windows-Installationsverzeichnis auf dem Domänencontroller oder lokalen Computer. Bei Standardinstallationen lautet der Standardordner \\ Windows \\ System32. Stellen Sie sicher, dass Sie eine 32-Bit-Kennwortfilter-DLL für 32-Bit-Computer und eine 64-Bit-Kennwortfilter-DLL für 64-Bit-Computer erstellen und sie dann an den entsprechenden Speicherort kopieren.
2.  Aktualisieren Sie den folgenden Systemregistrierungsschlüssel, um den Kennwortfilter zu registrieren:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Wenn der Wert **Benachrichtigungspakete** vom Typ *REG_MULTI_SZ* vorhanden ist, fügen Sie den vorhandenen Wertdaten den Namen Ihrer DLL hinzu. Überschreiben Sie die vorhandenen Werte nicht, und schließen Sie die DLL-Erweiterung nicht ein.

    Wenn der Wert **Benachrichtigungspakete** nicht vorhanden ist, erstellen Sie ihn, geben Sie ihm den *REG_MULTI_SZ* Typ an, und geben Sie dann den Namen der DLL für die Wertdaten an. Schließen Sie die DLL-Erweiterung nicht ein.

    Der Wert **Benachrichtigungspakete** kann mehrere Pakete hinzufügen.

3.  Suchen Sie die Einstellung für die Kennwortkomplexität.

    Klicken Sie in Systemsteuerung auf **Leistung und Wartung**, klicken Sie auf **Verwaltung,** doppelklicken Sie auf **Lokale Sicherheitsrichtlinie,** doppelklicken Sie auf **Kontorichtlinien**, und doppelklicken Sie dann auf **Kennwortrichtlinie.**

4.  Um sowohl den Windows-Standardkennwortfilter als auch den benutzerdefinierten Kennwortfilter zu erzwingen, stellen Sie sicher, dass die Richtlinieneinstellung Kennwörter müssen **Komplexitätsanforderungen** erfüllen aktiviert ist. Deaktivieren Sie andernfalls **die Richtlinieneinstellung Kennwörter müssen Komplexitätsanforderungen** erfüllen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen zur Programmierung von Kennwortfiltern](password-filter-programming-considerations.md)
</dt> <dt>

[Erzwingung und Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Kennwortfilterfunktionen](management-functions.md)
</dt> </dl>

 

 



