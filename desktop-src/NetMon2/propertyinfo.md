---
description: Die PROPERTYINFO-Datenstruktur definiert eine Eigenschaft des Protokolls.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: PROPERTYINFO-Struktur (Netmon.h)
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
ms.openlocfilehash: 8dc20b94fbf889b4c04712eadbee5d7d834d3cf260962fe01ef7837e5893c4a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128950"
---
# <a name="propertyinfo-structure"></a>PROPERTYINFO-Struktur

Die **PROPERTYINFO-Datenstruktur** definiert eine Eigenschaft des Protokolls.

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

**hProperty**
</dt> <dd>

Legen Sie dieses Feld auf 0 (null) fest. Bei der Ausgabe gibt Netzwerkmonitor ein Handle für die Eigenschaft zurück, nachdem die Eigenschaft der Eigenschaftendatenbank hinzugefügt wurde.

</dd> <dt>

**Version**
</dt> <dd>

Reserviert. Muss auf 0 (null) festgelegt werden.

</dd> <dt>

**Label**
</dt> <dd>

Der Name der Eigenschaft.

</dd> <dt>

**Comment**
</dt> <dd>

Beschreibung der Eigenschaft. Die Beschreibung wird auf der Netzwerkmonitor Statusleiste angezeigt.

</dd> <dt>

**DataType**
</dt> <dd>

