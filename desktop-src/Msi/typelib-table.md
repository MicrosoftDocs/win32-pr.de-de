---
description: Die TypeLib-Tabelle enthält die Informationen, die in der Registrierungs Registrierung von Typbibliotheken abgelegt werden müssen.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: TypeLib-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341169"
---
# <a name="typelib-table"></a>TypeLib-Tabelle

Die TypeLib-Tabelle enthält die Informationen, die in der Registrierungs Registrierung von Typbibliotheken abgelegt werden müssen.

Die TypeLib-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                               | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| LIBID       | [GUID](guid.md)                   | J   | N        |
| Sprache    | [Integer](integer.md)             | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md)       | J   | N        |
| Version     | [Doubleiteger](doubleinteger.md) | N   | J        |
| BESCHREIBUNG | [Text](text.md)                   | N   | J        |
| Verzeichnis\_ | [Bezeichner](identifier.md)       | N   | J        |
| Funktion\_   | [Bezeichner](identifier.md)       | N   | N        |
| „Cost“ (Kosten)        | [Doubleiteger](doubleinteger.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LIBID
</dt> <dd>

Der GUID, der die Bibliothek identifiziert.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Kurse
</dt> <dd>

Die Sprache der Typbibliothek. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md). Diese Spalte identifiziert die Komponente, die zu der Funktion gehört, \_ deren Schlüsseldatei die Typbibliothek ist, die registriert wird.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Dies ist die Version der Bibliothek. Die Haupt-und neben Versionen werden im ganzzahligen Wert von vier Bytes codiert. Die neben Version ist in den unteren acht Bits. Die Hauptversion liegt in den Mitte sechzehn Bits.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine lokalisierbare Beschreibung der Bibliothek.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Verzeichnis Tabelle](directory-table.md). Diese Spalte identifiziert den Hilfepfad für die Typbibliothek. Diese Spalte wird bei der Werbung ignoriert.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Funktions Tabelle](feature-table.md). Diese Spalte gibt die Funktion an, die installiert werden muss, damit die Typbibliothek funktionstüchtig ist.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Preis
</dt> <dd>

Die Kosten, die mit der Registrierung der Typbibliothek in Bytes verknüpft sind. Dies muss eine nicht negative Zahl oder NULL sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Auf diese Tabelle wird verwiesen, wenn die Aktion [registertypelibraries](registertypelibraries-action.md) oder die [unregistertypelibraries-Aktion](unregistertypelibraries-action.md) ausgeführt wird.

Das Installationsprogramm schreibt alle Typbibliotheks-Registrierungsinformationen in den \_ \_ Registrierungs Speicherort HKLM (HKEY Local Machine). Dies gilt auch für Installationen pro Benutzer. Typbibliotheken können nicht an Benutzer Standorten (HKCU) registriert werden.

Autoren von Installationspaketen wird dringend empfohlen, die TypeLib-Tabelle zu verwenden. Stattdessen sollten Sie Typbibliotheken mithilfe der [Registrierungs](registry-table.md) Tabelle registrieren. Gründe für die Vermeidung der Selbstregistrierung:

-   Wenn eine Installation mit der TypeLib-Tabelle fehlschlägt und ein Rollback ausgeführt werden muss, wird der Computer vom Rollback möglicherweise nicht in demselben Zustand wieder hergestellt, der vor dem Rollback vorhanden war. Typbibliotheken, die vor dem Rollback registriert wurden, werden nach dem Rollback möglicherweise nicht registriert.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



