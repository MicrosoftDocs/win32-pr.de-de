---
description: Diese temporäre Tabelle aktiviert die Option "Custom Action Patch Uninstall" für benutzerdefinierte Aktionen, die durch einen Patch hinzugefügt oder aktualisiert werden.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978f27fe68d89abd3ea94a4d13adc815bbc6510564caf949b937d8a4213428b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944248"
---
# <a name="msitransformview"></a>MsiTransformView

Diese temporäre Tabelle aktiviert die Option ["Custom Action Patch Uninstall"](custom-action-patch-uninstall-option.md) für benutzerdefinierte Aktionen, die durch einen Patch hinzugefügt oder aktualisiert werden.

Wenn ein Patch eine benutzerdefinierte Aktion mit dem **Attribut msidbCustomActionTypePatchUninstall** hinzufügt oder aktualisiert, führt Windows Installer die neue oder aktualisierte benutzerdefinierte Aktion aus, wenn der Patch deinstalliert wird. Windows Das Installationsprogramm stellt die Updates innerhalb des zu deinstallierenden Patches für die benutzerdefinierte Aktion zur Patchdeinstallation zur Verfügung. Der Patch muss eine MsiTransformView-Tabelle *<PatchGUID>* enthalten, um diese Informationen für den Windows bereitstellen zu können. Die Informationen in dieser Tabelle sind für alle unmittelbaren benutzerdefinierten Aktionen verfügbar und für zurückgestellte benutzerdefinierte Aktionen nicht verfügbar.

**[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)** Nicht unterstützt. Die [Option Zum Deinstallieren benutzerdefinierter Aktionspatches](custom-action-patch-uninstall-option.md) ist ab Windows Installer 4.5 verfügbar.

Diese Tabelle sollte msiTransformView Table heißen, wobei *<PatchGUID>* die GUID ist, die den Patch *<PatchGUID>* eindeutig identifiziert. Die MsiTransformView-Tabelle *<PatchGUID>* enthält die folgenden Spalten.



| Spalte  | Typ                         | Key | Nullwerte zulässig |
|---------|------------------------------|-----|----------|
| Tabelle   | [Identifier](identifier.md) | J   | N        |
| Column  | [Text](text.md)             | J   | N        |
| Zeile     | [Text](text.md)             | J   | J        |
| Daten    | [Text](text.md)             | N   | J        |
| Aktuell | [Text](text.md)             | N   | J        |



 

## <a name="column"></a>Column

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

Eine Liste der Primärschlüsselwerte, die durch Tabstopps getrennt sind. Null-Primärschlüsselwerte werden durch ein einzelnes Leerzeichen dargestellt. Ein NULL-Wert in dieser Spalte gibt eine Schemaänderung an.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Daten
</dt> <dd>

Daten, Name eines Datenstroms oder eine Spaltendefinition.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Aktuellen
</dt> <dd>

Der aktuelle Wert aus der Verweisdatenbank oder spaltet eine Zahl.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Benutzerdefinierte Aktionen zur Patchdeinstallation werden ausgeführt, wenn der Patch deinstalliert wird. Sie werden nicht ausgeführt, wenn das Produkt deinstalliert wird. Verwenden Sie die [Deinstallationsoption Benutzerdefinierte](custom-action-patch-uninstall-option.md) Aktion Patch und diese Tabelle, um einen benutzerdefinierten nur dann ausführen, wenn der Patch deinstalliert wird.

Ein Patch kann eine benutzerdefinierte Aktion aktualisieren, die im ursprünglichen Paket bereitgestellt wird (.msi Datei). Um die aktualisierte Version der benutzerdefinierten Aktion beim Deinstallieren des Patches ausführen zu können, markieren Sie die benutzerdefinierte Aktion mit dem **Attribut msidbCustomActionTypePatchUninstall** im ursprünglichen Paket.

 

 



