---
description: Diese temporäre Tabelle aktiviert die Option zum Deinstallieren von benutzerdefinierten Aktionen für benutzerdefinierte Aktionen, die von einem Patch hinzugefügt oder aktualisiert werden.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: Msitransformview
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363302"
---
# <a name="msitransformview"></a>Msitransformview

Diese temporäre Tabelle aktiviert die [Option zum Deinstallieren von benutzerdefinierten](custom-action-patch-uninstall-option.md) Aktionen für benutzerdefinierte Aktionen, die von einem Patch hinzugefügt oder aktualisiert werden.

Wenn ein Patch eine benutzerdefinierte Aktion hinzufügt oder aktualisiert, die über das **msidbcustomaction typepatchuninstall** -Attribut verfügt, führt Windows Installer die neue oder aktualisierte benutzerdefinierte Aktion aus, wenn der Patch deinstalliert wird. Durch Windows Installer werden die Updates, die im Patch deinstalliert werden, für die benutzerdefinierte Aktion zum Deinstallieren von Patches verfügbar. Der Patch muss eine msitransformview- *<PatchGUID>* Tabelle enthalten, um diese Informationen für Windows Installer bereitzustellen. Die Informationen in dieser Tabelle sind für jede unmittelbare benutzerdefinierte Aktion verfügbar und für verzögerte benutzerdefinierte Aktionen nicht verfügbar.

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. Die [Option zum Deinstallieren des benutzerdefinierten Aktions Patches](custom-action-patch-uninstall-option.md) ist ab Windows Installer 4,5 verfügbar.

Diese Tabelle sollte den Namen "msitransformview *<PatchGUID>* Table" haben, wobei *<PatchGUID>* die GUID ist, die den Patch eindeutig identifiziert. Die msitransformview- *<PatchGUID>* Tabelle weist die folgenden Spalten auf.



| Spalte  | Typ                         | Schlüssel | Nullwerte zulässig |
|---------|------------------------------|-----|----------|
| Tabelle   | [Bezeichner](identifier.md) | J   | N        |
| Column  | [Text](text.md)             | J   | N        |
| Zeile     | [Text](text.md)             | J   | J        |
| Daten    | [Text](text.md)             | N   | J        |
| Aktuell | [Text](text.md)             | N   | J        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

Der Name einer geänderten Datenbanktabelle.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Kolumne
</dt> <dd>

Der Name einer geänderten Tabellenspalte oder INSERT, DELETE, CREATE oder Drop.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile
</dt> <dd>

Eine Liste der Primärschlüssel Werte, die durch Registerkarten getrennt sind. NULL-Primärschlüssel Werte werden durch ein einzelnes Leerzeichen dargestellt. Ein NULL-Wert in dieser Spalte gibt eine Schema Änderung an.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats
</dt> <dd>

Daten, Name eines Datenstroms oder Spaltendefinition.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Strömung
</dt> <dd>

Aktueller Wert aus Verweis Datenbank oder Spalte a-Nummer.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Patch deinstallieren benutzerdefinierte Aktionen werden ausgeführt, wenn der Patch deinstalliert wird. Sie werden nicht ausgeführt, wenn das Produkt deinstalliert wird. Verwenden Sie die [Option zum Deinstallieren von benutzerdefinierten Aktionen](custom-action-patch-uninstall-option.md) , und verwenden Sie diese Tabelle, um nur einen benutzerdefinierten auszuführen, wenn der Patch deinstalliert wird.

Ein Patch kann eine benutzerdefinierte Aktion, die im ursprünglichen Paket (MSI-Datei) bereitgestellt wird, aktualisieren. Um die aktualisierte Version der benutzerdefinierten Aktion auszuführen, wenn der Patch deinstalliert wird, markieren Sie die benutzerdefinierte Aktion mit dem **msidbcustomaction typepatchuninstall** -Attribut im ursprünglichen Paket.

 

 



