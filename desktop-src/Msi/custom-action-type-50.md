---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 50 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Benutzerdefinierter Aktionstyp 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362393"
---
# <a name="custom-action-type-50"></a>Benutzerdefinierter Aktionstyp 50

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde

Siehe auch [ausführbare Dateien](executable-files.md).

## <a name="source"></a>`Source`

Die ausführbare Datei wird aus einer vorhandenen Datei generiert. Das Quellfeld der [Tabelle CustomAction](customaction-table.md) enthält einen Schlüssel für die [Eigenschaften Tabelle](property-table.md) für eine Eigenschaft, die den vollständigen Pfad zur ausführbaren Datei enthält.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                        | Hexadezimal | Decimal |
|------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypeproperty** | 0x032       | 50      |



 

## <a name="target"></a>Ziel

Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält die Befehlszeilen Zeichenfolge für die in der Spalte Quelle identifizierte ausführbare Datei.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben. Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript. Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben. Der Installer interpretiert jeden anderen Rückgabewert als Fehler. Zum Ignorieren von Rückgabe Werten legen Sie das Bitflag " **msidbcustomaction typecontinue** " im type-Feld der Tabelle "CustomAction" fest.

## <a name="remarks"></a>Bemerkungen

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind. Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm zum Erstellen des Prozesses den Prozess, wenn die benutzerdefinierte Aktion aus dem Installationsskript aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



