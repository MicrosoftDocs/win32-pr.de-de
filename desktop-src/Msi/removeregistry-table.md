---
description: Die Tabelle "removeregistry" enthält die Registrierungsinformationen, die von der Anwendung aus der Systemregistrierung gelöscht werden müssen.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Removeregistry-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959984"
---
# <a name="removeregistry-table"></a>Removeregistry-Tabelle

Die Tabelle "removeregistry" enthält die Registrierungsinformationen, die von der Anwendung aus der Systemregistrierung gelöscht werden müssen.

Die removeregistry-Tabelle weist die folgenden Spalten auf.



| Spalte         | Typ                         | Schlüssel | Nullwerte zulässig |
|----------------|------------------------------|-----|----------|
| Removeregistry | [Bezeichner](identifier.md) | J   | N        |
| Root           | [Integer](integer.md)       | N   | N        |
| Schlüssel            | [Regfad](regpath.md)       | N   | N        |
| Name           | [Großformatige](formatted.md)   | N   | J        |
| Komponente\_    | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>Removeregistry
</dt> <dd>

Der Schlüssel für diese Tabelle.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Fasst
</dt> <dd>

Der vordefinierte Stamm Schlüssel für den Registrierungs Wert.



| Konstante                          | Hexadezimal | Decimal | Stamm Schlüssel                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                            | \- 0x001    | -1      | **HKEY \_ Das \_** Installationsprogramm des aktuellen Benutzers legt diesen Schlüssel fest, während eine Installation pro Benutzer ausgeführt wird.<br/>                                                                                                                    |
| (none)                            | -0x001      | -1      | **HKEY \_ Das Installationsprogramm für den lokalen \_ Computer** legt diesen Schlüssel fest, während eine Installation aller Benutzer mit [**ALLUSERS**](allusers.md) auf 1 festgelegt wird.<br/>                                                                       |
| **msidbregistryrootclassesroot**  | 0x000       | 0       | **HKEY \_ Klassen \_** Stamm: das Installationsprogramm entfernt den Wert aus den **HKCU- \\ Software \\ Klassen** Hive während der Installationen im Einzelbenutzer-und computerspezifischen [Installations Kontext](installation-context.md).<br/> |
| **msidbregistryrootcurrentuser**  | 0x001       | 1       | **Aktueller HKEY- \_ \_ Benutzer**                                                                                                                                                                                            |
| **msidbregistryrootlocalmachine** | 0x002       | 2       | **lokaler HKEY- \_ \_ Computer**                                                                                                                                                                                           |
| **msidbregistryrootusers**        | 0x003       | 3       | **HKEY- \_ Benutzer**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen
</dt> <dd>

Der lokalisierbare Schlüssel für den Registrierungs Wert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der lokalisierbare Name des Registrierungs Werts.

Die folgende Zeichenfolge in der Spalte Name hat eine besondere Bedeutung.



| String | Bedeutung                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | Wenn die Komponente installiert ist, muss der Schlüssel ggf. mit allen zugehörigen Werten und unter Schlüsseln gelöscht werden. |



 

Beachten Sie, dass die [Registrierungs Tabelle](registry-table.md) zum Erstellen oder Entfernen eines Registrierungsschlüssels verwendet werden soll, wenn die Komponente entfernt wird.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md) , die auf die Komponente verweist, die das Löschen des Registrierungs Werts steuert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Registrierungsinformationen werden aus der Systemregistrierung gelöscht, wenn die entsprechende Komponente für die lokale Installation ausgewählt oder von der Quelle aus ausgeführt wurde.

Diese Tabelle wird beim Ausführen der [removeregistryvalues-Aktion](removeregistryvalues-action.md) bezeichnet.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




