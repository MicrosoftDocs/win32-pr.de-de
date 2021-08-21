---
description: Die TypeLib-Tabelle enthält die Informationen, die in der Registrierungsregistrierung von Typbibliotheken platziert werden müssen.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: TypeLib-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862bc37e325f8c615e8158cfa431c927841f6b33c403c804726cea8fee6f0469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500000"
---
# <a name="typelib-table"></a>TypeLib-Tabelle

Die TypeLib-Tabelle enthält die Informationen, die in der Registrierungsregistrierung von Typbibliotheken platziert werden müssen.

Die TypeLib-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                               | Key | Nullwerte zulässig |
|-------------|------------------------------------|-----|----------|
| Libid       | [GUID](guid.md)                   | J   | N        |
| Sprache    | [Integer](integer.md)             | J   | N        |
| Komponente\_ | [Identifier](identifier.md)       | J   | N        |
| Version     | [DoubleInteger](doubleinteger.md) | N   | J        |
| BESCHREIBUNG | [Text](text.md)                   | N   | J        |
| Verzeichnis\_ | [Identifier](identifier.md)       | N   | J        |
| Feature\_   | [Identifier](identifier.md)       | N   | N        |
| Kosten        | [DoubleInteger](doubleinteger.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>Libid
</dt> <dd>

Die GUID, die die Bibliothek identifiziert.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sprache
</dt> <dd>

Die Sprache der Typbibliothek. Dies muss eine nicht negative Zahl sein.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Component-Tabelle.](component-table.md) Diese Spalte identifiziert die Komponente, die zu Feature \_ gehört, deren Schlüsseldatei die zu registrierende Typbibliothek ist.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Version
</dt> <dd>

Dies ist die Version der Bibliothek. Die Haupt- und Nebenversionen werden im Ganzzahlwert von vier Byte codiert. Die Nebenversion befindet sich in den unteren acht Bits. Die Hauptversion befindet sich in den mittleren 16 Bits.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine lokalisierbare Beschreibung der Bibliothek.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Verzeichnis\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Verzeichnistabelle](directory-table.md). Diese Spalte identifiziert den Hilfepfad für die Typbibliothek. Diese Spalte wird während der Ankündigung ignoriert.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Featuretabelle](feature-table.md). Diese Spalte gibt das Feature an, das installiert werden muss, damit die Typbibliothek betriebsbereit ist.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Kosten
</dt> <dd>

Die Kosten für die Registrierung der Typbibliothek in Bytes. Dies muss eine nicht negative Zahl oder NULL sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diese Tabelle wird verwiesen, wenn die [RegisterTypeLibraries-Aktion](registertypelibraries-action.md) oder die [UnregisterTypeLibraries-Aktion](unregistertypelibraries-action.md) ausgeführt wird.

Das Installationsprogramm schreibt alle Registrierungsinformationen der Typbibliothek in den Registrierungsspeicherort HKEY \_ LOCAL \_ MACHINE (HKLM). Dies gilt auch für benutzerspezifische Installationen. Typbibliotheken können nicht an Benutzerstandorten (HKCU) registriert werden.

Installationspaketautoren wird dringend davon abgeraten, die TypeLib-Tabelle zu verwenden. Stattdessen sollten Sie Typbibliotheken mithilfe der [Registrierungstabelle](registry-table.md) registrieren. Gründe für die Vermeidung der Selbstregistrierung sind:

-   Wenn bei einer Installation mit der TypeLib-Tabelle ein Fehler auftritt und ein Rollback ausgeführt werden muss, wird der Computer möglicherweise nicht in dem Zustand wiederhergestellt, der vor dem Rollback vorhanden war. Typbibliotheken, die vor dem Rollback registriert wurden, werden nach dem Rollback möglicherweise nicht registriert.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



