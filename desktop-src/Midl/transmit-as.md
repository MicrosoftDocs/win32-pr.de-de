---
title: transmit_as-Attribut
description: Das Attribut \transmit as\ weist den Compiler an, type-id, einen dargestellten Typ, den Client- und Serveranwendungen bearbeiten, einem übertragenen \_ Typ xmit-type zu zuordnen.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as MIDL-Attribut
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d1b8e9aae9a147c929fade8030babbf6b02fd87c9170370252522001742e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382830"
---
# <a name="transmit_as-attribute"></a>als \_ Attribut übertragen

Das **\[ Attribut transmit \_ as \]** weist den Compiler an, **type-id**_,_ einen dargestellten Typ, den Client- und Serveranwendungen bearbeiten, einem übertragenen **Typ xmit-type zu zuordnen.**

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*xmit-type* 
</dt> <dd>

Gibt den Datentyp an, der zwischen Client und Server übertragen wird.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die für den Typ gelten. Gültige Typattribute sind **\[** [**handle,**](handle.md) **\]** switch **\[** [**\_ type,**](switch-type.md)das **\]** Zeigerattribut **\[** [**ref,**](ref.md)unique oder ptr sowie die **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** Verwendungsattribute **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** string und ignore. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp, eine](midl-base-types.md) [**Struktur,**](struct.md)eine [**Union,**](union.md) [**einen Enum-Typ**](enum.md) oder einen Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer vorangestellt werden.*

</dd> <dt>

*declarator-list* 
</dt> <dd>

Gibt C-Standarddeklaratoren an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute,](array-and-sized-pointer-attributes.md) [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers) Die *Declaratorliste besteht* aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameterdeklarator im Funktionsdeklarator, z. B. der Parametername, ist optional.

</dd> <dt>

*type-id* 
</dt> <dd>

Gibt den Namen des Datentyps an, der den Client- und Serveranwendungen angezeigt wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um die **\[ Übertragung \_ \]** als Attribut verwenden zu können, muss der Benutzer Routinen angeben, die Daten zwischen den dargestellten und den übertragenen Typen konvertieren. Diese Routinen müssen auch arbeitsspeicherfrei sein, der für die konvertierten Daten verwendet wird. Das **\[ Attribut transmit \_ as \]** weist die Stubs an, die vom Benutzer bereitgestellten Konvertierungsroutinen auf aufruft.

Der übertragene *Typ xmit-type* muss in einen MIDL-Basistyp, einen vordefinierten Typ oder einen Typbezeichner auflösen. Weitere Informationen finden Sie unter [MIDL-Basistypen.](midl-base-types.md)

Der Benutzer muss die folgenden Routinen liefern.



| Routinename              | BESCHREIBUNG                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *type-id** \_ zu \_ xmit**   | Konvertiert Daten vom dargestellten Typ in den übertragenen Typ. Diese Routine ordnet Arbeitsspeicher für den übertragenen Typ und für alle Daten zu, auf die von Zeigern im übertragenen Typ verwiesen wird.                            |
| *type-id** \_ von \_ xmit** | Konvertiert Daten vom übertragenen Typ in den dargestellten Typ. Diese Routine ist für die Zuweisung von Arbeitsspeicher für Daten zuständig, auf die von Zeigern im dargestellten Typ verwiesen wird. RPC weist Arbeitsspeicher für den Typ selbst zu. |
| *type-id** \_ free \_ inst** | Gibt Arbeitsspeicher frei, der für Daten zugeordnet ist, auf die von Zeigern im dargestellten Typ verwiesen wird. RPC gibt Arbeitsspeicher für den Typ selbst frei.                                                                                               |
| *type-id** \_ free \_ xmit** | Gibt den vom Aufrufer verwendeten Speicher für den übertragenen Typ und für Daten frei, auf die von Zeigern im übertragenen Typ verwiesen wird.                                                                                            |



 

 

Der Clientstub ruft *type-id** \_ \_ auf, um xmit** zu verwenden, um Speicherplatz für den übertragenen Typ zu reservieren und die Daten in Objekte vom Typ *xmit-type zu übersetzen.* Der Serverstub weist Speicherplatz für den ursprünglichen Datentyp zu und ruft *type-id** von \_ \_ xmit** auf, um die Daten aus dem übertragenen Typ in den dargestellten Typ zu übersetzen.

Nach der Rückgabe aus dem Anwendungscode ruft der Serverstub *type-id* \_ free \_ inst** auf, um die Speicherbelegung für *type-id* auf serverseitiger Seite frei zu machen. Der Clientstub ruft *type-id** \_ free \_ xmit** auf, um die Speicherbelegung *des xmit-Typs* auf clientseitiger Seite frei zu machen.

Die folgenden Typen können keine Übertragung **\[ als \_ Attribut \]** haben:

-   Kontexthandles (Typen mit dem **\[** [**\_ Kontexthandles-Typattribut**](context-handle.md) und Typen, die als Parameter mit dem **\]** **\[ Kontexthandlesattribut \_ verwendet \]** werden)
-   Typen, die Pipes sind oder von Pipes abgeleitet sind
-   Datentypen, die als Basistyp einer Pipedefinition verwendet werden
-   Parameter, die Zeiger sind oder in Zeiger auflösen
-   Parameter, die konformen, variierenden oder offenen Arrays entsprechen
-   Strukturen, die konforme Arrays enthalten
-   Der vordefinierte Typhand [**handle \_ t**](handle-t.md), [**void**](void.md)

Typen, die übertragen werden, müssen den folgenden Einschränkungen entsprechen:

-   Sie dürfen keine Zeiger sein oder Zeiger enthalten.
-   Sie dürfen keine Pipes sein oder Pipes enthalten.

## <a name="examples"></a>Beispiele

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Kontexthand \_ handle**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**Handlebezeichner**](handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorieren**](ignore.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> <dt>

[**Struktur**](struct.md)
</dt> <dt>

[**\_switch-Typ**](switch-type.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 