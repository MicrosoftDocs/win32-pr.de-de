---
description: Definiert ein einzelnes Objekt eines Anzeige Filters.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Filterobject-Struktur (Netmon. h)
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
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345481"
---
# <a name="filterobject-structure"></a>Filterobject-Struktur

Die **filterobject** -Struktur definiert ein einzelnes Objekt eines Anzeige Filters. Die [**FilterAddObject**](filteraddobject.md) -Funktion verwendet **filterobject** , um einen Anzeige Filter zu erstellen.

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

Flag, das die **filterobject** -Aktion angibt. Ein Flag kann eine Eigenschaft, einen Wert oder einen Operator angeben.

In der folgenden Tabelle sind die Eigenschaftenflags für Aktions Member aufgelistet



| Wert                                                                                                                                                                                                | Bedeutung                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**filteraction ( \_ Eigenschaft)**</dt> </dl>                | Enthält diese Eigenschaft.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**filteraction \_ PropertyExist**</dt> </dl> | Gibt an, dass eine Filter Aktions Eigenschaft bereits definiert ist.<br/> |



 

In der folgenden Tabelle sind die wertflags für Aktions Mitglieder aufgelistet.



| Wert                                                                                                                                                                                        | Bedeutung                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**filteraction- \_ Wert**</dt> </dl>                 | Enthält diesen Wert.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**filteraction- \_ Zeichenfolge**</dt> </dl>              | Enthält diese Zeichenfolge.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**filteraction- \_ Array**</dt> </dl>                 | Enthält dieses Array.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**filteraction ( \_ kontainsnc)**</dt> </dl>  | Gibt an, dass eine Eigenschaft eine Teil Zeichenfolge ohne Beachtung der Groß-und klein<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**filteraction \_ enthält**</dt> </dl>        | Gibt an, dass eine Eigenschaft eine Teil Zeichenfolge mit Beachtung der groß-<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**filteraction- \_ Adresse**</dt> </dl>           | Enthält die Mac-Adresse.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**"filteraction \_ addressany"**</dt> </dl>  | Entspricht einer beliebigen Mac-Adresse.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**filteraction \_ aus**</dt> </dl>                    | Gibt die **von Mac** -Adresse an.<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**filteraction \_ in**</dt> </dl>                          | Gibt die **an Mac** -Adresse an.<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**filteraction \_ FromTo**</dt> </dl>              | Gibt eine **from/to-** Kopplung von Mac-Adressen an.<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**filteraction \_ largeint**</dt> </dl>        | Enthält eine große Ganzzahl.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**filteraction- \_ Zeit**</dt> </dl>                    | Enthält eine **SYSTEMTIME** -Struktur.<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**filteraction- \_ addr- \_ Äther**</dt> </dl> | Enthält eine Ethernet-MAC-Adresse.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**filteraction- \_ addr- \_ Token**</dt> </dl> | Enthält eine TokenRing-Mac-Adresse.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**filteraction \_ addr- \_ fiddi**</dt> </dl>    | Enthält eine GDDI-Mac-Adresse.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**filteraction \_ addr \_ IPX**</dt> </dl>       | Enthält eine IPX-Mac-Adresse.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**filteraction \_ addr \_ -IP**</dt> </dl>          | Enthält eine IP-MAC-Adresse.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**filteraction- \_ OID**</dt> </dl>                       | Enthält einen Objekt Bezeichner (OID).<br/>                             |



 

In der folgenden Tabelle sind Aktionsmember-Operator Flags aufgeführt.



