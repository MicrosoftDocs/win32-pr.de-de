---
description: Die MsiLockPermissionsEx-Tabelle kann zum Sichern von Diensten, Dateien, Registrierungsschlüsseln und erstellten Ordnern verwendet werden.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: MsiLockPermissionsEx-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bff3d97bc6cd6003470b1be7d1feb20b385701d332ba852a660aa4ff6c57271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119294800"
---
# <a name="msilockpermissionsex-table"></a>MsiLockPermissionsEx-Tabelle

Die MsiLockPermissionsEx-Tabelle kann zum Sichern von Diensten, Dateien, Registrierungsschlüsseln und erstellten Ordnern verwendet werden.

Ein Paket darf nicht sowohl die MsiLockPermissionsEx-Tabelle als auch die [LockPermissions-Tabelle](lockpermissions-table.md)enthalten.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Wird nicht unterstützt. Diese Tabelle wird für Pakete empfohlen, die für die Installation mit Windows Installer 5.0 oder höher vorgesehen sind.

Die MsiLockPermissionsEx-Tabelle weist die folgenden Spalten auf.



| Spalte               | Typ                                       | Key | Nullwerte zulässig |
|----------------------|--------------------------------------------|-----|----------|
| MsiLockPermissionsEx | [Text](text.md)                           | J   | N        |
| LockObject           | [Identifier](identifier.md)               | N   | N        |
| Tabelle                | [Text](text.md)                           | N   | N        |
| SDDLText             | [FormattedSDDLText](formattedsddltext.md) | N   | N        |
| Bedingung            | [Condition](condition.md)                 | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle.

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Diese Spalte und die Spalte Tabelle geben zusammen die Zu sichernde Datei, das Verzeichnis, den Registrierungsschlüssel oder den Dienst an. Die LockObject-Spalte ist ein Fremdschlüssel, der auf den Primärschlüssel der tabelle verweist, die von der Table-Spalte angegeben wird.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabelle
</dt> <dd>

Diese Spalte und die Spalte LockObject geben die Zu sichernde Datei, das Verzeichnis, den Registrierungsschlüssel oder den Dienst an. Geben Sie in der Spalte Tabelle Datei, Registrierung, CreateFolder oder ServiceInstall ein, um ein LockObject anzugeben, das in der [Dateitabelle,](file-table.md) [der Registrierungstabelle,](registry-table.md)der [CreateFolder-Tabelle](createfolder-table.md)oder der [ServiceInstall-Tabelle](serviceinstall-table.md)aufgeführt ist.

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText
</dt> <dd>

Geben Sie die SDDL-Zeichenfolge ein, um die Berechtigungen anzugeben, die auf das ausgewählte Objekt angewendet werden sollen. Die SDDL muss im [Format der Sicherheitsbeschreibungszeichenfolge](../secauthz/security-descriptor-string-format.md)angegeben werden.

Private oder öffentliche Eigenschaften werden nicht unterstützt.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Diese Spalte enthält einen bedingten Ausdruck, mit dem bestimmt wird, ob die angegebene Berechtigung angewendet werden soll. Wenn die Bedingung als **FALSE** ausgewertet wird, wird die Berechtigung nicht angewendet. Wenn die Bedingung zu **TRUE** ausgewertet wird, wird die Berechtigung angewendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Sichern von Diensten, Dateien, Registrierungsschlüsseln und erstellten Ordnern finden Sie unter Sichern von [Ressourcen.](securing-resources-.md)

Verwenden Sie die MsiLockPermissionsEx-Tabelle, um Objekte für ein Benutzerkonto zu schützen, das während der Installation erstellt wird. Das Benutzerkonto muss bereits vorhanden sein, wenn die Installation das Objekt sichert. Erstellen Sie das Benutzerkonto, bevor Sie die zu sichernde Datei, den Registrierungsschlüssel, den Ordner oder den Dienst installieren.

Wenn ein LockObject- und Table-Paar in dieser Tabelle über mehrere bedingte Ausdrücke verfügt, die als TRUE ausgewertet werden, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1942 zurück.

Wenn die [FormattedSDDLText-Zeichenfolge](formattedsddltext.md) im Feld SDDLText nicht in eine gültige SDDL-Zeichenfolge aufgelöst werden kann, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1943 zurück.

Wenn der Benutzer nicht über ausreichende Berechtigungen verfügt, um den sicherheitsdeskriptor festzulegen, der im Feld SDDLText für eine Datei oder einen Ordner angegeben wird, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1926 zurück.

Wenn der Benutzer nicht über ausreichende Berechtigungen verfügt, um den sicherheitsdeskriptor festzulegen, der im Feld SDDLText für einen Registrierungsschlüssel angegeben wird, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1401 zurück.

Wenn der Benutzer nicht über ausreichende Berechtigungen zum Festlegen des Sicherheitsdeskriptors verfügt, der vom Feld SDDLText für einen Dienst angegeben wird, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1944 zurück.

## <a name="validation"></a>Überprüfung

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