Datentyp der Eigenschaft. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**PROP \_ TYPE \_ VOID**</dt> </dl>                                           | Der Eigenschaftentyp ist unbekannt. Es gibt keine implizite Länge oder kein Format.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**\_ZUSAMMENFASSUNG DES PROP-TYPS \_**</dt> </dl>                                  | Zusammenfassung des Eigenschaftentyps. Gibt die erste Eigenschaftsinstanz an, die der Parser an einen Frame anfügt. PROP \_ TYPE \_ SUMMARY kann als Platzhalter für Gruppen von Eigenschaften dienen. Dieser Wert gibt an, dass die -Eigenschaft im *Protokoll RFC* nicht definiert ist.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**PROP \_ TYPE \_ BYTE**</dt> </dl>                                           | Numerische Daten mit einer Größe von einem Byte (8-Bit-Entität).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**PROP \_ TYPE \_ WORD**</dt> </dl>                                           | Numerische Daten mit einer Größe von zwei Bytes (16-Bit-Entität).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**PROP \_ TYPE \_ DWORD**</dt> </dl>                                        | Numerische Daten mit einer Größe von vier Bytes (32-Bit-Entität).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**PROP \_ TYPE \_ LARGEINT**</dt> </dl>                               | Numerische Daten mit einer Größe von acht Bytes (64-Bit-Entität).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**PROP \_ TYPE \_ ADDR**</dt> </dl>                                           | MAC-Adresse (6-Byte-Entität).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**PROP \_ TYPE \_ TIME**</dt> </dl>                                           | **SYSTEMTIME-Struktur.**<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**PROP \_ TYPE \_ STRING**</dt> </dl>                                     | ASCII-Textdaten. Dieser Datentyp ist nicht NULL-terminiert. <br/> Wenn ASCII-Textdaten für Unicode-Daten angegeben werden, muss auch das IFLAG \_ UNICODE-Flag festgelegt werden, wenn die Attach-Eigenschaftsinstanzfunktion aufgerufen wird.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**\_PROP TYPE IP ADDRESS \_ (IP-ADRESSE DES PROP-TYPS) \_**</dt> </dl>                        | IP-Adresse. (4-Byte-Entität).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**PROP \_ TYPE \_ IPX \_ ADDRESS**</dt> </dl>                     | IPX-Adresse. (10-Byte-Entität).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**PROP \_ TYPE \_ BYTESWAPPED \_ WORD**</dt> </dl>      | Veraltet. Legen Sie für WORD-Daten mit Byteaustausch **DataType** auf PROP \_ TYPE WORD \_ fest, und legen Sie das IFLAG \_ SWAPPED-Flag fest, wenn Sie eine **Attach-Eigenschaftsinstanzfunktion** aufrufen.<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**PROP \_ TYPE \_ BYTESWAPPED \_ DWORD**</dt> </dl>   | Veraltet. Legen Sie für durch Byte getauschte DWORD-Daten **DataType** auf PROP \_ TYPE \_ DWORD und das IFLAG \_ SWAPPED-Flag fest, wenn Sie eine **Attach-Eigenschaftsinstanzfunktion** aufrufen.<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**TYPISIERTE ZEICHENFOLGE VOM TYP PROP \_ \_ \_**</dt> </dl>                  | Veraltet. Legen Sie für Zeichenfolgendaten variabler Typen **DataType** auf PROP \_ TYPE STRING \_ fest, und legen Sie das IFLAG \_ UNICODE-Flag fest, wenn Sie eine Attach-Eigenschaftsinstanzfunktion aufrufen. <br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**PROP \_ TYPE \_ RAW \_ DATA**</dt> </dl>                              | Rohdaten mit unbekannter Länge und unbekanntem Format.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**PROP \_ TYPE \_ COMMENT**</dt> </dl>                                  | Identisch mit PROP \_ TYPE \_ VOID.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**PROP \_ TYPE \_ SRCFRIENDLYNAME**</dt> </dl>          | Adresse des quellfreundlichen Namens. Netzwerkmonitor bietet keine integrierte Formatierungsunterstützung für diesen Datentyp.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**\_PROP-TYP \_ DSTFRIENDLYNAME**</dt> </dl>          | Adresse des Anzeigenamens des Ziels. Netzwerkmonitor bietet keine integrierte Formatierungsunterstützung für diesen Datentyp.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**PROP \_ TYPE \_ TOKENRING \_ ADDRESS**</dt> </dl>   | Tokenringadresse. Netzwerkmonitor bietet keine integrierte Formatierungsunterstützung für diesen Datentyp.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**PROP \_ TYPE \_ FDDI \_ ADDRESS**</dt> </dl>                  | FDDI-Adresse. Netzwerkmonitor bietet keine integrierte Formatierungsunterstützung für diesen Datentyp.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**PROP \_ TYPE \_ ETHERNET \_ ADDRESS**</dt> </dl>      | Ethernet-Adresse. Netzwerkmonitor bietet keine integrierte Formatierungsunterstützung für diesen Datentyp.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**\_OBJEKTBEZEICHNER DES PROP-TYPS \_ \_**</dt> </dl>   | BER-codierter SNMP-Objektbezeichner.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**PROP \_ TYPE \_ VINES \_ IP \_ ADDRESS**</dt> </dl>     | Vines-IP-Adresse (6-Byte-Entität).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**PROP \_ TYPE \_ VAR \_ LEN \_ SMALL \_ INT**</dt> </dl> | Numerischer Wert ohne vordefinierte Länge, aber nicht mehr als 8 Byte lang. Die Länge der angefügten Daten bestimmt die Länge des Werts.<br/>                                                                                                                                                |



 

</dd> <dt>

**DataQualifier**
</dt> <dd>

Der Datenqualifizierer einer Eigenschaft. Dieser Member stellt genaue Informationen zum Datentyp bereit.

