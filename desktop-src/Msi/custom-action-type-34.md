---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 34 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Benutzerdefinierter Aktionstyp 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373195"
---
# <a name="custom-action-type-34"></a>Benutzerdefinierter Aktionstyp 34

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde Weitere Informationen finden Sie unter [ausführbare Dateien](executable-files.md).

## <a name="source"></a>`Source`

Die ausführbare Datei wird aus einer Datei generiert. Das Quellfeld der Tabelle " [CustomAction](customaction-table.md) " enthält einen Schlüssel in der [Verzeichnis](directory-table.md) Tabelle. Der Verzeichnis Tabelleneintrag, auf den verwiesen wird, wird verwendet, um den vollständigen Pfad zu einem Arbeitsverzeichnis aufzulösen. Dies ist nicht erforderlich, um den Pfad zu dem Verzeichnis zu sein, das die ausführbare Datei enthält.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                         | Hexadezimal | Decimal |
|-------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypedirectory** | 0x022       | 34      |



 

## <a name="target"></a>Ziel

Die Ziel Spalte der Tabelle [CustomAction](customaction-table.md) enthält den vollständigen Pfad und den Namen der ausführbaren Datei, gefolgt von optionalen Argumenten für die ausführbare Datei. Der vollständige Pfad und Name der ausführbaren Datei ist erforderlich. Anführungszeichen müssen in Bezug auf lange Dateinamen oder-Pfade verwendet werden. Der Wert wird als [formatierter](formatted.md) Text behandelt und kann Verweise auf Eigenschaften, Dateien, Verzeichnisse oder andere formatierte Text Attribute enthalten.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Schließen Sie optionale Flagbits in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben. Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript. Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben. Der Installer interpretiert jeden anderen Rückgabewert als Fehler. Zum Ignorieren von Rückgabe Werten legen Sie das Bitflag " **msidbcustomaction typecontinue** " im type-Feld der Tabelle " [CustomAction](customaction-table.md) " fest.

## <a name="remarks"></a>Bemerkungen

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind. Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm [**zum Erstellen**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) des Prozesses den Prozess, wenn [**die benutzerdefinierte**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Aktion aus dem Installationsskript aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 
