---
description: Die ModuleConfiguration-Tabelle identifiziert die konfigurierbaren Attribute des Moduls. Diese Tabelle wird nicht mit der Datenbank zusammengeführt.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: ModuleConfiguration-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c499e313633d1668db81c91654800d1d5824192839329316f55040fd3bc7bad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963060"
---
# <a name="moduleconfiguration-table"></a>ModuleConfiguration-Tabelle

Die ModuleConfiguration-Tabelle identifiziert die konfigurierbaren Attribute des Moduls. Diese Tabelle wird nicht mit der Datenbank zusammengeführt.

Die ModuleConfiguration-Tabelle enthält die folgenden Spalten.



| Spalte       | Typ                         | Key | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| Name         | [Identifier](identifier.md) | J   | N        |
| Format       | [Integer](integer.md)       | N   | N        |
| type         | [Text](text.md)             | N   | J        |
| ContextData  | [Text](text.md)             | N   | J        |
| DefaultValue | [Text](text.md)             | N   | J        |
| Attribute   | [Integer](integer.md)       | N   | J        |
| DisplayName  | [Text](text.md)             | N   | J        |
| BESCHREIBUNG  | [Text](text.md)             | N   | J        |
| HelpLocation | [Text](text.md)             | N   | J        |
| Helpkeyword  | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Dieses Feld definiert den Namen des konfigurierbaren Elements. Auf diesen Namen wird in der Formatierungsvorlage in der Spalte Wert der [Tabelle ModuleSubs standardwert verwiesen.](modulesubstitution-table.md)

</dd> <dt>

<span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format
</dt> <dd>

Diese Spalte gibt das Format der zu ändernden Daten an.



| Format                                       | Wert |
|----------------------------------------------|-------|
| [Text](text-format-types.md)                | 0     |
| [Schlüssel](key-format-types.md)                  | 1     |
| [Integer](integer-format-types.md)          | 2     |
| [Bitfield-Format](bitfield-format-types.md) | 3     |



 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Typ
</dt> <dd>

Diese Spalte gibt den Typ für die zu ändernden Daten an. Dieser Typ wird verwendet, um einen Kontext für jede Benutzeroberfläche zur Verfügung zu stellen, und wird nicht im Mergeprozess verwendet. Die gültigen Werte für diese Spalte hängen vom Wert in der Spalte Format ab.

</dd> <dt>

<span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData
</dt> <dd>

Diese Spalte gibt einen semantischen Kontext für die angeforderten Daten an. Der -Typ wird verwendet, um einen Kontext für jede Benutzeroberfläche zur Verfügung zu stellen, und wird nicht im Mergeprozess verwendet. Die gültigen Werte für diese Spalte hängen von den Werten in den Spalten Format und Type ab.

</dd> <dt>

<span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>Defaultvalue
</dt> <dd>

Diese Spalte gibt einen Standardwert für das Element in diesem Datensatz an, wenn das Mergetool die Bereitstellung eines Werts abgelehnt hat. Dieser Wert muss das Format, den Typ und den Kontext des Elements haben. Wenn es sich um ein Formatelement "Schlüssel" handelt, muss der Fremdschlüssel ein gültiger Schlüssel in den Tabellen des Moduls sein. Null kann je nach Element ein gültiger Wert für diese Spalte sein. Für "Key"-Formatelemente hat dieser Wert das [CMSM-Sonderformat](cmsm-special-format.md). Für alle anderen Typen wird der Wert wörtlich behandelt.

Modulautoren müssen sicherstellen, dass das Modul im Standardzustand gültig ist. Dadurch wird sichergestellt, dass Versionen Mergemod.dll Version 2.0 das Modul weiterhin im Standardzustand verwenden können.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Diese Spalte ist ein Bitfeld, das Attribute für dieses konfigurierbare Element enthält. NULL entspricht 0. Alle anderen Bits in dieser Spalte sind für die zukünftige Verwendung reserviert und müssen 0 sein.



