---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 50 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Benutzerdefinierter Aktionstyp 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b17c6b512e53bb085c23f6ad0e8af412f6f9de44da3cc70c7153dbef7fb99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119263250"
---
# <a name="custom-action-type-50"></a>Benutzerdefinierter Aktionstyp 50

Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die über eine Befehlszeile gestartet wurde.

Siehe auch [Ausführbare Dateien.](executable-files.md)

## <a name="source"></a>`Source`

Die ausführbare Datei wird aus einer vorhandenen Datei generiert. Das Feld Quelle der [CustomAction-Tabelle](customaction-table.md) enthält einen Schlüssel zur [Property-Tabelle](property-table.md) für eine Eigenschaft, die den vollständigen Pfad zur ausführbaren Datei enthält.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                        | Hexadezimal | Decimal |
|------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty** | 0x032       | 50      |



 

## <a name="target"></a>Ziel

Die Target -Spalte der [CustomAction-Tabelle](customaction-table.md) enthält die Befehlszeilenzeichenfolge für die ausführbare Datei, die in der Spalte Quelle identifiziert wird.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Rückgabeverarbeitung anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter [Benutzerdefinierte Optionen für die Aktionsrückgabeverarbeitung.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

Benutzerdefinierte Aktionen, bei denen es sich um [ausführbare Dateien](executable-files.md) handelt, müssen für den Erfolg den Wert 0 zurückgeben. Das Installationsprogramm interpretiert alle anderen Rückgabewerte als Fehler. Um Rückgabewerte zu ignorieren, legen Sie das **msidbCustomActionTypeContinue-Bitflag** im Feld Type der CustomAction-Tabelle fest.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, verwendet eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt werden. Wenn es sich auch um eine benutzerdefinierte Aktion mit [verzögerter Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm CreateProcessAsUser oder CreateProcess, um den Prozess zu erstellen, wenn die benutzerdefinierte Aktion aus dem Installationsskript aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



