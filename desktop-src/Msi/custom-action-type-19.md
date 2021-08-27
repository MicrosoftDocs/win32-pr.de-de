---
description: Entwickler von Windows Installer-Paketen können einen benutzerdefinierten Aktionstyp 19 verwenden, wenn die Standardaktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Benutzerdefinierter Aktionstyp 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cbbef4ec07d805e41c0de25c371f995782ce3d8df66a89ee93363afa05f55b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075060"
---
# <a name="custom-action-type-19"></a>Benutzerdefinierter Aktionstyp 19

Diese benutzerdefinierte Aktion zeigt eine angegebene Fehlermeldung an, gibt einen Fehler zurück und beendet dann die Installation. Die angezeigte Fehlermeldung kann als Zeichenfolge oder als Index in der [Fehlertabelle angegeben werden.](error-table.md)

## <a name="source"></a>Quelle

Lassen Sie die Spalte Source der [Tabelle CustomAction](customaction-table.md) leer.

## <a name="type-value"></a>Typwert

Fügen Sie den folgenden Wert in die Spalte Typ der CustomAction-Tabelle ein, um den grundlegenden numerischen Typ anzugeben.



| Konstanten                                                               | Hexadezimal | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile** | 0x013       | 19      |



 

## <a name="target"></a>Ziel

Die Target -Spalte der [CustomAction-Tabelle](customaction-table.md) enthält eine Textzeichenfolge, die mit der in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) angegebenen Funktionalität formatiert ist (ohne die numerischen Feldspezifizierer). Zu ersetzende Parameter werden in eckige Klammern ( ... ) eingeschlossen, und es kann sich um Eigenschaften, Umgebungsvariablen (Präfix in Prozent), Dateipfade (Präfix) oder Komponentenverzeichnispfade \[ \] \# (Präfix $) handelt. Wenn die Zeichenfolge nach dem Formatieren zu einer ganzen Zahl ausgewertet wird, wird diese ganze Zahl als Index in der [Tabelle Error](error-table.md) verwendet, um die anzuzeigende Meldung abzurufen. Wenn die Zeichenfolge nach dem Formatieren nicht numerische Zeichen enthält, wird die Zeichenfolge selbst als Meldung angezeigt.

## <a name="return-processing-options"></a>Optionen für die Rückgabeverarbeitung

Die benutzerdefinierte Aktion verwendet keine Optionen.

## <a name="execution-scheduling-options"></a>Optionen für die Ausführungsplanung

Die benutzerdefinierte Aktion verwendet keine Optionen.

## <a name="in-script-execution-options"></a>In-Script Ausführungsoptionen

Die benutzerdefinierte Aktion verwendet keine Optionen.

## <a name="return-values"></a>Rückgabewerte

Weitere Informationen [finden Sie unter Rückgabewerte für benutzerdefinierte Aktionen.](custom-action-return-values.md)

## <a name="remarks"></a>Hinweise

Beispielsweise geben die benutzerdefinierten Aktionen CAError1, CAError2, CAError3 und CAError4 diese Meldungen zurück.

[CustomAction-Tabelle](customaction-table.md)



| Aktion   | type | `Source` | Ziel                              |
|----------|------|--------|-------------------------------------|
| CAError1 | 19   |        | \[Prop1\]                           |
| CAError2 | 19   |        | Installationsfehler aufgrund von Error2. |
| CAError3 | 19   |        | 25000                               |
| CAError4 | 19   |        | \[Prop2\]                           |



 

[Eigenschaftentabelle](property-table.md)



| Eigenschaft | Wert                                 |
|----------|---------------------------------------|
| Prop1    | "Installationsfehler aufgrund von Error1." |
| Prop2    | "25100"                               |



 

[Fehlertabelle](error-table.md)



| Code  | `Message`                             |
|-------|-------------------------------------|
| 25000 | Installationsfehler aufgrund von Error3. |
| 25100 | Installationsfehler aufgrund von Error4. |



 

Diese benutzerdefinierten Aktionen geben die folgenden Fehlermeldungen zurück:



| Benutzerdefinierte Aktion | Zurückgegebene Meldungszeichenfolge             |
|---------------|-------------------------------------|
| CAError1      | Installationsfehler aufgrund von Error1. |
| CAError2      | Installationsfehler aufgrund von Error2. |
| CAError3      | Installationsfehler aufgrund von Error3. |
| CAError4      | Installationsfehler aufgrund von Error4. |



 

Beachten Sie, dass Sie benutzerdefinierte Aktionen vom Typ "Benutzerdefinierter Aktionstyp 19" in Ihrer Installation verwenden sollten, um Bedingungen in einer bestimmten Reihenfolge zu bewerten, da die Reihenfolge der Auswertung von Startbedingungen nicht durch erstellen der [LaunchCondition-Tabelle](launchcondition-table.md)garantiert werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte \_ Aktionen](custom-actions.md)
</dt> </dl>

 

 



