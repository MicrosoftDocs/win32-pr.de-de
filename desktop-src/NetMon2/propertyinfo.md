---
description: Die PropertyInfo-Datenstruktur definiert eine Eigenschaft des Protokolls.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: PropertyInfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959488"
---
# <a name="propertyinfo-structure"></a>PropertyInfo-Struktur

Die **PropertyInfo** -Datenstruktur definiert eine Eigenschaft des Protokolls.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**hproperty**
</dt> <dd>

Legen Sie dieses Feld auf NULL fest. Bei der Ausgabe gibt Netzwerkmonitor ein Handle für die-Eigenschaft zurück, nachdem die-Eigenschaft der Eigenschaften Datenbank hinzugefügt wurde.

</dd> <dt>

**Version**
</dt> <dd>

Reserviert. Muss auf 0 (null) festgelegt werden.

</dd> <dt>

**Label**
</dt> <dd>

Der Name der Eigenschaft.

</dd> <dt>

**Kommentar**
</dt> <dd>

Die Beschreibung der Eigenschaft. Die Beschreibung wird auf der Netzwerkmonitor Statusleiste angezeigt.

</dd> <dt>

**DataType**
</dt> <dd>

Datentyp der Eigenschaft. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**Prop- \_ Typ \_ void**</dt> </dl>                                           | Der Eigenschaftentyp ist unbekannt. Es gibt keine implizite Länge oder kein implizites Format.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**Prop \_ - \_ typzusammenfassung**</dt> </dl>                                  | Eigenschaften Typen werden zusammengefasst. Gibt die erste Eigenschaften Instanz an, die der Parser an einen Frame anfügt. Die \_ \_ Zusammenfassung des prop-Typs kann als Platzhalter für Gruppen von Eigenschaften dienen. Dieser Wert gibt an, dass die Eigenschaft nicht im Protokoll *RFC* definiert ist.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**Prop \_ - \_ typbyte**</dt> </dl>                                           | Numerische Daten mit einer Größe von einem Byte (8-Bit-Entität).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**Prop \_ - \_ typwort**</dt> </dl>                                           | Numerische Daten mit einer Größe von zwei Bytes (16-Bit-Entität).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**Prop- \_ Typ \_ DWORD**</dt> </dl>                                        | Numerische Daten mit einer Größe von vier Bytes (32-Bit-Entität).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**Prop- \_ Typ \_ largeint**</dt> </dl>                               | Numerische Daten mit einer Größe von 8 Bytes (64-Bit-Entität).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**Prop \_ Type \_ addr**</dt> </dl>                                           | Mac-Adresse (6-Byte-Entität).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**Prop \_ - \_ typzeit**</dt> </dl>                                           | **SYSTEMTIME** -Struktur.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**Prop \_ - \_ Zeichenfolge**</dt> </dl>                                     | ASCII-Textdaten. Dieser Datentyp wird nicht mit Null beendet. <br/> Bei Unicode-Daten muss beim Aufrufen von ASCII-Textdaten auch das iflag- \_ Unicode-Flag festgelegt werden, wenn die Anfüge Eigenschaft-Instanzfunktion aufgerufen wird.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**\_ \_ IP-Adresse des prop-Typs \_**</dt> </dl>                        | IP-Adresse. (4-Byte-Entität).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**\_ \_ IPX- \_ Adresse des prop-Typs**</dt> </dl>                     | IPX-Adresse (10-Byte-Entität).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**"prop \_ Type \_ byteswlapp \_ Word"**</dt> </dl>      | Veraltet. Legen Sie für Byte gesteuerte Word-Daten den **DataType** auf Prop \_ Type \_ Word fest, und legen Sie \_ beim Aufrufen einer **Anfüge** Eigenschaft-Instanzfunktion das eingetauschte iflag-Flag fest.<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**der prop- \_ Typ \_ byteswlapp \_ DWORD**</dt> </dl>   | Veraltet. Legen Sie für in Byte ausgelegte DWORD-Daten einen **DataType** -Wert auf Prop \_ Type \_ DWORD fest, und legen Sie \_ beim Aufrufen einer **Anfüge** Eigenschaft-Instanzfunktion das eingetauschte iflag fest.<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**\_Typzeichenfolge für den Prop \_ \_**</dt> </dl>                  | Veraltet. Legen Sie für Zeichen folgen Daten variabler Art **DataType** auf Prop \_ Type \_ String fest, und legen Sie das iflag Unicode-Flag fest, \_ Wenn Sie eine **Anfüge** Eigenschaften-Instanzfunktion aufrufen.<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**Rohdaten des prop- \_ Typs \_ \_**</dt> </dl>                              | Rohdaten unbekannter Länge und Format.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**Prop \_ - \_ typkommentar**</dt> </dl>                                  | Identisch mit dem Prop- \_ Typ " \_ void".<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**Prop- \_ Typ \_ srcfriendlyname**</dt> </dl>          | Adresse des Quell freundlichen namens. Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**Prop- \_ Typ \_ dstfriendlyname**</dt> </dl>          | Adresse des Ziel anzeigen Amens. Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**\_ \_ tokenringadresse des prop-Typs \_**</dt> </dl>   | Tokenringadresse. Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**Prop \_ Type-Adresse des Typs " \_ f" \_**</dt> </dl>                  | Die Adresse von "f". Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**IP-Adresse des prop- \_ Typs \_ \_**</dt> </dl>      | Ethernet-Adresse. Netzwerkmonitor bietet keine integrierte Formatierungs Unterstützung für diesen Datentyp.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**\_ \_ Objekt \_ Bezeichner des prop-Typs**</dt> </dl>   | BER-codierter SNMP-Objekt Bezeichner.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**\_ \_ \_ IP-Adresse der prop-typreben \_**</dt> </dl>     | IP-Adresse der Reben (6-Byte-Entität).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**Prop \_ Type \_ var \_ len \_ Small \_ int**</dt> </dl> | Numerischer Wert ohne vordefinierte Länge, aber nicht mehr als 8 Bytes. Die Länge der angefügten Daten bestimmt die Länge des Werts.<br/>                                                                                                                                                |



 

