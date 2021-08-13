---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 22 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Benutzerdefinierter Aktionstyp 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe14690ec1d966abfe1ead0b7856360270570f30e2aaf2e93ea81181962ec8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637904"
---
# <a name="custom-action-type-22"></a>Benutzerdefinierter Aktionstyp 22

Diese benutzerdefinierte Aktion ist in VBScript geschrieben. Siehe auch [Skripts](scripts.md).

## <a name="source"></a>`Source`

Das Skript wird mit der Anwendung während der aktuellen Sitzung installiert. Das Feld Quelle der [Tabelle CustomAction](customaction-table.md) enthält einen Schlüssel für die [Dateitabelle](file-table.md). Der Speicherort des benutzerdefinierten Aktionscodes wird durch die Auflösung des Zielpfads für diese Datei bestimmt. daher muss diese benutzerdefinierte Aktion aufgerufen werden, nachdem die Datei installiert und entfernt wurde.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                               | Hexadezimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile** | 0x016       | 22      |



 

Windows Das Installationsprogramm kann benutzerdefinierte 64-Bit-Aktionen unter 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript-Bit** in seinem numerischen Typ enthalten. Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md) Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                      | Hexadezimal | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript** | 0x0001016   | 4118    |



 

## <a name="target"></a>Ziel

Das Feld Target der [Tabelle CustomAction](customaction-table.md) enthält eine optionale Skriptfunktion. Die Verarbeitung sendet zuerst das Skript zur Analyse und ruft dann die optionale Skriptfunktion auf.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Rückgabeverarbeitung anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter [Benutzerdefinierte Optionen für die Aktionsrückgabeverarbeitung.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

In Skript geschriebene optionale Funktionen müssen einen der unter [Rückgabewerte von JScript und benutzerdefinierten VBScript-Aktionen](return-values-of-jscript-and-vbscript-custom-actions.md)beschriebenen Werte zurückgeben.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, erfordert die Installation des [**Sitzungsobjekts**](session-object.md). Dies ist vom Typ **Sitzungsobjekt,** und das Installationsprogramm fügt es mit dem Namen "Session" an das Skript an. Da das **Session-Objekt** während eines Installationsrollbacks möglicherweise nicht vorhanden ist, muss eine im Skript geschriebene verzögerte benutzerdefinierte Aktion eine der Methoden oder Eigenschaften des **Session-Objekts** verwenden, die im Abschnitt [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben sind, um den Kontext abzurufen.

Benutzerdefinierte Aktionen, die auf eine installierte Datei als Quelle verweisen, z. B. benutzerdefinierter Aktionstyp 22 (VBcript), müssen die folgenden Sequenzeinschränkungen einhalten:

-   Die benutzerdefinierte Aktion muss nach der [CostFinalize-Aktion](costfinalize-action.md)sequenziert werden. Dies ist so, dass die benutzerdefinierte Aktion den Pfad auflösen kann, der zum Suchen der Quelldatei mit VBScript erforderlich ist.
-   Wenn die Quelldatei noch nicht auf dem Computer installiert ist, müssen verzögerte (skriptbasierte) benutzerdefinierte Aktionen dieses Typs nach der [InstallFiles-Aktion](installfiles-action.md)sequenziert werden.
-   Wenn die Quelldatei nicht bereits auf dem Computer installiert ist, müssen nicht verzögerte benutzerdefinierte Aktionen dieses Typs nach der [InstallFinalize-Aktion](installfinalize-action.md)sequenziert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



