---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 51 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Benutzerdefinierter Aktionstyp 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e780c1a38b60c855f4bfe665f5f68a3f6a037a078f4a2875d1a2ea57c5e7e8dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075050"
---
# <a name="custom-action-type-51"></a>Benutzerdefinierter Aktionstyp 51

Diese benutzerdefinierte Aktion legt eine Eigenschaft aus einer formatierten Textzeichenfolge fest.

Um eine Eigenschaft zu beeinflussen, die in einer Bedingung für eine Komponente oder ein Feature verwendet wird, muss die benutzerdefinierte Aktion vor der [CostFinalize-Aktion](costfinalize-action.md) in der Aktionssequenz stehen.

## <a name="source"></a>Quelle

Das Feld Quelle der [CustomAction-Tabelle](customaction-table.md) kann entweder den Namen einer Eigenschaft oder einen Schlüssel für die [Property-Tabelle](property-table.md)enthalten. Diese Eigenschaft wird mithilfe von [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)von der formatierten Zeichenfolge im Feld Target festgelegt.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                             | Hexadezimal | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty** | 0x033       | 51      |



 

## <a name="target"></a>Ziel

Die Spalte Target der [CustomAction-Tabelle](customaction-table.md) enthält eine Textzeichenfolge, die mithilfe der in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) angegebenen Funktionalität formatiert ist (ohne die numerischen Feldspezifizierer). Parameter, die ersetzt werden sollen, werden in eckige Klammern eingeschlossen, \[ ... , und können \] Eigenschaften, Umgebungsvariablen (% Präfix), Dateipfade \# (Präfix) oder Komponentenverzeichnispfade ($ Präfix) sein.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Die benutzerdefinierte Aktion verwendet diese Optionen nicht.

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Fügen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben. Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen. Eine Beschreibung der Optionen finden Sie unter [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Die benutzerdefinierte Aktion verwendet diese Optionen nicht.

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen finden Sie unter [Rückgabewerte für benutzerdefinierte Aktionen.](custom-action-return-values.md)

## <a name="remarks"></a>Hinweise

Wenn Sie eine [private Eigenschaft](private-properties.md) in der Benutzeroberflächensequenz festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Benutzeroberflächensequenztabellen erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt. Um die -Eigenschaft in der Ausführungssequenz festzulegen, müssen Sie auch eine benutzerdefinierte Aktion in eine Ausführungssequenztabelle einreihen. Alternativ können Sie die Eigenschaft zu einer [öffentlichen Eigenschaft](public-properties.md) machen und sie in die [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md)einschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> <dt>

[Benutzerdefinierte Aktionen für formatierten Text](formatted-text-custom-actions.md)
</dt> </dl>

 

 



