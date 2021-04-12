---
title: wire_marshal-Attribut
description: Das Attribut \ Wire \_ Marshal \ gibt einen Datentyp an, der anstelle eines anwendungsspezifischen Datentyps (dem userm-Type) für die Übertragung verwendet wird (der Wire-Typ).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- Wire_marshal Attribut-Mittel l
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391143"
---
# <a name="wire_marshal-attribute"></a>Wire \_ Marshal-Attribut

Das **\[ Wire \_ Marshal \]** -Attribut gibt einen Datentyp an, der anstelle eines anwendungsspezifischen Datentyps (dem *userm-Type*) für die Übertragung verwendet wird (der *Wire-Typ*).

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Wire-Type* 
</dt> <dd>

Gibt den benannten Übertragungs Datentyp an, der zwischen Client und Server tatsächlich übertragen wird. Der Typ " *Wire-Type* " muss ein Basistyp der Mitte, ein vordefinierter Typ oder ein Typbezeichner eines Typs sein, der über das Netzwerk übertragen werden kann.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Der Typ, für den *userm-Type* zu einem Alias wird.

</dd> <dt>

*User m-Type* 
</dt> <dd>

Gibt den Bezeichner des Benutzer Datentyps an, der gemarshallt werden soll. Dies kann ein beliebiger Typ sein, wie er vom *Typspezifizierer* angegeben wird, sofern er über eine klar definierte Größe verfügt. Der *userm-Typ* muss nicht transaktionabel sein, muss jedoch ein Typ sein, der dem Mittelwert Compiler bekannt ist.

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

Gibt einen Zeiger auf ein Objekt des *userm- \_ Typs an.*

</dd> <dt>

*Buffer* 
</dt> <dd>

Gibt den aktuellen Puffer Zeiger an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Jeder anwendungsspezifische Datentyp, *userm-Type,* weist eine eins-zu-eins-Entsprechung mit einem *Wire-Typ* auf, der die Wire-Darstellung des Typs definiert. Sie müssen Routinen bereitstellen, um die Größe der Daten für das Marshalling, das Mars Hallen und das Entsperren der Daten und das Freigeben von Arbeitsspeicher zu verkleinern. Beachten Sie Folgendes: Wenn in den Daten eingebettete Typen vorhanden sind, die auch mit **\[ Wire \_ \] Marshal** oder **\[** [**User \_ Marshal**](user-marshal.md)definiert sind **\]** , müssen Sie die Wartung dieser eingebetteten Typen ebenfalls verwalten. Weitere Informationen zu diesen Routinen finden Sie [unter dem Wire \_ Marshal-Attribut](/windows/desktop/Rpc/the-wire-marshal-attribute).

Ihre Implementierung muss gemäß der OSF-DCE-Spezifikation den Marshalling-Regeln folgen. Details zur Syntax der NDR-Übertragung finden Sie unter [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) . Es wird nicht empfohlen, **\[ Wire \_ Marshal \]** zu verwenden, wenn Sie mit dem Wire-Protokoll nicht vertraut sind.

Der *Wire-Type* darf kein Schnittstellen Zeiger oder ein vollständiger Zeiger sein. Der *Wire-Typ* muss eine klar definierte Arbeitsspeicher Größe aufweisen. Ausführliche Informationen zum Mars Hallen eines bestimmten Netzwerk *Typs* finden Sie unter [Mars Hallen von Regeln für Benutzer \_ Mars Hall und Wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .

Der *userm-Type* darf kein Schnittstellen Zeiger sein, da diese direkt gemarshallt werden können. Wenn der Benutzertyp ein vollständiger Zeiger ist, müssen Sie das Aliasing selbst verwalten.

Sie können das **\[ Wire \_ Marshal \]** -Attribut nicht direkt oder indirekt mit dem Attribut "Allocation" verwenden **\[** [](allocate.md) **\]** , da die NDR-Engine nicht die Speicher Belegung für den übertragenen Typ steuert.

## <a name="examples"></a>Beispiele

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[Datendarstellung](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**Ndrgetusermarshalinfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[Das Wire \_ Marshal-Attribut](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> <dt>

[**Benutzer \_ Mars Hall**](user-marshal.md)
</dt> </dl>

 

 