---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 35 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Benutzerdefinierter Aktionstyp 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a724fa5a7fc469ea688c64e5935242f088c010da02d963f2f1dc4b05f5eb5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947968"
---
# <a name="custom-action-type-35"></a>Benutzerdefinierter Aktionstyp 35

Diese benutzerdefinierte Aktion legt das Installationsverzeichnis aus einer formatierten Textzeichenfolge fest. Weitere Informationen finden Sie unter [Ändern des Zielspeicherorts für ein Verzeichnis.](changing-the-target-location-for-a-directory.md)

## <a name="source"></a>Quelle

Das Feld Quelle der [Tabelle CustomAction](customaction-table.md) enthält einen Schlüssel für die [Directory-Tabelle](directory-table.md). Das angegebene Verzeichnis wird mithilfe von [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)von der formatierten Zeichenfolge im Feld Ziel festgelegt. Dadurch werden der Zielpfad und die zugeordnete Eigenschaft auf den erweiterten Wert der formatierten Textzeichenfolge im Feld Ziel festgelegt. Versuchen Sie nicht, den Speicherort eines Zielverzeichnisses während einer [Wartungsinstallation](maintenance-installation.md)zu ändern. Versuchen Sie nicht, den Zielverzeichnispfad zu ändern, wenn einige Komponenten, die diesen Pfad verwenden, bereits für einen Benutzer installiert sind.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                              | Hexadezimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>Ziel

Die Spalte Target der [CustomAction-Tabelle](customaction-table.md) enthält eine Textzeichenfolge, die mithilfe der in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) angegebenen Funktionalität formatiert ist (ohne die numerischen Feldspezifizierer). Parameter, die ersetzt werden sollen, werden in eckige Klammern ... eingeschlossen \[ \] und können Eigenschaften, Umgebungsvariablen (% Präfix), Dateipfade \# (Präfix) oder Komponentenverzeichnispfade ($-Präfix) sein. Beachten Sie, dass Verzeichnispfade immer mit einem Verzeichnistrennzeichen enden.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Die benutzerdefinierte Aktion verwendet diese Optionen nicht.

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Die benutzerdefinierte Aktion verwendet diese Optionen nicht.

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen finden Sie unter [Rückgabewerte für benutzerdefinierte Aktionen.](custom-action-return-values.md)

## <a name="remarks"></a>Hinweise

Wenn Sie eine [private Eigenschaft](private-properties.md) in der Benutzeroberflächensequenz festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Benutzeroberflächensequenztabellen erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt. Um die -Eigenschaft in der Ausführungssequenz festzulegen, müssen Sie auch eine benutzerdefinierte Aktion in einer Ausführungssequenztabelle festlegen. Alternativ können Sie die Eigenschaft zu einer [öffentlichen Eigenschaft](public-properties.md) machen und sie in die [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md)einschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Benutzerdefinierte Aktionen für formatierten Text](formatted-text-custom-actions.md)
</dt> </dl>

 

 



