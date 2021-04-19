---
description: Die msilockpermissionsex-Tabelle kann verwendet werden, um Dienste, Dateien, Registrierungsschlüssel und erstellte Ordner zu sichern.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Msilockpermissionsex-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373273"
---
# <a name="msilockpermissionsex-table"></a>Msilockpermissionsex-Tabelle

Die msilockpermissionsex-Tabelle kann verwendet werden, um Dienste, Dateien, Registrierungsschlüssel und erstellte Ordner zu sichern.

Ein Paket sollte nicht sowohl die msilockpermissionsex-Tabelle als auch die [lockberechtigungs Tabelle](lockpermissions-table.md)enthalten.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Tabelle wird für Pakete empfohlen, die für die Installation mit Windows Installer 5,0 oder höher vorgesehen sind.

Die msilockpermissionsex-Tabelle weist die folgenden Spalten auf.



| Spalte               | Typ                                       | Schlüssel | Nullwerte zulässig |
|----------------------|--------------------------------------------|-----|----------|
| Msilockpermissionsex | [Text](text.md)                           | J   | N        |
| LockObject           | [Bezeichner](identifier.md)               | N   | N        |
| Tabelle                | [Text](text.md)                           | N   | N        |
| Sddltext             | [Formattedsddltext](formattedsddltext.md) | N   | N        |
| Bedingung            | [Condition](condition.md)                 | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>Msilockpermissionsex
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle.

</dd> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

In dieser Spalte und in der Tabellenspalte werden die Datei, das Verzeichnis, der Registrierungsschlüssel oder der Dienst angegeben, der gesichert werden soll. Die LockObject-Spalte ist ein Fremdschlüssel, der auf den Primärschlüssel der Tabelle verweist, die in der Tabellenspalte angegeben ist.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub
</dt> <dd>

In dieser Spalte und der Spalte lockobject werden die Datei, das Verzeichnis, der Registrierungsschlüssel oder der Dienst angegeben, der gesichert werden soll. Geben Sie in der Spalte Tabelle den Eintrag File, Registry, kreatefolder oder ServiceInstall ein, um ein lockobject anzugeben, das in der [Dateitabelle](file-table.md), in der [Registrierungs Tabelle](registry-table.md), in der [Tabelle](createfolder-table.md)mit den Tabellen oder in der Tabelle " [ServiceInstall](serviceinstall-table.md)" aufgeführt ist.

</dd> <dt>

<span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>Sddltext
</dt> <dd>

Geben Sie die SDDL-Zeichenfolge ein, um die Berechtigungen für das ausgewählte Objekt anzugeben. Die SDDL muss im Format der [Sicherheits Deskriptor-Zeichenfolge](../secauthz/security-descriptor-string-format.md)bereitgestellt werden.

Dies unterstützt keine privaten oder öffentlichen Eigenschaften.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Diese Spalte enthält einen bedingten Ausdruck, der verwendet wird, um zu bestimmen, ob die angegebene Berechtigung angewendet werden soll. Wenn die Bedingung zu **false** ausgewertet wird, wird die Berechtigung nicht angewendet. Wenn die Bedingung als **true** ausgewertet wird, wird die Berechtigung angewendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Sichern von Diensten, Dateien, Registrierungs Schlüsseln und erstellten Ordnern finden Sie unter [Sichern von Ressourcen](securing-resources-.md).

Verwenden Sie die msilockpermissionsex-Tabelle, um Objekte für ein Benutzerkonto zu sichern, das während der Installation erstellt wird. Das Benutzerkonto muss bereits vorhanden sein, wenn das Objekt durch die Installation gesichert wird. Erstellen Sie das Benutzerkonto, bevor Sie die zu sichernden Dateien, Registrierungsschlüssel, Ordner oder Dienste installieren.

Wenn ein lockobject-und Tabellen Paar in dieser Tabelle über mehr als einen Bedingungs Ausdruck verfügt, der als true ausgewertet wird, schlägt die Installation fehl, und Windows Installer gibt eine Fehlermeldung 1942 zurück.

Wenn die [formattedsddltext](formattedsddltext.md) -Zeichenfolge im sddltext-Feld nicht in eine gültige SDDL-Zeichenfolge aufgelöst werden kann, schlägt die Installation fehl, und Windows Installer gibt eine Fehlermeldung 1943 zurück.

Wenn der Benutzer nicht über ausreichende Berechtigungen verfügt, um die vom sddltext-Feld angegebene Sicherheits Beschreibung für eine Datei oder einen Ordner festzulegen, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1926 zurück.

Wenn der Benutzer nicht über ausreichende Berechtigungen zum Festlegen der Sicherheits Beschreibung verfügt, die im Feld sddltext eines Registrierungsschlüssels angegeben ist, tritt bei der Installation ein Fehler auf, und Windows Installer gibt die Fehlermeldung 1401 zurück.

Wenn der Benutzer nicht über ausreichende Berechtigungen zum Festlegen der vom sddltext-Feld für einen Dienst angegebenen Sicherheits Beschreibung verfügt, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1944 zurück.

## <a name="validation"></a>Überprüfen

<dl>

[ICE104](ice-104.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 
