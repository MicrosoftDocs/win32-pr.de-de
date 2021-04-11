---
title: user_marshal-Attribut
description: Das \_ ACF-Attribut User Marshal ordnet einen benannten lokalen Typ in der Zielsprache (User m-Type) einem Übertragungstyp (Wire-Type) zu, der zwischen Client und Server übertragen wird.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal Attribut-Mittel l
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314798"
---
# <a name="user_marshal-attribute"></a>Benutzer \_ Mars Hall Attribut

Das ACF-Attribut **User \_ Marshal** ordnet einen benannten lokalen Typ in der Zielsprache (*User m-Type*) einem Übertragungstyp (*Wire-* Type) zu, der zwischen Client und Server übertragen wird.

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

*User m-Type* 
</dt> <dd>

Gibt den Bezeichner des Benutzer Datentyps an, der gemarshallt werden soll. Der *userm-Typ* muss nicht transaktierbar sein und muss kein Typ sein, der dem mittlerer l-Compiler bekannt ist.

</dd> <dt>

*Wire-Type* 
</dt> <dd>

Gibt den benannten Übertragungs Datentyp an, der zwischen Client und Server tatsächlich übertragen wird. Der Netzwerktyp muss ein Basistyp der Mitte, ein vordefinierter Typ oder ein Typbezeichner eines Typs sein, der über das Netzwerk übertragen werden kann.

</dd> <dt>

*pflags* 
</dt> <dd>

Gibt einen Zeiger auf ein Flagfeld an ( [**Ganzzahl ohne Vorzeichen**](unsigned.md) [**Long**](long.md)). Das höchst wertige Wort gibt die von DCE für Gleit Komma-, Big-oder Little-Endian-und Zeichen Darstellung definierten Daten darstellungenflags der NDR-Daten an. Mit dem nieder wertigen Wort wird ein marshallingkontextflag angegeben. Das genaue Layout der Flags wird in [der Type \_ usersize-Funktion](/windows/desktop/Rpc/the-type-usersize-function)beschrieben.

</dd> <dt>

*Startingsize* 
</dt> <dd>

Gibt die aktuelle Puffergröße (Offset) vor der Größenanpassung des Objekts an.

</dd> <dt>

*puser \_ TypeObject* 
</dt> <dd>

Gibt einen Zeiger auf ein Objekt des *userm- \_ Typs* an.

</dd> <dt>

*Buffer* 
</dt> <dd>

Gibt den aktuellen Puffer Zeiger an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Jeder benannte lokale Typ, *userm-Type*, weist eine eins-zu-eins-Entsprechung mit einem *Wire-Typ* auf, der die Wire-Darstellung des Typs definiert. Sie müssen Routinen bereitstellen, um die Größe der Daten für das Marshalling, das Mars Hallen und das Entsperren der Daten und das Freigeben von Arbeitsspeicher zu verkleinern. Weitere Informationen zu diesen Routinen finden Sie [unter User \_ Marshal Attribute](/windows/desktop/Rpc/the-user-marshal-attribute). Beachten Sie Folgendes: Wenn in den Daten eingebettete Typen vorhanden sind, die auch mit dem **Benutzer \_ Mars** Hall oder \[ dem [**\[ Wire \_ \] Marshal**](wire-marshal.md)definiert sind, müssen Sie die Wartung dieser eingebetteten Typen ebenfalls verwalten.

Der *Wire-Type* darf kein Schnittstellen Zeiger oder ein vollständiger Zeiger sein. Der *Wire-Typ* muss eine klar definierte Arbeitsspeicher Größe aufweisen. Ausführliche Informationen zum Mars Hallen eines bestimmten Netzwerk *Typs* finden Sie unter [Mars Hallen von Regeln für Benutzer \_ Mars Hall und Wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .

Der *userm-Type* darf kein Schnittstellen Zeiger sein, da diese direkt gemarshallt werden können. Wenn der Benutzertyp ein vollständiger Zeiger ist, müssen Sie das Aliasing selbst verwalten.

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

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**Darstellung \_ als**](represent-as.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> <dt>

[Das Mars-Attribut des Benutzers \_](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**Wire \_ Marshal**](wire-marshal.md)
</dt> <dt>

[**Ndrgetusermarshalinfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 