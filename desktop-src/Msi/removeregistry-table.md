---
description: Die Tabelle RemoveRegistry enthält die Registrierungsinformationen, die die Anwendung aus der Systemregistrierung löschen muss.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: RemoveRegistry-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170dc727eef47ac214f7a7f42af7f487f53ad0b9a0658182420b28eb5224e38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314880"
---
# <a name="removeregistry-table"></a>RemoveRegistry-Tabelle

Die Tabelle RemoveRegistry enthält die Registrierungsinformationen, die die Anwendung aus der Systemregistrierung löschen muss.

Die RemoveRegistry-Tabelle enthält die folgenden Spalten.



| Spalte         | Typ                         | Key | Nullwerte zulässig |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [Identifier](identifier.md) | J   | N        |
| Root           | [Integer](integer.md)       | N   | N        |
| Key            | [RegPath](regpath.md)       | N   | N        |
| Name           | [Formatiert](formatted.md)   | N   | J        |
| Komponente\_    | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

Der Schlüssel für diese Tabelle.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>wurzel
</dt> <dd>

Der vordefinierte Stammschlüssel für den Registrierungswert.



| Konstante                          | Hexadezimal | Decimal | Stammschlüssel                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                            | \- 0x001    | –1      | **HKEY \_ Current \_ USER** Installer legt diesen Schlüssel bei einer benutzerspezifischen Installation fest.<br/>                                                                                                                    |
| (none)                            | -0x001      | –1      | **HKEY \_ Local \_ Machine** Installer legt diesen Schlüssel fest, während eine Installation für alle Benutzer mit [**ALLUSERS**](allusers.md) auf 1 festgelegt ist.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ \_KLASSENSTAMM** Das Installationsprogramm entfernt den Wert aus der **Hive HKCU \\ Software \\ Classes** während der Installation im Installationskontext pro Benutzer und [computerspezifischem](installation-context.md).<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **AKTUELLER \_ \_ HKEY-BENUTZER**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ LOCAL \_ MACHINE**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **\_HKEY-BENUTZER**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Schlüssel
</dt> <dd>

Der lokalisierbare Schlüssel für den Registrierungswert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Der lokalisierbare Registrierungswertname.

Die folgende Zeichenfolge in der Spalte Name hat eine besondere Bedeutung.



| String | Bedeutung                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | Der Schlüssel muss bei der Installation der Komponente gelöscht werden(sofern vorhanden) mit allen Werten und Unterschlüsseln. |



 

Beachten Sie, [dass die Registrierungstabelle](registry-table.md) verwendet werden sollte, um einen Registrierungsschlüssel zu erstellen oder zu entfernen, wenn die Komponente entfernt wird.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Tabelle Komponente,](component-table.md) die auf die Komponente verweisen, die das Löschen des Registrierungswerts steuert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Registrierungsinformationen werden aus der Systemregistrierung gelöscht, wenn die entsprechende Komponente ausgewählt wurde, um lokal installiert oder aus der Quelle ausgeführt zu werden.

Auf diese Tabelle wird verwiesen, wenn die [RemoveRegistryValues-Aktion](removeregistryvalues-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




