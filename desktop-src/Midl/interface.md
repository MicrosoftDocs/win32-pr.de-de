---
title: Schnittstellenattribut
description: Das Interface-Schlüsselwort gibt den Namen der Schnittstelle an. Der Schnittstellen Name muss sowohl in der IDL-Datei als auch in der ACF angegeben werden.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- Schnittstellen Attribut-Mittel l
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858186"
---
# <a name="interface-attribute"></a>Schnittstellenattribut

Das **Interface** -Schlüsselwort gibt den Namen der Schnittstelle an. Der Schnittstellen Name muss sowohl in der IDL-Datei als auch in der ACF angegeben werden.

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt Attribute an, die auf die gesamte Schnittstelle angewendet werden. Gültige Schnittstellen Attribute für eine IDL-Datei sind **\[** [**EndPoint**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**Object**](object.md) **\]** , **\[** [**Zeiger \_ Standard**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** und **\[** [**Version**](version.md) **\]** . Gültige Schnittstellen Attribute für eine ACF sind z **\[** . b. [**Codieren**](encode.md) **\]** , **\[** [**decodieren**](decode.md) **\]** , entweder **\[** [**Automatisches \_ handle**](auto-handle.md) **\]** oder **\[** [**implizites \_ handle**](implicit-handle.md) **\]** und entweder **\[** [**Code**](code.md) **\]** oder **\[** [**NoCode**](nocode.md) **\]** .

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an. Der Schnittstellen Name muss ein eindeutiger Name sein und muss mit einem Buchstaben oder einem Unterstrich beginnen.

</dd> <dt>

*Basisschnittstelle* 
</dt> <dd>

Gibt den Namen einer Schnittstelle an, von der diese abgeleitete Schnittstelle Member-Funktionen, Statuscodes und Schnittstellen Attribute erbt. Die abgeleitete Schnittstelle erbt keine Typdefinitionen. Verwenden Sie hierzu das Schlüsselwort [**Import**](import.md) , um die IDL-Datei der Basisschnittstelle zu importieren.

</dd> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Schnittstellennamen in der IDL-Datei und der ACF müssen identisch sein, es sei denn, Sie verwenden den Mittelwert des Compilerschalters [**/ACF**](-acf.md).

Der Schnittstellen Name bildet den ersten Teil des Namens von Schnittstellen handle-Datenstrukturen, die Parameter für die RPC-Lauf Zeitfunktionen sind. Weitere Informationen finden Sie unter [**RPC- \_ if- \_ handle**](/windows/desktop/Rpc/rpc-if-handle).

Wenn der Schnittstellen Header das Object-Attribut enthält, **\[** [](object.md) **\]** um eine COM-Schnittstelle anzugeben, muss er auch das **\[** [**UUID**](uuid.md) **\]** -Attribut enthalten und muss die Basis-com-Schnittstelle angeben, von der er abgeleitet ist. Weitere Informationen zu COM-Schnittstellen finden Sie unter **\[** [**Object**](object.md) **\]** .

Sie können auch das **Interface** -Schlüsselwort mit dem [**typedef**](typedef.md) -Schlüsselwort verwenden, um einen Schnittstellen Datentyp zu definieren.

## <a name="examples"></a>Beispiele

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Dreher**](endpoint.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**Zeiger \_ Standard**](pointer-default.md)
</dt> <dt>

[**RPC- \_ if- \_ handle**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 