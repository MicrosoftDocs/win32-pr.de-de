---
description: 'Dieser Abschnitt zu Dateitypen und Dateizuordnungen ist wie folgt organisiert:'
ms.assetid: 45d8b729-1e9d-40c0-8306-9a475262ac40
title: Dateitypen und Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf84bbf44475d32768d2359d3723952ada843c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215959"
---
# <a name="file-types-and-file-associations"></a>Dateitypen und Dateizuordnungen

Dieser Abschnitt zu Dateitypen und Dateizuordnungen ist wie folgt organisiert:

-   [Anwendungs Registrierung](app-registration.md)
-   [Dateitypen](fa-file-types.md)
-   [Vorgehensweise beim Auswählen einer Dateityp Erweiterung](how-to-choose-a-file-type-extension.md)
-   [Definieren von Dateityp Attributen](how-to-define-file-type-attributes.md)
-   [Einschließen einer Anwendung im Dialog Feld "Öffnen mit"](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Ausschließen einer Anwendung aus dem Dialog Feld "Öffnen mit" für nicht zugeordnete Dateitypen](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)
-   [Funktionsweise von Dateizuordnungen](fa-how-work.md)
-   [Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
-   [Registrieren von benutzerdefinierten Eigenschaften und Layouts für den Dateityp](how-to-register-custom-properties-and-layout-for-your-file-type.md)
-   [Dateityp Überprüfung](file-type-verifier.md)
-   [Verwenden des Dateityp-verifizierers](how-to-use-the-file-type-verifier.md)
-   [Dateityp Handler](fa-file-extensions.md)
-   [Programmgesteuerte Bezeichner](fa-progids.md)
-   [Registrieren eines Dateityps für eine neue Anwendung](how-to-register-a-file-type-for-a-new-application.md)
-   [Wahrgenommene Typen](fa-perceivedtypes.md)
-   [Zuordnungs Arrays](fa-associationarray.md)

## <a name="additional-resources"></a>Weitere Ressourcen

-   Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD) ist eine Windows-Systemsteuerung, die Benutzern mit Administratorrechten das Festlegen eines Computers als Standard und das Ausblenden oder Anzeigen einer Anwendung ermöglicht. Medien, e-Mail, Browser, Messenger und Java-Anwendungen sind Beispiele für Anwendungen, die in SPAD registriert sind. Festlegen der Standardprogramme (SYDP) ist eine Windows-Systemsteuerung, die mit eingeschränkten Berechtigungen funktioniert und es Benutzern ermöglicht, einen Benutzer Standardwert festzulegen. Jede Anwendung kann in SYDP registriert werden. Informationen zur Registrierung von SPAD-und SYDP-Anwendungen finden Sie unter [Richtlinien für Dateizuordnungen und Standardprogramme](appguide-fa-defpro.md)und [Festlegen des Programm Zugriffs und der Computer Standards (SPAD)](cpl-setprogramaccess.md).
-   Verwandte konzeptionelle Hintergrundinformationen finden Sie unter [Übersicht über Verben und Dateizuordnungen](fa-verbs.md).
-   Informationen zum Erstellen eines Shell-Datenspeicher finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](nse-implement.md).

Weitere Informationen zur zugehörigen Referenz Dokumentation finden Sie in den folgenden Themen:

-   Informationen zum Ausführen eines Verbs für ein shellelement finden Sie unter der [**invokeverb**](folderitem-invokeverb.md) -Methode.
-   Weitere Informationen zum Abrufen einer Auflistung von Verben, die für ein shellelement ausgeführt werden können, finden Sie in der [**Verbs**](folderitem-verbs.md) -Methode.
-   Informationen zum Ausführen eines Vorgangs für eine angegebene Datei finden Sie unter den Funktionen [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .
-   Eine Liste der erkannten Standardtypen finden Sie unter der [**wahrgenommenen**](/windows/win32/api/shtypes/ne-shtypes-perceived) Enumeration.
-   Informationen zum Abrufen des wahrgenommenen Datentyps einer Datei anhand ihrer Erweiterung finden Sie unter der Funktion " [**assocgetwahrnehmvedtype**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) ".

 

 



