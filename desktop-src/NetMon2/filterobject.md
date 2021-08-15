---
description: Definiert ein einzelnes Objekt eines Anzeigefilters.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: FILTEROBJECT-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6a8da526eb60d8d581ca10e24f87a78b91492c4c043e6322eebe6a2ca0ebfd10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795783"
---
# <a name="filterobject-structure"></a>FILTEROBJECT-Struktur

Die **FILTEROBJECT-Struktur** definiert ein einzelnes Objekt eines Anzeigefilters. Die [**FilterAddObject-Funktion**](filteraddobject.md) verwendet **FILTEROBJECT,** um einen Anzeigefilter zu erstellen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a>Member

<dl> <dt>

**Aktion**
</dt> <dd>

Flag, das die **FILTEROBJECT-Aktion** angibt. Ein Flag kann eine Eigenschaft, einen Wert oder einen Operator angeben.

In der folgenden Tabelle sind Eigenschaftenflags für Aktionsmember aufgeführt.



| Wert                                                                                                                                                                                                | Bedeutung                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**\_FILTERACTION-EIGENSCHAFT**</dt> </dl>                | Enthält diese Eigenschaft.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**FILTERACTION \_ PROPERTYEXIST**</dt> </dl> | Gibt an, dass eine Filteraktionseigenschaft bereits definiert ist.<br/> |



 

Die folgende Tabelle enthält Flags für Aktionsmemberwerte.



| Wert                                                                                                                                                                                        | Bedeutung                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**\_FILTERACTION-WERT**</dt> </dl>                 | Enthält diesen Wert.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**FILTERACTION \_ STRING**</dt> </dl>              | Enthält diese Zeichenfolge.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**FILTERACTION \_ ARRAY**</dt> </dl>                 | Enthält dieses Array.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**FILTERACTION \_ CONTAINSNC**</dt> </dl>  | Gibt an, dass eine Eigenschaft eine Teilzeichenfolge enthält, bei der die Groß-/Kleinschreibung nicht beachtet wird.<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**FILTERACTION \_ CONTAINS**</dt> </dl>        | Gibt an, dass eine Eigenschaft eine Teilzeichenfolge enthält, bei der die Groß-/Kleinschreibung beachtet wird.<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**FILTERACTION \_ ADDRESS**</dt> </dl>           | Enthält die MAC-Adresse.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**FILTERACTION \_ ADDRESSANY**</dt> </dl>  | Entspricht einer beliebigen MAC-Adresse.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**FILTERACTION \_ FROM**</dt> </dl>                    | Gibt die **From MAC-Adresse** an.<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**FILTERACTION \_ TO**</dt> </dl>                          | Gibt die **To MAC-Adresse an.**<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**FILTERACTION \_ FROMTO**</dt> </dl>              | Gibt eine **From/To-Kopplung** von MAC-Adressen an.<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**FILTERACTION \_ LARGEINT**</dt> </dl>        | Enthält eine große ganze Zahl.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**FILTERACTION \_ TIME**</dt> </dl>                    | Enthält eine **SYSTEMTIME-Struktur.**<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**FILTERACTION \_ ADDR \_ ETHER**</dt> </dl> | Enthält eine Ethernet-MAC-Adresse.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**FILTERACTION \_ ADDR \_ TOKEN**</dt> </dl> | Enthält eine MAC-Adresse für den Tokenring.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**FILTERACTION \_ ADDR \_ FDDI**</dt> </dl>    | Enthält eine FDDI-MAC-Adresse.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**FILTERACTION \_ ADDR \_ IPX**</dt> </dl>       | Enthält eine IPX-MAC-Adresse.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**FILTERACTION \_ ADDR \_ IP**</dt> </dl>          | Enthält eine IP-MAC-Adresse.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**\_FILTERACTION-OID**</dt> </dl>                       | Enthält einen Objektbezeichner (Object Identifier, OID).<br/>                             |



 

In der folgenden Tabelle sind Die Operatorflags für Aktionsmember aufgeführt.



