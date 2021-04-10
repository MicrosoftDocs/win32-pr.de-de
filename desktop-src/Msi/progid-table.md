---
description: Die ProgID-Tabelle enthält Informationen zu Programm-IDs und Versions unabhängigen Programm-IDs, die als Teil der Produktankündigung generiert werden müssen.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: ProgID-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960758"
---
# <a name="progid-table"></a>ProgID-Tabelle

Die ProgID-Tabelle enthält Informationen zu Programm-IDs und Versions unabhängigen Programm-IDs, die als Teil der Produktankündigung generiert werden müssen.

Die ProgID-Tabelle weist die folgenden Spalten auf.



| Spalte         | Typ                         | Schlüssel | Nullwerte zulässig |
|----------------|------------------------------|-----|----------|
| ProgId         | [Text](text.md)             | J   | N        |
| ProgID \_ übergeordnet | [Text](text.md)             | N   | J        |
| Klasse\_        | [GUID](guid.md)             | N   | J        |
| BESCHREIBUNG    | [Text](text.md)             | N   | J        |
| Symbol\_         | [Bezeichner](identifier.md) | N   | J        |
| IconIndex      | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgID
</dt> <dd>

Die Programm-ID oder Versions unabhängige Programm-ID. Die in der ProgID-Tabelle aufgeführten ProgIDs werden registriert, wenn die in der Class-Spalte der Tabelle aufgeführte CLSID \_ angekündigt oder installiert wird. Wenn die ProgID für die Registrierung ausgewählt ist, werden alle ProgIDs, die auf diese Zeile über die übergeordnete ProgID-Spalte verweisen, \_ ebenfalls für die Registrierung ausgewählt.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgID \_ übergeordnet
</dt> <dd>

Nur für Versions unabhängige Programm-IDs definiert. Dieses Feld ist ein Fremdschlüssel in die ProgID-Spalte. Um eine Versions unabhängige Programm-ID zu definieren, geben Sie die entsprechende ProgID in die übergeordnete ProgID- \_ Spalte ein. Wenn die ProgID für die Installation ausgewählt ist, werden die entsprechenden Versions unabhängigen ProgIDs, die über die übergeordnete Spalte ProgID verknüpft \_ sind, ebenfalls für die Registrierung ausgewählt.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Klassi\_
</dt> <dd>

Ein optionaler Fremdschlüssel in die [Klassen Tabelle](class-table.md). Diese Spalte muss für eine Versions unabhängige ProgID NULL sein. Wenn der Klassen \_ Wert für eine ProgID NULL ist, wird die ProgID registriert, wenn Sie in der ProgID-Spalte einer Zeile in der [Erweiterungs Tabelle](extension-table.md) angezeigt wird und der Erweiterung mindestens ein Verb in der [Verb Tabelle](verb-table.md)zugeordnet ist. Bei der auf diese Weise für die Registrierung ausgewählten ProgIDs werden andere Programm-IDs, die auf die aktuelle ProgID verweisen, nicht mithilfe des ProgID- \_ Standardwerts installiert.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine optionale lokalisierte Beschreibung der zugeordneten Programm-ID.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Angezeigt\_
</dt> <dd>

Ein optionaler Fremdschlüssel in der [Symboltabelle](icon-table.md) , der die Symbol Datei angibt, die dieser ProgID zugeordnet ist. Diese wird unter dem DefaultIcon-Schlüssel geschrieben, der dieser ProgID zugeordnet ist. Diese Spalte muss für eine Versions unabhängige ProgID NULL sein.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Der Symbol Index in die Symbol Datei. Diese Spalte muss für eine Versions unabhängige ProgID NULL sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Aktionen [registerprogidinfo](registerprogidinfo-action.md) und [unregisterprogidinfo](unregisterprogidinfo-action.md) in [*Sequenz Tabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