**DataQualifier** kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ QUAL \_ NONE**</dt> </dl>                                      | Der Eigenschaftsdatentyp ist die einzige Spezifikation der Eigenschaft. <br/> Wenn dieser Wert festgelegt ist, wird der Union-Member der -Struktur auf **NULL** festgelegt und dann ignoriert.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**PROP \_ QUAL \_ RANGE**</dt> </dl>                                   | Es wird erwartet, dass sich der numerische Wert innerhalb eines bestimmten Bereichs befindet. Definieren Sie den Bereich im **lpRange-Member.**<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**PROP \_ QUAL \_ SET**</dt> </dl>                                         | Der Wert einer Eigenschaft wird mit einem Satz von Werten verglichen, die im **lpSet-Member** der Union der Struktur angegeben sind. Der Wert einer Eigenschaft kann **byte,** **WORD,** **DWORD,** **LARGEINT** oder **TIME** sein.<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**PROP \_ QUAL \_ BITFIELD**</dt> </dl>                          | Veraltet.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**PROP \_ QUAL \_ LABELED \_ SET**</dt> </dl>                | Der Wert einer Eigenschaft wird mit einem Wert in einem Satz von Wertbezeichnungspaaren verglichen. Die Wertbezeichnungspaare werden im **lpSet-Member** der Union der Struktur angegeben. <br/> Wenn der Wert der Eigenschaft zur Anzeigezeit mit einem Wert in der Menge übereinstimmt, werden sowohl ein Wert als auch die zugeordnete Bezeichnung angezeigt.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD**</dt> </dl> | Veraltet. Verwenden Sie stattdessen PROP \_ QUAL \_ FLAGS.<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**PROP \_ QUAL \_ CONST**</dt> </dl>                                   | Der Wert einer Eigenschaft wird mit einer Konstante verglichen, die im **Value-Member** der Union angegeben ist. <br/> Wenn die Eigenschaftswerte und die Konstante zur Anzeigezeit nicht übereinstimmen, wird eine formatierte Fehlermeldung angezeigt, deren Wert auf Normal festgelegt ist.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**\_ \_ PROP-QUAL-FLAGS**</dt> </dl>                                   | Der Wert der -Eigenschaft wird mit bestimmten BITs verglichen, die im **lpSet-Member** der Union identifiziert werden.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**PROP \_ QUAL \_ ARRAY**</dt> </dl>                                   | Der Wert einer Eigenschaft gibt ein Array von Werten an. Die Länge der angefügten Daten bestimmt die Länge eines Arrays. <br/> Wenn der PROP \_ QUAL \_ ARRAY-Wert festgelegt wird, wird der Union-Member der **PROPERTYINFO-Datenstruktur** auf **NULL** festgelegt und ignoriert.<br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Reserviert (Mitglied der Union).

</dd> <dt>

**lpRange**
</dt> <dd>

Zeiger auf eine [RANGE-Struktur,](range.md) die einen Wertebereich definiert. Dieser Member muss festgelegt werden, wenn der **DataQualifier-Member** dieser Struktur auf PROP \_ QUAL \_ RANGE (Member der Union) festgelegt ist.

</dd> <dt>

**lpSet**
</dt> <dd>

Zeiger auf eine [SET-Struktur,](set.md) die einen Satz von Werten oder Bezeichnungen angibt. Dieser Member muss festgelegt werden, wenn der **DataQualifier-Member** der Struktur auf PROP \_ QUAL \_ SET, PROP \_ QUAL \_ LABELED \_ SET oder PROP \_ QUAL \_ FLAGS (Member der Union) festgelegt ist.

</dd> <dt>

**Bitmaske**
</dt> <dd>

Veraltet (Mitglied der Union).

</dd> <dt>

**Wert**
</dt> <dd>

Konstanter Wert, der verwendet wird, wenn **DataQualifier** auf PROP \_ QUAL \_ CONST (Member der Union) festgelegt ist.

</dd> <dt>

**FormatStringSize**
</dt> <dd>

Maximale Größe, die nur für die Eigenschaftenbeschreibung verwendet wird.

</dd> <dt>

**Instancedata**
</dt> <dd>

Geben Sie die Formatfunktion an, die aufgerufen wird, um die angezeigten Daten für die Eigenschaft zu formatieren. Um das generische Formatierer zu verwenden, geben Sie die **FormatPropertyInstance-Funktion** an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **PROPERTYINFO-Struktur** wird in Aufrufen der [AddProperty-Funktion](/previous-versions/bb251873(v=msdn.10)) verwendet. Die **AddProperty-Funktion** fügt der [*Parsereigenschaftendatenbank*](p.md)eine einzelne Eigenschaftendefinition hinzu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Addproperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[Bereich](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