| Wert                                                                                                                                                                                                        | Bedeutung                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**filteraction ist \_ ungültig.**</dt> </dl>                           | Gibt eine ungültige Filter Aktion an.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**filteraction \_ und**</dt> </dl>                                       | Gibt eine logische **and-** Anweisung an.<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**filteraction \_ oder**</dt> </dl>                                          | Gibt eine logische **or** -Anweisung an.<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**filteraction- \_ Xor**</dt> </dl>                                       | Gibt eine logische exklusive **or** -Anweisung (XOR) an.<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**filteraction \_ nicht**</dt> </dl>                                       | Gibt eine logische **Not** -Anweisung an.<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**filteraction \_ equalnc**</dt> </dl>                           | Filter Aktion ist gleich und Groß-/Kleinschreibung nicht beachtet<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**filteraction \_ gleich**</dt> </dl>                                 | Filter Aktion ist gleich und Groß-/Kleinschreibung beachtet.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**filteraction \_ notequalnc**</dt> </dl>                  | Die logische NOT-Anweisung ist gleich und unterscheidet **nicht** .<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**filteraction- \_ NotEqual**</dt> </dl>                        | Die logische **Not** -Anweisung ist gleich und berücksichtigt die Groß-/Kleinschreibung<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**filteraction \_ greaternc**</dt> </dl>                     | Die Filter Aktion ist größer als (>) und Groß-/Kleinschreibung nicht beachtet.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**filteraction \_ größer**</dt> </dl>                           | Die Filter Aktion ist größer als (>) und Groß-/Kleinschreibung beachten.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**filteraction \_ lessnc**</dt> </dl>                              | Die Filter Aktion ist kleiner als (<) und Groß-/Kleinschreibung nicht beachtet.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**weniger filteraction \_**</dt> </dl>                                    | Filter Aktion ist kleiner als (<) und Unterscheidung nach Groß-/Kleinschreibung.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**filteraction \_ greaterequalnc**</dt> </dl>      | Die Filter Aktion ist größer als oder gleich (>=) und Groß-/Kleinschreibung nicht beachtet.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**filteraction \_ greaterequal**</dt> </dl>            | Die Filter Aktion ist größer als oder gleich (>=) und Unterscheidung nach Groß-/Kleinschreibung.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**filteraction \_ lessequalnc**</dt> </dl>               | Die Filter Aktion ist kleiner oder gleich (<=) und Groß-/Kleinschreibung nicht beachtet.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**filteraction- \_ lessequenz**</dt> </dl>                     | Die Filter Aktion ist kleiner als oder gleich (<=) und beachtet die Groß-/Kleinschreibung.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**filteraction \_ Plus**</dt> </dl>                                    | Operator hinzufügen (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**filteraction \_ minus**</dt> </dl>                                 | Subtract-Operator (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**filteraction \_ arebitson**</dt> </dl>                     | Gibt eine bitweise-Operation an.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**filteraction \_ arebitsoff**</dt> </dl>                  | Gibt eine nicht bitweise-Operation an.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**filteraction \_ protocolsexistisch**</dt> </dl>      | Gibt an, dass die ausgewählten Protokolle vorhanden sind.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**filteraction \_ protocolexist**</dt> </dl>         | Gibt an, dass das ausgewählte Protokoll vorhanden ist.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**filteraction \_ arrayequal**</dt> </dl>                  | Gibt an, dass der Array Inhalt gleich ist. Das Flag muss mit einer **filteraction- \_ Array** Struktur verwendet werden.<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**filteraction- \_ derefproperty**</dt> </dl>         | Beschreibt eine Muster Übereinstimmung mit einem Offset (in Bytes) aus dem Protokoll.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**filteraction- \_ OID \_ enthält**</dt> </dl>           | Wertet eine Teil Zeichenfolge in einem Objekt Bezeichner aus. Die Aktion muss mit der " **filteraction \_ OID** "-Struktur verwendet werden.<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**filteraction \_ OID \_ beginnt \_ mit**</dt> </dl> | Wertet eine Teil Zeichenfolge aus, die einen Objekt Bezeichner startet. Das Flag muss mit der **filteraction- \_ OID** verwendet werden.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**filteraction- \_ OID \_ endet \_ mit**</dt> </dl>       | Wertet eine Teil Zeichenfolge aus, die einen Objekt Bezeichner beendet. Das Flag muss mit der **filteraction- \_ OID** verwendet werden.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**filteraction \_ addr- \_ Reben**</dt> </dl>                 | Enthält die Mac-Adresse der Reben.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**filteraction- \_ Ausdruck**</dt> </dl>                  | Enthält einen Aktions Ausdruck.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**filteraction \_ bool**</dt> </dl>                                    | Enthält einen **booleschen** Datentyp.<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**\_Richtung \_ weiter filtern**</dt> </dl>                       | Steuert die sequenzielle Richtung (Nächster Frame) innerhalb einer Erfassungs Datei.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**Filter \_ Richtung ( \_ Prev)**</dt> </dl>                       | Steuert die sequenzielle Richtung (Vorheriger Frame) innerhalb einer Erfassungs Datei.<br/>                                                |



 

</dd> <dt>

**hproperty**
</dt> <dd>

Handle für einen Eigenschafts Schlüssel.

</dd> <dt>

**Wert**
</dt> <dd>

Der Wert eines Objekts.

</dd> <dt>

**hprotocol**
</dt> <dd>

Handle zum Anzeigen des Filter Protokolls.

</dd> <dt>

**lpArray**
</dt> <dd>

Zeiger auf ein Array.

</dd> <dt>

**lpprotocoltable**
</dt> <dd>

Ein Zeiger auf eine Protokoll Liste, mit der das vorhanden sein des Protokolls in einem Frame getestet werden soll.

</dd> <dt>

**lpAddress**
</dt> <dd>

Zeiger auf die kerneltyp Adresse. Beispielsweise Mac oder IP.

</dd> <dt>

**lplargeint**
</dt> <dd>

Doppeltes **DWORD** , das in einer Windows NT-oder Windows 2000-Anwendung verwendet wird.

</dd> <dt>

**lptime**
</dt> <dd>

Ein Zeiger auf eine **SYSTEMTIME** -Struktur.

</dd> <dt>

**lpoid**
</dt> <dd>

Ein Zeiger auf die **Objekt \_ Bezeichner** -Struktur (OID).

</dd> <dt>

**ByteCount**
</dt> <dd>

Die Zahl in Bytes im Frame.

</dd> <dt>

**Byte Offset**
</dt> <dd>

Der Offset Byte Wert der filterobject-Struktur, die zum Vergleichen von Arrays verwendet wird.

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
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




