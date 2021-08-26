---
description: Die Tabelle ProgId enthält Informationen zu Programm-IDs und versionsunabhängigen Programm-IDs, die im Rahmen der Produktankündigung generiert werden müssen.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: ProgId-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed8baea9bd8421757cf2e31f0ba06679db3394c95f732537a7e230c02b5ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042060"
---
# <a name="progid-table"></a>ProgId-Tabelle

Die Tabelle ProgId enthält Informationen zu Programm-IDs und versionsunabhängigen Programm-IDs, die im Rahmen der Produktankündigung generiert werden müssen.

Die Tabelle ProgId enthält die folgenden Spalten.



| Spalte         | Typ                         | Key | Nullwerte zulässig |
|----------------|------------------------------|-----|----------|
| ProgId         | [Text](text.md)             | J   | N        |
| ProgId \_ Parent | [Text](text.md)             | N   | J        |
| Klasse\_        | [GUID](guid.md)             | N   | J        |
| BESCHREIBUNG    | [Text](text.md)             | N   | J        |
| Symbol\_         | [Identifier](identifier.md) | N   | J        |
| IconIndex      | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>Progid
</dt> <dd>

Die Programm-ID oder versionsunabhängige Programm-ID. ProgIds, die in der ProgId-Tabelle aufgeführt sind, werden registriert, wenn die CLSID, die in der Spalte Klasse dieser Tabelle aufgeführt \_ ist, angekündigt oder installiert werden soll. Wenn die ProgId für die Registrierung ausgewählt ist, werden alle ProgIds, die über die Spalte ProgId Parent auf diese Zeile verweisen, ebenfalls für die \_ Registrierung ausgewählt.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ Parent
</dt> <dd>

Nur für versionsunabhängige Programm-IDs definiert. Dieses Feld ist ein Fremdschlüssel in der ProgId-Spalte. Um eine versionsunabhängige Programm-ID zu definieren, geben Sie die entsprechende ProgId in die Spalte ProgId \_ Parent ein. Wenn die ProgId für die Installation ausgewählt ist, werden die entsprechenden versionsunabhängigen ProgIds, die über die Spalte ProgId Parent zugeordnet sind, ebenfalls für die \_ Registrierung ausgewählt.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Klasse\_
</dt> <dd>

Ein optionaler Fremdschlüssel in der [Class-Tabelle.](class-table.md) Diese Spalte muss null für eine versionsunabhängige ProgId sein. Wenn der \_ Class-Wert für eine ProgId NULL ist, wird die ProgId registriert, wenn sie in der ProgId-Spalte einer Zeile in der [Extension-Tabelle](extension-table.md) angezeigt wird und der Erweiterung mindestens ein Verb in der [Verb-Tabelle](verb-table.md)zugeordnet ist. ProgIds, die auf diese Weise für die Registrierung ausgewählt wurden, installieren keine anderen ProgIds, die über den ProgId-Standardwert auf die aktuelle ProgId \_ verweisen.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine optionale lokalisierte Beschreibung der zugeordneten Programm-ID.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Symbol\_
</dt> <dd>

Ein optionaler Fremdschlüssel in der [Symboltabelle,](icon-table.md) der die Symboldatei angibt, die dieser ProgId zugeordnet ist. Dies wird unter dem DefaultIcon-Schlüssel geschrieben, der dieser ProgId zugeordnet ist. Diese Spalte muss null für eine versionsunabhängige ProgId sein.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Der Symbolindex in der Symboldatei. Diese Spalte muss null für eine versionsunabhängige ProgId sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Aktionen [RegisterProgIdInfo](registerprogidinfo-action.md) und [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in [*Sequenztabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen* finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



