---
description: Die ModuleConfiguration-Tabelle identifiziert die konfigurierbaren Attribute des Moduls. Diese Tabelle wird nicht in der Datenbank zusammengeführt.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: ModuleConfiguration-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216566"
---
# <a name="moduleconfiguration-table"></a>ModuleConfiguration-Tabelle

Die ModuleConfiguration-Tabelle identifiziert die konfigurierbaren Attribute des Moduls. Diese Tabelle wird nicht in der Datenbank zusammengeführt.

Die ModuleConfiguration-Tabelle weist die folgenden Spalten auf.



| Spalte       | Typ                         | Schlüssel | Nullwerte zulässig |
|--------------|------------------------------|-----|----------|
| Name         | [Bezeichner](identifier.md) | J   | N        |
| Format       | [Integer](integer.md)       | N   | N        |
| type         | [Text](text.md)             | N   | J        |
| ContextData  | [Text](text.md)             | N   | J        |
| DefaultValue | [Text](text.md)             | N   | J        |
| Attribute   | [Integer](integer.md)       | N   | J        |
| DisplayName  | [Text](text.md)             | N   | J        |
| BESCHREIBUNG  | [Text](text.md)             | N   | J        |
| Helplocation | [Text](text.md)             | N   | J        |
| HelpKeyword  | [Text](text.md)             | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Dieses Feld definiert den Namen des konfigurierbaren Elements. Auf diesen Namen wird in der Formatierungs Vorlage in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)verwiesen.

</dd> <dt>

<span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Ges
</dt> <dd>

Diese Spalte gibt das Format der Daten an, die geändert werden.



| Format                                       | Wert |
|----------------------------------------------|-------|
| [Text](text-format-types.md)                | 0     |
| [Schlüssel](key-format-types.md)                  | 1     |
| [Integer](integer-format-types.md)          | 2     |
| [Bitfield-Format](bitfield-format-types.md) | 3     |



 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Diese Spalte gibt den Typ für die Daten an, die geändert werden. Dieser Typ wird verwendet, um einen Kontext für jede Benutzeroberfläche bereitzustellen, und wird im Mergeprozess nicht verwendet. Die gültigen Werte für diese Spalte hängen von dem Wert in der Spalte Format ab.

</dd> <dt>

<span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData
</dt> <dd>

In dieser Spalte wird ein semantischer Kontext für die angeforderten Daten angegeben. Der-Typ wird verwendet, um einen Kontext für jede Benutzeroberfläche bereitzustellen, und wird im Mergeprozess nicht verwendet. Die gültigen Werte für diese Spalte sind von den Werten in den Spalten Format und Typ abhängig.

</dd> <dt>

<span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue
</dt> <dd>

Diese Spalte gibt einen Standardwert für das Element in diesem Datensatz an, wenn das Merge-Tool einen Wert bereitstellt. Dieser Wert muss das Format, den Typ und den Kontext des Elements aufweisen. Wenn es sich um ein "Key"-Format Element handelt, muss der Fremdschlüssel ein gültiger Schlüssel in die Tabellen des Moduls sein. NULL ist möglicherweise ein gültiger Wert für diese Spalte, abhängig vom Element. Bei Key-Format Elementen liegt dieser Wert im [cmsm-Sonderformat](cmsm-special-format.md)vor. Für alle anderen Typen wird der Wert wörtlich behandelt.

Modul Autoren müssen sicherstellen, dass das Modul in seinem Standardzustand gültig ist. Dadurch wird sichergestellt, dass Versionen von Mergemod.dll vor Version 2,0 das Modul weiterhin in seinem Standardzustand verwenden können.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Diese Spalte ist ein Bitfeld, das Attribute für dieses konfigurierbare Element enthält. Null entspricht 0. Alle anderen Bits in dieser Spalte sind für die zukünftige Verwendung reserviert und müssen den Wert 0 aufweisen.



