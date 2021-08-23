---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 54 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Benutzerdefinierter Aktionstyp 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c206eec715982e1fd23978a04393b6036f77abf4c18807d2e5d43d27755640c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520080"
---
# <a name="custom-action-type-54"></a>Benutzerdefinierter Aktionstyp 54

Diese benutzerdefinierte Aktion ist in VBScript geschrieben. Siehe auch [Skripts](scripts.md).

## <a name="source"></a>Quelle

Das Feld Quelle der [CustomAction-Tabelle](customaction-table.md) enthält einen Eigenschaftennamen oder einen Schlüssel für die [Property-Tabelle](property-table.md) für eine Eigenschaft, die den Skripttext enthält.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                             | Hexadezimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty** | 0x036       | 54      |



 

Windows Das Installationsprogramm kann benutzerdefinierte 64-Bit-Aktionen unter 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript-Bit** in seinem numerischen Typ enthalten. Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md) Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                    | Hexadezimal | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript** | 0x0001036   | 4150    |



 

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

Eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, erfordert das [**Session-Objekt**](session-object.md) installieren. Das Installationsprogramm fügt das **Sitzungsobjekt** mit dem Namen *Sitzung* an das Skript an. Da das **Session-Objekt** während eines Installationsrollbacks möglicherweise nicht vorhanden ist, muss eine im Skript geschriebene verzögerte benutzerdefinierte Aktion eine der Methoden oder Eigenschaften des **Session-Objekts** verwenden, die im Abschnitt [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben sind, um den Kontext abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



