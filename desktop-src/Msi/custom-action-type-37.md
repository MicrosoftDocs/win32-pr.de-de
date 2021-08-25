---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 37 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Benutzerdefinierter Aktionstyp 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1595279d2c8f66e1b899ad88ad6a9d5c164c2727b5c905ce66700479ed32446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996819"
---
# <a name="custom-action-type-37"></a>Benutzerdefinierter Aktionstyp 37

Diese benutzerdefinierte Aktion wird in JScript geschrieben, z. B. ECMA 262. Windows Das Installationsprogramm unterstützt JScript 1.0 nicht. Weitere Informationen finden Sie unter [Skripts](scripts.md).

## <a name="source"></a>Quelle

Das Feld Source der [CustomAction-Tabelle enthält](customaction-table.md) den NULL-Wert. Der Skriptcode für die benutzerdefinierte Aktion wird als Zeichenfolge aus literalem Skripttext im Feld Ziel gespeichert.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                             | Hexadezimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory** | 0x025       | 37      |



 

Windows Das Installationsprogramm kann benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **bit msidbCustomActionType64BitScript** in seinem numerischen Typ enthalten. Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md) Fügen Sie den folgenden Wert in die Spalte Typ der [CustomAction-Tabelle](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                    | Hexadezimal | Decimal |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001025   | 4133    |



 

## <a name="target"></a>Ziel

Das Feld Target der [CustomAction-Tabelle enthält](customaction-table.md) den Skriptcode für die benutzerdefinierte Aktion als Zeichenfolge mit literalem Skripttext.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Rückgabeverarbeitungsoptionen anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter Rückgabeverarbeitungsoptionen [für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung benutzerdefinierter Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Benutzerdefinierte Aktionsausführungsplanung.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Schließen Sie optionale Flagbits in die Spalte Typ der [CustomAction-Tabelle ein,](customaction-table.md) um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Rückgabewerte

Dieser benutzerdefinierte Aktionstyp gibt immer erfolgreich zurück.

## <a name="remarks"></a>Hinweise

Für eine benutzerdefinierte Aktion, die in JScript ODER VBScript geschrieben ist, ist das [**Session-Installationsobjekt**](session-object.md) erforderlich. Das Installationsprogramm hängt das **Sitzungsobjekt** mit dem Namen "Session" an das Skript an. Da das **Session-Objekt** während eines Installationsrollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben wurde, eine der Methoden oder Eigenschaften des **Session-Objekts** verwenden, die im Abschnitt [Abrufen](obtaining-context-information-for-deferred-execution-custom-actions.md) von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung beschrieben sind, um den Kontext abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



