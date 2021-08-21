---
description: Die Tabelle Verb enthält Befehlsverbinformationen, die Dateinamenerweiterungen zugeordnet sind, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungsschlüsseln und -werten.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Verbtabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fc546cd3db5fecb3861120fa15b1ffa3f21327b889599b77a1b067193c886c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499110"
---
# <a name="verb-table"></a>Verbtabelle

Die Tabelle Verb enthält Befehlsverbinformationen, die Dateinamenerweiterungen zugeordnet sind, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungsschlüsseln und -werten.

Die Verb-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                       | Key | Nullwerte zulässig |
|-------------|----------------------------|-----|----------|
| Erweiterung\_ | [Text](text.md)           | J   | N        |
| Verb        | [Text](text.md)           | J   | N        |
| Sequenz    | [Integer](integer.md)     | N   | J        |
| Get-Help     | [Formatiert](formatted.md) | N   | J        |
| Argument    | [Formatiert](formatted.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Erweiterung\_
</dt> <dd>

Die der Tabellenzeile zugeordnete Erweiterung. Diese Spalte ist ein externer Schlüssel für die erste Spalte der [Erweiterungstabelle](extension-table.md).

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb
</dt> <dd>

Das Verb für den Befehl.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Sequenz der Befehle. Nur Verben, für die die Sequenzspalte ungleich NULL ist, werden verwendet, um eine sortierte Liste für den Standardwert des Shellschlüssels vorzubereiten. Das Verb mit dem niedrigsten Wert in dieser Spalte wird zum Standardverb.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Befehl
</dt> <dd>

Der lokalisierbare Text, der im Kontextmenü angezeigt wird.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Wert für die Befehlsargumente.

Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argument eingeschränkt ist. Eine Eigenschaft, die in diesem Feld als Eigenschaft formatiert \[  \] ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits über den beabsichtigten Wert verfügt, wenn die Komponente installiert wird, die das Verb besitzt. Für das Argument "MyDoc.doc" muss beispielsweise \[ \# der gleiche Prozess die Datei MyDoc.doc und \] die Komponente installieren, die das Verb besitzt, um den richtigen Wert aufzulösen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diese Tabelle wird verwiesen, wenn die [RegisterExtensionInfo-Aktion](registerextensioninfo-action.md) oder die [UnregisterExtensionInfo-Aktion](unregisterextensioninfo-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



