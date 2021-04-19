---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 35 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Benutzerdefinierter Aktionstyp 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357033"
---
# <a name="custom-action-type-35"></a>Benutzerdefinierter Aktionstyp 35

Diese benutzerdefinierte Aktion legt das Installationsverzeichnis aus einer formatierten Text Zeichenfolge fest. Weitere Informationen finden Sie unter [Ändern des Zielspeicher Orts für ein Verzeichnis](changing-the-target-location-for-a-directory.md) .

## <a name="source"></a>`Source`

Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [Verzeichnis Tabelle](directory-table.md). Das angegebene Verzeichnis wird von der formatierten Zeichenfolge im Zielfeld mithilfe von " [**msisettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)" festgelegt. Dadurch wird der Zielpfad und die zugehörige Eigenschaft auf den erweiterten Wert der formatierten Text Zeichenfolge im Zielfeld festgelegt. Versuchen Sie nicht, den Speicherort eines Zielverzeichnisses während einer [Wartungs Installation](maintenance-installation.md)zu ändern. Versuchen Sie nicht, den Zielverzeichnis Pfad zu ändern, wenn einige Komponenten, die diesen Pfad verwenden, für einen beliebigen Benutzer bereits installiert sind.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                              | Hexadezimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbcustomaktiontypetextdata**  +  **msidbcustomaktiontypedirectory** | 0x023       | 35      |



 

## <a name="target"></a>Ziel

Die Ziel Spalte der [Tabelle CustomAction](customaction-table.md) enthält eine Text Zeichenfolge, die mit der in [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (ohne numerische feldspezifizierer) angegebenen Funktionalität formatiert ist. Die zu ersetzenden Parameter werden in eckige Klammern eingeschlossen \[ ... \] , und können Eigenschaften, Umgebungsvariablen (% prefix), Dateipfade ( \# Präfix) oder Komponenten Verzeichnispfade ($ prefix) sein. Beachten Sie, dass Verzeichnispfade immer mit einem Verzeichnis Trennzeichen enden.

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

 

 