| Name                             | Decimal | Hexadezimal | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msmconfigurableoptionkeynoverwaiste | 1       | 0x00000001  | Dieses Attribut gilt nur für Datensätze, die einen Fremdschlüssel für eine Modul Tabelle in Ihrem DefaultValue-Feld auflisten. Das Merge-Tool ignoriert das-Attribut für alle anderen Formate als die [Schlüssel Format Typen](key-format-types.md). Elemente, die nicht in der [ModuleSubstitution-Tabelle](modulesubstitution-table.md) aufgeführt sind, werden von der folgenden Überprüfung ausgeschlossen. Das Merge-Tool führt die Zeile, auf die in der Spalte DefaultValue verwiesen wird, nicht in die Zieldatenbank zusammen, wenn die folgenden Bedingungen erfüllt sind, nachdem alle Konfigurationsoptionen abgeschlossen wurden.<br/> Für jede Zeile in der ModuleConfiguration-Tabelle mit dem gleichen DefaultValue-Wert ist msmconfigurationitemskeynowaist festgelegt.<br/> Keine Zeilen verwenden den DefaultValue, weil das Authoring Tool einen Wert bereitstellt.<br/> Das Zusammenführungs Tool führt die Zeile zusammen, wenn eine der folgenden Bedingungen erfüllt ist.<br/> Das Merge-Tool findet eine beliebige Zeile, für die kein msmconfigitemskeynoverwaister festgelegt ist.<br/> , Wenn das Merge-Tool eine Zeile mithilfe von DefaultValue findet, weil das Authoring Tool einen Wert bereitgestellt hat.<br/> |
| msmconfigurableoptionnonnullable | 2       | 0x00000002  | Wenn dieses Attribut festgelegt ist, ist NULL keine gültige Antwort für dieses Element. Dieses Attribut hat keine Auswirkung auf [ganzzahlige Format Typen](integer-format-types.md) oder [Bitfield-Format Typen](bitfield-format-types.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Display Name
</dt> <dd>

Diese Spalte enthält eine kurze Beschreibung dieses Elements, das vom Authoring Tool in der Benutzeroberfläche verwendet werden kann. Diese Spalte ist möglicherweise nicht lokalisiert. Legen Sie diese Spalte auf NULL fest, damit das Modul angefordert wird, dass das Authoring Tool diese Eigenschaft nicht in der Benutzeroberfläche verfügbar macht. Das Tool ignoriert möglicherweise den Wert in diesem Feld.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Diese Spalte enthält eine Beschreibung dieses Elements, das vom Authoring Tool in Benutzeroberflächen Elementen verwendet werden kann. Diese Zeichenfolge kann durch die sprach Transformation des Moduls lokalisiert werden. Diese Spalte kann NULL sein.

</dd> <dt>

<span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>Helplocation
</dt> <dd>

Diese Spalte enthält entweder den Namen einer Hilfedatei (ohne die Erweiterung ". chm") oder eine durch Semikolons getrennte Liste der Hilfe Namespaces. Diese Spalte kann NULL sein, wenn keine Hilfe verfügbar ist. Diese Spalte darf nur NULL sein, wenn die HelpKeyword-Spalte NULL ist.

</dd> <dt>

<span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword
</dt> <dd>

Diese Spalte stellt ein Schlüsselwort in der Hilfedatei oder im Namespace aus der helplocation-Spalte bereit. Die Interpretation dieses Schlüssel Worts hängt von der helplocation-Spalte ab. Diese Spalte kann NULL sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die ModuleConfiguration-Tabelle wird von [konfigurierbaren Mergemodulen](configurable-merge-modules.md)verwendet. Mergemod.dll 2,0 oder höher ist erforderlich, um ein konfigurierbares Mergemodul zu erstellen.

Um die Kompatibilität mit älteren Versionen von Mergemod.dll sicherzustellen, sollten die Tabelle ModuleConfiguration und die [Tabelle ModuleSubstitution](modulesubstitution-table.md) der Tabelle [moduleignoretable](moduleignoretable-table.md) jedes Moduls hinzugefügt werden.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
[ICE45](ice45.md)  
</dl>

 

 




