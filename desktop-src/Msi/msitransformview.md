---
description: Diese temporäre Tabelle aktiviert die Option Zum Deinstallieren von benutzerdefinierten Aktionspatches für benutzerdefinierte Aktionen, die von einem Patch hinzugefügt oder aktualisiert werden.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b6c46ebfcfb82ee23ce6acec998490f53fe67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882238"
---
# <a name="msitransformview"></a>MsiTransformView

Diese temporäre Tabelle aktiviert die Option Zum Deinstallieren von [benutzerdefinierten Aktionspatches](custom-action-patch-uninstall-option.md) für benutzerdefinierte Aktionen, die von einem Patch hinzugefügt oder aktualisiert werden.

Wenn ein Patch eine benutzerdefinierte Aktion mit dem **msidbCustomActionTypePatchUninstall-Attribut** hinzufügt oder aktualisiert, führt Windows Installer die neue oder aktualisierte benutzerdefinierte Aktion aus, wenn der Patch deinstalliert wird. Windows Das Installationsprogramm macht die Updates innerhalb des zu deinstallierenden Patches für die benutzerdefinierte Aktion "Patchdeinstallation" verfügbar. Der Patch muss eine MsiTransformView *&lt; &gt; PatchGUID-Tabelle* enthalten, um diese Informationen für Windows Installer bereitzustellen. Die Informationen in dieser Tabelle sind für alle unmittelbaren benutzerdefinierten Aktionen verfügbar und nicht für verzögerte benutzerdefinierte Aktionen verfügbar.

**[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)** Wird nicht unterstützt. Die [Deinstallationsoption für benutzerdefinierte Aktionspatches](custom-action-patch-uninstall-option.md) ist ab Windows Installer 4.5 verfügbar.

Diese Tabelle sollte msiTransformView *&lt; &gt; PatchGUID-Tabelle* genannt werden, wobei *&lt; PatchGUID &gt;* die GUID ist, die den Patch eindeutig identifiziert. Die MsiTransformView *&lt; &gt; PatchGUID-Tabelle* enthält die folgenden Spalten.



| Spalte  | Typ                         | Schlüssel | Nullwerte zulässig |
|---------|------------------------------|-----|----------|
| Tabelle   | [Identifier](identifier.md) | J   | N        |
| Column  | [Text](text.md)             | J   | N        |
| Zeile     | [Text](text.md)             | J   | J        |
| Daten    | [Text](text.md)             | N   | J        |
| Aktuell | [Text](text.md)             | N   | J        |



 

## <a name="column"></a>Spalte

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Name einer geänderten Datenbanktabelle.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Spalte
</dt> <dd>

Name einer geänderten Tabellenspalte oder INSERT, DELETE, CREATE oder DROP.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Zeile
</dt> <dd>

Eine Liste der Primärschlüsselwerte, die durch Registerkarten getrennt sind. NULL-Primärschlüsselwerte werden durch ein einzelnes Leerzeichen dargestellt. Ein NULL-Wert in dieser Spalte gibt eine Schemaänderung an.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Daten
</dt> <dd>

Daten, Name eines Datenstroms oder einer Spaltendefinition.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Aktuellen
</dt> <dd>

Aktueller Wert aus der Verweisdatenbank oder Spalte einer Zahl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Benutzerdefinierte Aktionen zur Patchdeinstallation werden ausgeführt, wenn der Patch deinstalliert wird. Sie werden nicht ausgeführt, wenn das Produkt deinstalliert wird. Verwenden Sie die [Option Benutzerdefinierte Aktion Patchdeinstallation](custom-action-patch-uninstall-option.md) und diese Tabelle, um eine benutzerdefinierte nur auszuführen, wenn der Patch deinstalliert wird.

Ein Patch kann eine benutzerdefinierte Aktion aktualisieren, die im ursprünglichen Paket (.msi-Datei) bereitgestellt wird. Um die aktualisierte Version der benutzerdefinierten Aktion auszuführen, wenn der Patch deinstalliert wird, markieren Sie die benutzerdefinierte Aktion mit dem **msidbCustomActionTypePatchUninstall-Attribut** im ursprünglichen Paket.

 

 