| Wert                                                                                                                                                                                                        | Bedeutung                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**FILTERACTION \_ INVALID**</dt> </dl>                           | Gibt eine ungültige Filteraktion an.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**FILTERACTION \_ UND**</dt> </dl>                                       | Gibt eine logische **AND-Anweisung** an.<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**FILTERACTION \_ ODER**</dt> </dl>                                          | Gibt eine logische **OR-Anweisung** an.<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**FILTERACTION \_ XOR**</dt> </dl>                                       | Gibt eine logische exklusive **OR-Anweisung** (XOR) an.<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**FILTERACTION \_ NOT**</dt> </dl>                                       | Gibt eine logische **NOT-Anweisung** an.<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**FILTERACTION \_ EQUALNC**</dt> </dl>                           | Die Filteraktion ist gleich, und die Groß-/Kleinschreibung wird nicht beachtet.<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**FILTERACTION \_ EQUAL**</dt> </dl>                                 | Die Filteraktion ist gleich, und die Groß-/Kleinschreibung wird beachtet.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**FILTERACTION \_ NOTEQUALNC**</dt> </dl>                  | Die logische **NOT-Anweisung** ist gleich, und die Groß-/Kleinschreibung wird nicht beachtet.<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**FILTERACTION \_ NOTEQUAL**</dt> </dl>                        | Die logische **NOT-Anweisung** ist gleich und berücksichtigt die Groß-/Kleinschreibung.<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**FILTERACTION \_ GREATERNC**</dt> </dl>                     | Die Filteraktion ist größer als (>), und die Groß-/Kleinschreibung wird nicht beachtet.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**FILTERACTION \_ GREATER**</dt> </dl>                           | Die Filteraktion ist größer als (>), und die Groß-/Kleinschreibung wird beachtet.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**FILTERACTION \_ LESSNC**</dt> </dl>                              | Die Filteraktion ist kleiner als (<), und die Groß-/Kleinschreibung wird nicht beachtet.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**FILTERACTION \_ LESS**</dt> </dl>                                    | Die Filteraktion ist kleiner als (<), und die Groß-/Kleinschreibung wird beachtet.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**FILTERACTION \_ GREATEREQUALNC**</dt> </dl>      | Die Filteraktion ist größer oder gleich (>=), und die Groß-/Kleinschreibung wird nicht beachtet.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**FILTERACTION \_ GREATEREQUAL**</dt> </dl>            | Die Filteraktion ist größer oder gleich (>=), und die Groß-/Kleinschreibung wird beachtet.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**FILTERACTION \_ LESSEQUALNC**</dt> </dl>               | Die Filteraktion ist kleiner oder gleich (<=), und die Groß-/Kleinschreibung wird nicht beachtet.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**FILTERACTION \_ LESSEQUAL**</dt> </dl>                     | Die Filteraktion ist kleiner oder gleich (<=) und berücksichtigt die Groß-/Kleinschreibung.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**FILTERACTION \_ PLUS**</dt> </dl>                                    | Add-Operator (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**FILTERACTION \_ MINUS**</dt> </dl>                                 | Subtraktionsoperator (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**FILTERACTION \_ AREBITSON**</dt> </dl>                     | Gibt eine bitweise Operation an.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**FILTERACTION \_ AREBITSOFF**</dt> </dl>                  | Gibt einen nicht bitweisen Vorgang an.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**\_FILTERACTION-PROTOKOLLEEXIST**</dt> </dl>      | Gibt an, dass die ausgewählten Protokolle vorhanden sind.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLEXIST**</dt> </dl>         | Gibt an, dass das ausgewählte Protokoll vorhanden ist.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**FILTERACTION \_ ARRAYEQUAL**</dt> </dl>                  | Gibt an, dass der Arrayinhalt gleich ist. Das Flag muss mit einer **FILTERACTION \_ ARRAY-Struktur** verwendet werden.<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**FILTERACTION \_ DEREFPROPERTY**</dt> </dl>         | Beschreibt eine Musterabgleich an einem Offset (in Bytes) aus dem Protokoll.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**FILTERACTION \_ OID \_ CONTAINS**</dt> </dl>           | Wertet eine Teilzeichenfolge innerhalb eines Objektbezeichners aus. Die Aktion muss mit der **\_ FILTERACTION-OID-Struktur** verwendet werden.<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**\_FILTERACTION-OID \_ BEGINNT \_ MIT**</dt> </dl> | Wertet eine Teilzeichenfolge aus, die einen Objektbezeichner beginnt. Das Flag muss mit **filteraction \_ OID** verwendet werden.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**\_FILTERACTION-OID \_ ENDET \_ MIT**</dt> </dl>       | Wertet eine Teilzeichenfolge aus, die einen Objektbezeichner beendet. Das Flag muss mit **filteraction \_ OID** verwendet werden.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**FILTERACTION \_ ADDR \_ VINES**</dt> </dl>                 | Enthält eine MAC-Adresse für Vines.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**FILTERACTION \_ EXPRESSION**</dt> </dl>                  | Enthält einen Aktionsausdruck.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**FILTERACTION \_ BOOL**</dt> </dl>                                    | Enthält einen **BOOL-Datentyp.**<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**FILTERRICHTUNG \_ \_ WEITER**</dt> </dl>                       | Steuert die sequenzielle Richtung (Nächster Frame) innerhalb einer Aufzeichnungsdatei.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**FILTER \_ DIRECTION \_ PREV**</dt> </dl>                       | Steuert die sequenzielle Richtung (Vorheriger Frame) innerhalb einer Aufzeichnungsdatei.<br/>                                                |



 

</dd> <dt>

**hProperty**
</dt> <dd>

Handle für einen Eigenschaftsschlüssel.

</dd> <dt>

**Wert**
</dt> <dd>

Der Wert eines Objekts.

</dd> <dt>

**hProtocol**
</dt> <dd>

Handle zum Anzeigen des Filterprotokolls.

</dd> <dt>

**lpArray**
</dt> <dd>

Zeiger auf ein Array.

</dd> <dt>

**lpProtocolTable**
</dt> <dd>

Zeiger auf eine Protokollliste, die das Vorhandensein des Protokolls in einem Frame testen soll.

</dd> <dt>

**lpAddress**
</dt> <dd>

Zeiger auf die Kerneltypadresse. Beispiel: MAC oder IP.

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Doppeltes **DWORD,** das in einer Windows NT- oder Windows 2000-Anwendung verwendet wird.

</dd> <dt>

**lpTime**
</dt> <dd>

Ein Zeiger auf eine **SYSTEMTIME-Struktur.**

</dd> <dt>

**lpOID**
</dt> <dd>

Ein Zeiger auf die OID-Struktur **(OBJECT \_ IDENTIFIER).**

</dd> <dt>

**ByteCount**
</dt> <dd>

Die Zahl im Frame in Bytes.

</dd> <dt>

**ByteOffset**
</dt> <dd>

Der Offset-Bytewert der FILTEROBJECT-Struktur, der zum Vergleichen von Arrays verwendet wird.

</dd> <dt>

**pNext**
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