| Name                             | Decimal | Hexadezimal | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msmConfigurableOptionKeyNoOrphan | 1       | 0x00000001  | Dieses Attribut gilt nur für Datensätze, die einen Fremdschlüssel für eine Modultabelle in ihrem DefaultValue-Feld auflisten. Das Mergetool ignoriert das -Attribut für alle Formate außer den [Schlüsselformattypen](key-format-types.md). Elemente, die nicht in der [Tabelle ModuleSubstitution aufgeführt sind,](modulesubstitution-table.md) werden von der folgenden Überprüfung ausgeschlossen. Das Mergetool führt die Zeile, auf die von der DefaultValue -Spalte verwiesen wird, nicht mit der Zieldatenbank zusammen, wenn die folgenden Bedingungen erfüllt sind, nachdem alle Konfigurationsoptionen abgeschlossen wurden.<br/> Für jede Zeile in der ModuleConfiguration-Tabelle mit demselben DefaultValue-Wert ist msmConfigurationItemsKeyNoOrphan festgelegt.<br/> Der DefaultValue wird von keinen Zeilen verwendet, da das Erstellungstool abgelehnt hat, einen Wert bereitzustellen.<br/> Das Mergetool führt die Zeile zusammen, wenn eine der folgenden Bedingungen erfüllt ist.<br/> Das Mergetool sucht alle Zeilen, für die msmConfigItemsKeyNoOrphan nicht festgelegt ist.<br/> Wenn das Mergetool eine Zeile mit DefaultValue findet, weil das Erstellungstool abgelehnt hat, einen Wert bereitzustellen.<br/> |
| msmConfigurableOptionNonNullable | 2       | 0x00000002  | Wenn dieses Attribut festgelegt ist, ist NULL keine gültige Antwort für dieses Element. Dieses Attribut hat keine Auswirkungen auf [Ganzzahlformattypen](integer-format-types.md) oder [Bitfield-Formattypen.](bitfield-format-types.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Displayname
</dt> <dd>

Diese Spalte enthält eine kurze Beschreibung dieses Elements, das das Erstellungstool auf der Benutzeroberfläche verwenden kann. Diese Spalte ist möglicherweise nicht lokalisiert. Legen Sie diese Spalte auf NULL fest, damit das Modul anfordert, dass das Erstellungstool diese Eigenschaft nicht auf der Benutzeroberfläche verfügbar macht. Das Tool ignoriert möglicherweise den Wert in diesem Feld.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Diese Spalte enthält eine Beschreibung dieses Elements, das das Erstellungstool in Benutzeroberflächenelementen verwenden kann. Diese Zeichenfolge kann durch die Sprachtransformation des Moduls lokalisiert werden. Diese Spalte kann NULL sein.

</dd> <dt>

<span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation
</dt> <dd>

Diese Spalte enthält entweder den Namen einer Hilfedatei (ohne die Erweiterung .chm) oder eine durch Semikolons getrennte Liste von Hilfenamespaces. Diese Spalte kann NULL sein, wenn keine Hilfe verfügbar ist. Diese Spalte kann nur NULL sein, wenn die HelpKeyword-Spalte NULL ist.

</dd> <dt>

<span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>Helpkeyword
</dt> <dd>

Diese Spalte stellt ein Schlüsselwort in die Hilfedatei oder den Namespace aus der HelpLocation-Spalte bereit. Die Interpretation dieses Schlüsselworts hängt von der HelpLocation-Spalte ab. Diese Spalte kann NULL sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Tabelle ModuleConfiguration wird von [konfigurierbaren Mergemodulen](configurable-merge-modules.md)verwendet. Mergemod.dll 2.0 oder höher ist erforderlich, um ein konfigurierbares Mergemodul zu erstellen.

Um die Kompatibilität mit älteren Versionen von Mergemod.dll sicherzustellen, sollten die Tabelle ModuleConfiguration und die [Tabelle ModuleSubsdatenbank](modulesubstitution-table.md) der [Tabelle ModuleIgnoreTable](moduleignoretable-table.md) jedes Moduls hinzugefügt werden.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
[ICE45](ice45.md)  
</dl>

 

 




