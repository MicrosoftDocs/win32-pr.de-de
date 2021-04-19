---
description: Die Verb Tabelle enthält Befehls Verb Informationen, die Dateinamen Erweiterungen zugeordnet sind und als Teil der Produktankündigung generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungs Schlüsseln und-Werten.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Verb Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366520"
---
# <a name="verb-table"></a>Verb Tabelle

Die Verb Tabelle enthält Befehls Verb Informationen, die Dateinamen Erweiterungen zugeordnet sind und als Teil der Produktankündigung generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungs Schlüsseln und-Werten.

Die Verb Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                       | Schlüssel | Nullwerte zulässig |
|-------------|----------------------------|-----|----------|
| Durchwahl\_ | [Text](text.md)           | J   | N        |
| Verb        | [Text](text.md)           | J   | N        |
| Sequenz    | [Integer](integer.md)     | N   | J        |
| Get-Help     | [Großformatige](formatted.md) | N   | J        |
| Argument    | [Großformatige](formatted.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Weiterung\_
</dt> <dd>

Die der Tabellenzeile zugeordnete Erweiterung. Diese Spalte ist ein externer Schlüssel für die erste Spalte der [Erweiterungs Tabelle](extension-table.md).

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Ben
</dt> <dd>

Das Verb für den Befehl.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Sequenz der Befehle. Nur Verben, für die die Sequenz Spalte ungleich NULL ist, werden verwendet, um eine geordnete Liste für den Standardwert des shellschlüssels vorzubereiten. Das Verb mit dem niedrigsten Wert in dieser Spalte wird zum Standardverb.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>S
</dt> <dd>

Der lokalisierbare Text, der im Kontextmenü angezeigt wird.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Gestritten
</dt> <dd>

Der Wert für die Befehlsargumente.

Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argument eingeschränkt ist. Eine Eigenschaft, die als \[ *Eigenschaft* \] in diesem Feld formatiert ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits den vorgesehenen Wert aufweist, wenn die Komponente, die das Verb besitzt, installiert ist. Damit das Argument "MyDoc.doc" z. b. \[ \# \] in den richtigen Wert aufgelöst wird, muss der gleiche Prozess die Datei MyDoc.doc und die Komponente, die das Verb besitzt, installieren.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Tabelle wird beim Ausführen der [RegisterExtensionInfo-Aktion](registerextensioninfo-action.md) oder der [unregisterextensioninfo-Aktion](unregisterextensioninfo-action.md) bezeichnet.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



