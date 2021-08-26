---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 34 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Benutzerdefinierter Aktionstyp 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4173633e7912897a3327d6d4c9c556d33f38bbd7f45cca6d4a1d96ef916b08ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077940"
---
# <a name="custom-action-type-34"></a>Benutzerdefinierter Aktionstyp 34

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die über eine Befehlszeile gestartet wurde. Weitere Informationen finden Sie unter [Ausführbare Dateien.](executable-files.md)

## <a name="source"></a>Quelle

Die ausführbare Datei wird aus einer Datei generiert. Das Feld Quelle der [Tabelle CustomAction](customaction-table.md) enthält einen Schlüssel in der [Directory-Tabelle.](directory-table.md) Der Verzeichnistabelleneintrag, auf den verwiesen wird, wird verwendet, um den vollständigen Pfad zu einem Arbeitsverzeichnis aufzulösen. Dies muss nicht der Pfad zum Verzeichnis sein, das die ausführbare Datei enthält.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                         | Hexadezimal | Decimal |
|-------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory** | 0x022       | 34      |



 

## <a name="target"></a>Ziel

Die Spalte Target der [Tabelle CustomAction](customaction-table.md) enthält den vollständigen Pfad und Namen der ausführbaren Datei, gefolgt von optionalen Argumenten für die ausführbare Datei. Der vollständige Pfad und Name der ausführbaren Datei ist erforderlich. Anführungszeichen müssen für lange Dateinamen oder Pfade verwendet werden. Der Wert wird als [formatierter](formatted.md) Text behandelt und kann Verweise auf Eigenschaften, Dateien, Verzeichnisse oder andere formatierte Textattribute enthalten.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Rückgabeverarbeitung anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter [Benutzerdefinierte Optionen für die Aktionsrückgabeverarbeitung.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, bei denen es sich um [ausführbare Dateien](executable-files.md) handelt, müssen für den Erfolg den Wert 0 zurückgeben. Das Installationsprogramm interpretiert alle anderen Rückgabewerte als Fehler. Um Rückgabewerte zu ignorieren, legen Sie das **msidbCustomActionTypeContinue-Bitflag** im Feld Type der [CustomAction-Tabelle](customaction-table.md) fest.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, verwendet eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt werden. Wenn es sich auch um eine [benutzerdefinierte Aktion](deferred-execution-custom-actions.md)mit verzögerter Ausführung handelt, verwendet das Installationsprogramm [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) oder [**CreateProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) um den Prozess zu erstellen, wenn die benutzerdefinierte Aktion aus dem Installationsskript aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 
