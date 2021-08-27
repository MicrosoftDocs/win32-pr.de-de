---
title: user_marshal-Attribut
description: Das ACF-Attribut des Benutzers ordnet einen benannten lokalen Typ in der Zielsprache (userm-type) einem Übertragungstyp (Wire-Type) zu, der zwischen Client und Server \_ übertragen wird.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal MIDL-Attribut
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f17b4ef9d4376309307403ee12e2c5aae507556beaf091f9d742998d18671a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105570"
---
# <a name="user_marshal-attribute"></a>User \_ Marshal-Attribut

Das **\_ ACF-Attribut** des Benutzers ordnet einen benannten lokalen Typ in der Zielsprache (*userm-type*) einem Übertragungstyp (*wire-type*) zu, der zwischen Client und Server übertragen wird.

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*userm-type* 
</dt> <dd>

Gibt den Bezeichner des benutzerdatentyps an, der gemarshallt werden soll. Der *userm-type muss* nicht übertragbar sein und muss kein Typ sein, der dem MIDL-Compiler bekannt ist.

</dd> <dt>

*wire-type* 
</dt> <dd>

Gibt den benannten Übertragungsdatentyp an, der tatsächlich zwischen Client und Server übertragen wird. Der Wire-Typ muss ein MIDL-Basistyp, ein vordefinierter Typ oder ein Typbezeichner eines Typs sein, der über das Netzwerk übertragen werden kann.

</dd> <dt>

*pFlags* 
</dt> <dd>

Gibt einen Zeiger auf ein Flagfeld an ( [**unsigned**](unsigned.md) [**long**](long.md)). Das obere Wort gibt NDR-Datendarstellungsflags an, die von DCE für Gleitkomma-, Big- oder Little-Endian- und Zeichendarstellung definiert werden. Das niedrige Wort gibt ein Marshallingkontextflag an. Das genaue Layout der Flags wird unter Der Typ [ \_ UserSize-Funktion beschrieben.](/windows/desktop/Rpc/the-type-usersize-function)

</dd> <dt>

*StartingSize* 
</dt> <dd>

Gibt die aktuelle Puffergröße (Offset) an, bevor die Größe des Objekts festgelegt wird.

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

Gibt einen Zeiger auf ein Objekt vom *Typ userm \_ an.*

</dd> <dt>

*Buffer* 
</dt> <dd>

Gibt den aktuellen Pufferzeiger an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Jeder benannte lokale Typ, *userm-type,* verfügt über eine 1:1-Entsprechung mit einem Wire-Typ, der die *Wire-Darstellung* des Typs definiert. Sie müssen Routinen zur Größengröße der Daten für das Marshalling, zum Marshallen und Zum Unmarshalieren der Daten und zum Freien von Arbeitsspeicher verwenden. Weitere Informationen zu diesen Routinen finden Sie unter [Das \_ Benutzer-Marshallattribut](/windows/desktop/Rpc/the-user-marshal-attribute). Beachten Sie, dass Sie die Wartung dieser **\_** eingebetteten Typen auch verwalten müssen, wenn ihre Daten eingebettete Typen sind, die auch mit dem Marshalling oder dem \[ [**\[ Wire \_ Marshal \]**](wire-marshal.md)des Benutzers definiert sind.

Der *wire-type darf* kein Schnittstellenzeiger oder ein vollständiger Zeiger sein. Der *Wire-Typ muss* eine klar definierte Arbeitsspeichergröße haben. Weitere Informationen zum Marshallen eines bestimmten *Wire-Typs* finden Sie unter Marshallingregeln für das Marshallen von Benutzer und [ \_ Wire \_ Marshal.](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal)

Der *userm-type sollte* kein Schnittstellenzeiger sein, da diese direkt gemarshallt werden können. Wenn der Benutzertyp ein vollständiger Zeiger ist, müssen Sie das Aliasing selbst verwalten.

## <a name="examples"></a>Beispiele

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**darstellen \_ als**](represent-as.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[Das \_ Marshallattribut des Benutzers](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**Wire \_ Marshal**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 