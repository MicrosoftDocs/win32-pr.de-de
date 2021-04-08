---
title: implicit_handle-Attribut
description: Das Attribut \ implizites \_ handle \ ACF gibt das Handle an, das für Funktionen verwendet wird, die kein explizites Handle als Prozedur Parameter enthalten.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857228"
---
# <a name="implicit_handle-attribute"></a>impliziertes \_ handle-Attribut

Das **\[ implizite \_ handle \]** -ACF-Attribut gibt das Handle an, das für Funktionen verwendet wird, die kein explizites Handle als Prozedur Parameter enthalten.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle-Typ* 
</dt> <dd>

Gibt den Datentyp des Handles an, z. b. das Basistyp [**handle \_ t**](handle-t.md) oder einen benutzerdefinierten Handlertyp.

</dd> <dt>

*Handle-Name* 
</dt> <dd>

Gibt den Namen des Handles an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das vom **\[ impliziten \_ handle \]** angegebene Handle wird abhängig von der Art der Prozedur auf unterschiedliche Weise verwendet. Wenn die Prozedur Remote ist, wird das Handle als Bindungs Handle für den Remote-Befehl verwendet. Das implizite Handle kann auch verwendet werden, um eine anfängliche Bindung für eine Funktion einzurichten, die ein Kontext Handle verwendet. Wenn es sich bei der Prozedur um eine Serialisierungsprozedur handelt, wird das Handle als serialisierungshandle verwendet, das den Vorgang steuert. Bei der Typserialisierung wird das Handle als serialisierungshandle für alle serialisierten Typen verwendet.

Das **\[ implizite \_ handle \]** -Attribut gibt eine globale Variable an, die ein Handle enthält, das von jeder Funktion verwendet wird, die implizite Handles benötigt.

Der Typ des impliziten Bindungs Handles muss entweder [**handle \_ t**](handle-t.md) (oder ein Typ, der auf **handle \_ t** basiert) oder ein benutzerdefinierter Handlertyp sein, der mit dem [**handle**](handle.md) -Attribut angegeben wird. Der implizite serialisierungshandle muss ein Typ sein, der auf **handle \_ t** basiert.

Wenn der implizite Handlertyp nicht in der IDL-Datei oder in Dateien definiert ist, die von der IDL-Datei für den mittleren Computer eingeschlossen und importiert werden, müssen Sie beim Kompilieren der Stubdateien die Datei angeben, die die Handle-Type-Definition enthält. Verwenden Sie die ACF [**include**](include.md) -Anweisung, um die Datei einzufügen, die die Handle-Type-Definition enthält.

Das **\[ implizite \_ handle \]** -Attribut kann höchstens einmal auftreten. Das **\[ implizite \_ handle \]** -Attribut kann nur auftreten, wenn die Attribute des [**\[ automatischen \_ Handles \]**](auto-handle.md) und des [**\[ expliziten \_ Handles \]**](explicit-handle.md) nicht auftreten.

## <a name="examples"></a>Beispiele

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Automatisches \_ handle**](auto-handle.md)
</dt> <dt>

[**explizites \_ handle**](explicit-handle.md)
</dt> <dt>

[**Handle \_ t**](handle-t.md)
</dt> <dt>

[**darunter**](include.md)
</dt> </dl>

 

 




