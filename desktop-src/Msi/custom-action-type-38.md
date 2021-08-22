---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 38 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Benutzerdefinierter Aktionstyp 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361da558a6b1cf9d483d5cdb84d3a4290f9d25fb88ed844d564a26228378a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947941"
---
# <a name="custom-action-type-38"></a>Benutzerdefinierter Aktionstyp 38

Diese benutzerdefinierte Aktion ist in VBScript geschrieben. Siehe auch [Skripts](scripts.md).

## <a name="source"></a>Quelle

Das Feld Source der [Tabelle CustomAction](customaction-table.md) enthält den NULL-Wert. Der Skriptcode für die benutzerdefinierte Aktion wird als Zeichenfolge mit Literalskripttext im Feld Ziel gespeichert.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.



| Konstanten                                                              | Hexadezimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory** | 0x026       | 38      |



 

Windows Das Installationsprogramm kann benutzerdefinierte 64-Bit-Aktionen unter 64-Bit-Betriebssystemen verwenden. Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript-Bit** in seinem numerischen Typ enthalten. Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md) Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.



| Konstanten                                                                                                     | Hexadezimal | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript** | 0x0001026   | 4134    |



 

## <a name="target"></a>Ziel

Das Feld Target der [Tabelle CustomAction](customaction-table.md) enthält den Skriptcode für die benutzerdefinierte Aktion als Zeichenfolge mit Literalskripttext.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Rückgabeverarbeitung anzugeben. Eine Beschreibung der Optionen und Werte finden Sie unter [Benutzerdefinierte Optionen für die Aktionsrückgabeverarbeitung.](custom-action-return-processing-options.md)

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine Skriptausführungsoption anzugeben. Diese Optionen kopieren den Aktionscode in das Ausführungs-, Rollback- oder Commitskript. Eine Beschreibung der Optionen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

## <a name="return-values"></a>Rückgabewerte

Dieser benutzerdefinierte Aktionstyp gibt immer Erfolg zurück.

## <a name="remarks"></a>Hinweise

Eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, erfordert das [**Session-Objekt**](session-object.md) installieren. Das Installationsprogramm fügt das **Sitzungsobjekt** mit dem Namen "Session" an das Skript an. Da das **Session-Objekt** während eines Installationsrollbacks möglicherweise nicht vorhanden ist, muss eine im Skript geschriebene verzögerte benutzerdefinierte Aktion eine der Methoden oder Eigenschaften des **Session-Objekts** verwenden, die im Abschnitt [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben sind, um den Kontext abzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



