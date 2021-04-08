---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 51 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Benutzerdefinierter Aktionstyp 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960351"
---
# <a name="custom-action-type-51"></a>Benutzerdefinierter Aktionstyp 51

Diese benutzerdefinierte Aktion legt eine Eigenschaft aus einer formatierten Text Zeichenfolge fest.

Um eine Eigenschaft zu beeinflussen, die in einer Bedingung für eine Komponente oder eine Funktion verwendet wird, muss die benutzerdefinierte Aktion vor der [Aktion "costfinalize](costfinalize-action.md) " in der Aktions Sequenz erfolgen.

## <a name="source"></a>`Source`

Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " kann entweder den Namen einer Eigenschaft oder einen Schlüssel für die [Eigenschaften Tabelle](property-table.md)enthalten. Diese Eigenschaft wird von der formatierten Zeichenfolge im Zielfeld mithilfe von " [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)" festgelegt.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                             | Hexadezimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypetextdata**  +  **msidbcustomaktiontypeproperty** | 0x033       | 51      |



 

## <a name="target"></a>Ziel

Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält eine Text Zeichenfolge, die mit der in [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (ohne numerische feldspezifizierer) angegebenen Funktionalität formatiert ist. Die zu ersetzenden Parameter sind in eckige Klammern ( \[ ...) eingeschlossen \] und können Eigenschaften, Umgebungsvariablen (% prefix), Dateipfade ( \# Präfix) oder Komponenten Verzeichnispfade ($ prefix) sein.

## <a name="return-processing-options"></a>Rückgabe Verarbeitungsoptionen

Diese Optionen werden von der benutzerdefinierten Aktion nicht verwendet.

## <a name="execution-scheduling-options"></a>Ausführungszeit Planungsoptionen

Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Ausführungs Optionen für In-Script

Diese Optionen werden von der benutzerdefinierten Aktion nicht verwendet.

## <a name="return-values"></a>Rückgabewerte

Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).

## <a name="remarks"></a>Bemerkungen

Wenn Sie in der UI-Sequenz eine [private Eigenschaft](private-properties.md) festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Benutzeroberflächen-Sequenz Tabellen erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt. Wenn Sie die-Eigenschaft in der Ausführungssequenz festlegen möchten, müssen Sie auch eine benutzerdefinierte Aktion in eine Ausführungssequenz Tabelle einfügen. Alternativ können Sie die Eigenschaft zu einer [öffentlichen Eigenschaft](public-properties.md) machen und in der [**securecustomproperties-Eigenschaft**](securecustomproperties.md)einschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Formatierte Text benutzerdefinierte Aktionen](formatted-text-custom-actions.md)
</dt> </dl>

 

 



