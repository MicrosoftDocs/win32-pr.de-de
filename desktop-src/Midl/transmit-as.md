---
title: transmit_as-Attribut
description: Das Attribut \ überträgt \_ As \ weist den Compiler an, Type-ID zuzuordnen, bei dem es sich um einen dargestellten Typ handelt, der von Client-und Server Anwendungen bearbeitet wird, wobei der übertragene Typ xmit-Type ist.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- Transmit_as Attribut-Mittel l
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337644"
---
# <a name="transmit_as-attribute"></a>\_als Attribut übertragen

Das Attribut "über **\[ tragen \_ als \]** " weist den Compiler an *, * Type-ID * * * zuzuordnen,* bei dem es sich um einen dargestellten Typ handelt, den Client-und Server Anwendungen mit einem übertragenen Typ " **xmit-Type** " bearbeiten.

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

*xmit-Typ* 
</dt> <dd>

Gibt den Datentyp an, der zwischen Client und Server übertragen wird.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die **\[** [**Zeichenfolge**](string.md) der Verwendungs Attribute **\]** und **\[** [**Ignore**](ignore.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.

</dd> <dt>

*Typ-ID* 
</dt> <dd>

Gibt den Namen des Datentyps an, der den Client-und Server Anwendungen angezeigt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um das Attribut "über **\[ tragen \_ als \]** " zu verwenden, muss der Benutzer Routinen bereitstellen, mit denen Daten zwischen den dargestellten und übertragenen Typen konvertiert werden. diese Routinen müssen auch Speicher freigeben, der zum Speichern der konvertierten Daten verwendet wird. Das Attribut "über **\[ tragen \_ als \]** " weist die stubzeichen an, die vom Benutzer bereitgestellten Konvertierungs Routinen aufzurufen.

Der übertragene Typ " *xmit-Type* " muss in einen mittleren Basistyp, vordefinierten Typ oder einen Typbezeichner aufgelöst werden. Weitere Informationen finden Sie unter [Mittel l-Basis Typen](midl-base-types.md).

Der Benutzer muss die folgenden Routinen bereitstellen.



| Routine Name              | BESCHREIBUNG                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Type-ID * * * \_ bis \_ xmit**   | Konvertiert Daten aus dem dargestellten Typ in den übertragenen Typ. Diese Routine weist Speicher für den übertragenen Typ und für alle Daten zu, auf die von Zeigern im übertragenen Typ verwiesen wird.                            |
| *Type-ID * * * \_ from \_ xmit** | Konvertiert Daten aus dem übertragenen Typ in den dargestellten Typ. Diese Routine ist für die Zuweisung von Speicher für Daten reserviert, auf die von Zeigern im dargestellten Typ verwiesen wird. RPC ordnet Speicher für den Typ selbst zu. |
| *Type-ID * * * \_ freie \_ inst** | Gibt für Daten, auf die Zeiger im dargestellten Typ verweisen, zugeordneten Arbeitsspeicher frei. RPC gibt Arbeitsspeicher für den Typ selbst frei.                                                                                               |
| *Type-ID * * * \_ freie \_ xmit** | Gibt Speicher frei, der vom Aufrufer für den übertragenen Typ verwendet wird, sowie für Daten, auf die Zeiger im übertragenen Typ verweisen.                                                                                            |



 

 

Der Clientstub ruft *Type-ID * * * \_ in \_ xmit** auf, um Speicherplatz für den übertragenen Typ zuzuweisen und die Daten in Objekte vom Typ *xmit-Type* zu übersetzen. Der Serverstub ordnet Speicherplatz für den ursprünglichen Datentyp zu und ruft *Type-ID * * * \_ von \_ xmit** auf, um die Daten vom übertragenen Typ in den dargestellten Typ zu übersetzen.

Bei Rückgabe aus dem Anwendungscode ruft der Server-Stub *Type-ID * * * \_ Free \_ inst** auf, um den Speicher für *Type-ID* auf Serverseite freizugeben. Der Clientstub ruft *Type-ID * * * \_ Free \_ xmit** auf, um den *xmit-Typspeicher* auf der Clientseite freizugeben.

Die folgenden Typen können kein Attribut "über **\[ tragen \_ als \]** " aufweisen:

-   Kontext Handles (Typen mit dem **\[** Kontotyp Attribut des [**Kontext \_ Handles**](context-handle.md) **\]** ) und Typen, die als Parameter mit dem **\[ Kontext \_ \] handle** -Attribut verwendet werden.
-   Typen, die Pipes sind oder von Pipes abgeleitet sind
-   Datentypen, die als Basistyp einer Pipe-Definition verwendet werden
-   Parameter, die Zeiger sind oder zu Zeigern aufgelöst werden
-   Parameter, die konforme, abweichende oder geöffnete Arrays sind
-   Strukturen, die konforme Arrays enthalten
-   Das vordefinierte [**Typhandle \_ t**](handle-t.md), [**void**](void.md)

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

[**Mikro**](arrays-1.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[**bewältigen**](handle.md)
</dt> <dt>

[**Handle \_ t**](handle-t.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**\_Switchtyp**](switch-type.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 