</dd> <dt>

**Dataqualifizierer**
</dt> <dd>

Der Daten Qualifizierer einer Eigenschaft. Dieser Member stellt genaue Informationen zum Datentyp bereit.

**Dataqualifizierer** kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**Prop \_ Qual \_ None**</dt> </dl>                                      | Der-Eigenschafts Datentyp ist die einzige Spezifikation der-Eigenschaft. <br/> Wenn dieser Wert festgelegt wird, wird der Union-Member der-Struktur auf **null** festgelegt und dann ignoriert.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**Bereich für die Stütz \_ Qual \_**</dt> </dl>                                   | Es wird erwartet, dass der numerische Wert innerhalb eines angegebenen Bereichs liegt. Definieren Sie den Bereich im **lprange** -Member.<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**Prop- \_ Qual- \_ Satz**</dt> </dl>                                         | Der Wert einer Eigenschaft wird mit einem Satz von Werten verglichen, die im **lpset** -Member der Union-Struktur angegeben werden. Der Wert einer Eigenschaft kann ein **Byte**-, **Word**-, **DWORD**-, **largeint** -oder **time**-Wert sein.<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**Prop \_ - \_ Bitfeld**</dt> </dl>                          | Veraltet.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**Bezeichnung für "prop \_ Qual" \_ \_**</dt> </dl>                | Der Wert einer Eigenschaft wird mit einem Wert in einem Satz von Wert Bezeichnungs Paaren verglichen. Die Wert Bezeichnungs Paare werden im **lpset** -Member der Union-Struktur angegeben. <br/> Wenn der Wert der Eigenschaft zur Anzeigezeit mit einem Wert in der Menge übereinstimmt, werden sowohl ein Wert als auch die zugehörige Bezeichnung angezeigt.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld**</dt> </dl> | Veraltet. Verwenden Sie \_ stattdessen Prop-Qual- \_ Flags.<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**Prop \_ Qual \_ konstant**</dt> </dl>                                   | Der Wert einer Eigenschaft wird mit einer Konstante verglichen, die im **Wertmember** der Union angegeben wird. <br/> Wenn die Eigenschaftswerte und die Konstante nicht mit der Anzeigezeit identisch sind, wird eine formatierte Fehlermeldung angezeigt, und der Wert wird auf Normal festgelegt.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**Prop- \_ Qual- \_ Flags**</dt> </dl>                                   | Der Wert der-Eigenschaft wird mit bestimmten Bits verglichen, die im **lpset** -Member der Union identifiziert werden.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**Prop- \_ Qual- \_ Array**</dt> </dl>                                   | Der Wert einer Eigenschaft gibt ein Array von Werten an. Die Länge der angefügten Daten bestimmt die Länge eines Arrays. <br/> Wenn der Wert des prop \_ Qual \_ -Arrays festgelegt wird, wird das Unionmember der **PropertyInfo** -Datenstruktur auf **null** festgelegt und ignoriert.<br/>                                                    |



 

</dd> <dt>

**lpextendedinfo**
</dt> <dd>

Reserviert (Union-Mitglied).

</dd> <dt>

**lprange**
</dt> <dd>

Ein Zeiger auf eine [Bereichs](range.md) Struktur, die einen Wertebereich definiert. Dieser Member muss festgelegt werden, wenn der **dataqualifier** -Member dieser Struktur auf den Prop-Wert \_ \_ Bereich (Member of Union) festgelegt ist.

</dd> <dt>

**lpset**
</dt> <dd>

Ein Zeiger auf eine [Set](set.md) -Struktur, die einen Satz von Werten oder Bezeichnungen angibt. Dieser Member muss festgelegt werden, wenn der **dataqualifier** -Member der Struktur auf Prop \_ Qual \_ Set, Prop \_ Qual \_ bezeichnete \_ Menge oder Prop \_ Qual \_ Flags (Member of Union) festgelegt ist.

</dd> <dt>

**Bitmaske**
</dt> <dd>

Veraltet (Member der Union).

</dd> <dt>

**Wert**
</dt> <dd>

Konstanter Wert, der verwendet wird, wenn **dataqualifizierer** auf Prop \_ Qual \_ konstant (Member of Union) festgelegt ist.

</dd> <dt>

**Formatstringsize**
</dt> <dd>

Maximale Größe, die nur für die Eigenschafts Beschreibung verwendet wird.

</dd> <dt>

**InstanceData**
</dt> <dd>

Geben Sie die Format Funktion an, die zum Formatieren der angezeigten Daten für die Eigenschaft aufgerufen wird. Wenn Sie den generischen Formatierer verwenden möchten, geben Sie die **formatpropertyinstance** -Funktion an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **PropertyInfo** -Struktur wird in Aufrufen der [AddProperty](/previous-versions/bb251873(v=msdn.10)) -Funktion verwendet. Die **AddProperty** -Funktion fügt der Parser- [*Eigenschaften Datenbank*](p.md)eine einzelne Eigenschafts Definition hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[Bereich](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

