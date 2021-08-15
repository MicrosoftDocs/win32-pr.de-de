---
description: 'Dieser Abschnitt zu Dateitypen und Dateizuordnungen ist wie folgt organisiert:'
ms.assetid: 45d8b729-1e9d-40c0-8306-9a475262ac40
title: Dateitypen und Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd096aa81970ee1baff27ae87368d26827fd8d0b46f6bdd7c69190d5ddfc56f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459193"
---
# <a name="file-types-and-file-associations"></a>Dateitypen und Dateizuordnungen

Dieser Abschnitt zu Dateitypen und Dateizuordnungen ist wie folgt organisiert:

-   [Anwendungsregistrierung](app-registration.md)
-   [Dateitypen](fa-file-types.md)
-   [Auswählen einer Dateityperweiterung](how-to-choose-a-file-type-extension.md)
-   [Definieren von Dateitypattributen](how-to-define-file-type-attributes.md)
-   [Einschließen einer Anwendung in das dialogfeld "Öffnen mit"](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Ausschließen einer Anwendung aus dem dialogfeld "Öffnen mit" für nicht zugeordnete Dateitypen](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)
-   [Funktionsweise von Dateizuordnungen](fa-how-work.md)
-   [Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
-   [Registrieren von benutzerdefinierten Eigenschaften und Layouts für Ihren Dateityp](how-to-register-custom-properties-and-layout-for-your-file-type.md)
-   [Dateitypüberprüfung](file-type-verifier.md)
-   [Verwenden der Dateitypüberprüfung](how-to-use-the-file-type-verifier.md)
-   [Dateityphandler](fa-file-extensions.md)
-   [Programmgesteuerte Bezeichner](fa-progids.md)
-   [Registrieren eines Dateityps für eine neue Anwendung](how-to-register-a-file-type-for-a-new-application.md)
-   [Wahrgenommene Typen](fa-perceivedtypes.md)
-   [Zuordnungsarrays](fa-associationarray.md)

## <a name="additional-resources"></a>Weitere Ressourcen

-   Set Program Access and Computer Defaults (SPAD) ist ein Windows Systemsteuerung mit dem Benutzer mit Administratorrechten einen Computerstandard festlegen und eine Anwendung ausblenden oder einblenden können. Medien-, E-Mail-, Browser-, Messenger- und Java-Anwendungen sind Beispiele für Anwendungen, die in SPAD registriert sind. Set Your Default Programs (SYDP) ist eine Windows Systemsteuerung, die mit eingeschränkten Berechtigungen funktioniert und Benutzern ermöglicht, einen Benutzerstandard festzulegen. Jede Anwendung kann sich in SYDP registrieren. Informationen zur Registrierung von SPAD- und SYDP-Anwendungen finden Sie unter [Richtlinien für Dateizuordnungen und Standardprogramme](appguide-fa-defpro.md)und Festlegen von [Programmzugriff und Computerstandard (SPAD).](cpl-setprogramaccess.md)
-   Verwandte konzeptuelle Hintergrundinformationen finden Sie unter [Übersicht über Verben und Dateizuordnungen.](fa-verbs.md)
-   Informationen zum Erstellen eines Shell-Datenspeichers finden Sie unter [Implementieren der grundlegenden Ordnerobjektschnittstellen.](nse-implement.md)

Die zugehörige Referenzdokumentation finden Sie in den folgenden Themen:

-   Informationen zum Ausführen eines Verbs für ein Shellelement finden Sie in der [**InvokeVerb-Methode.**](folderitem-invokeverb.md)
-   Informationen zum Abrufen einer Auflistung von Verben, die für ein Shellelement ausgeführt werden können, finden Sie in der [**Verbs-Methode.**](folderitem-verbs.md)
-   Informationen zum Ausführen eines Vorgangs für eine angegebene Datei finden Sie unter den [**ShellExecute-**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) oder [**ShellExecuteEx-Funktionen.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)
-   Eine Liste der standardmäßig erkannten Typen finden Sie in der [**PERCEIVED-Enumeration.**](/windows/win32/api/shtypes/ne-shtypes-perceived)
-   Informationen zum Abrufen des wahrgenommenen Typs einer Datei basierend auf ihrer Erweiterung finden Sie in der [**AssocGetPerceivedType-Funktion.**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)

 

 



