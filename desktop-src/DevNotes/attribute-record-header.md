---
description: Stellt einen Attributdatensatz dar.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9664af36448bb125dc8d5fde3c4d22b04e58b1ca341acad561b94708acbf143c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045389"
---
# <a name="attribute_record_header-structure"></a>ATTRIBUTE \_ RECORD \_ HEADER-Struktur

\[Diese Struktur ist nur für Version 3 von NTFS-Volumes gültig. sie kann in zukünftigen Versionen geändert werden.\]

Stellt einen Attributdatensatz dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**TypeCode**
</dt> <dd>

Der Attributtypcode.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$STANDARD \_ INFORMATIONEN**</dt> <dt>0x10</dt> </dl> | Dateiattribute (z. B. schreibgeschützt und archivieren), Zeitstempel (z. B. Dateierstellung und letzte Änderung) und die Anzahl der hardlinks.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$ATTRIBUTE \_ LIST**</dt> <dt>0x20</dt> </dl>                   | Eine Liste der Attribute, aus denen die Datei besteht, und der Dateiverweis des MFT-Dateidatensatz, in dem sich jedes Attribut befindet.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$FILE \_ NAME**</dt> <dt>0x30</dt> </dl>                                  | Der Name der Datei in Unicode-Zeichen.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$OBJECT \_ ID-0x40**</dt> <dt></dt> </dl>                                  | Ein vom Linkverfolgungsdienst zugewiesener 64-Byte-Objektbezeichner.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$VOLUME \_ NAME**</dt> <dt>0x60</dt> </dl>                            | Die Volumebezeichnung. In der $Volume vorhanden.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$VOLUME \_ INFORMATION**</dt> <dt>0X70</dt> </dl>       | Die Volumeinformationen. In der $Volume vorhanden.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$DATA**</dt> <dt>0x80</dt> </dl>                                                  | Der Inhalt der Datei.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$INDEX \_ ROOT-0x90**</dt> <dt></dt> </dl>                               | Wird zum Implementieren der Dateinamenzuordnung für große Verzeichnisse verwendet.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$INDEX \_**</dt> <dt>ZUORDNUNGs 0xA0</dt> </dl>             | Wird zum Implementieren der Dateinamenzuordnung für große Verzeichnisse verwendet.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$BITMAP**</dt> <dt>0xB0</dt> </dl>                                            | Ein Bitmapindex für ein großes Verzeichnis.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ POINT**</dt> <dt>0xC0</dt> </dl>                      | Die Reparsepunktdaten.<br/>                                                                                                          |



 

</dd> <dt>

**Recordlength**
</dt> <dd>

Die Größe des Attributdatensatz in Bytes. Dieser Wert gibt die erforderliche Größe für die Datensatzvariante an und wird immer auf die nächste Quadwordgrenze gerundet.

</dd> <dt>

**FormCode**
</dt> <dd>

Der Attributformularcode.



| Wert                                                                                                                                                                                                                            | Bedeutung                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**RESIDENT \_ FORMULAR**</dt> <dt>0X00</dt> </dl>          | Der Wert ist im Dateidatensatz enthalten und folgt unmittelbar auf den Attributdatensatzheader.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <dt>**NONRESIDENT \_ FORMULAR**</dt> <dt>0X01</dt> </dl> | Der Wert ist in anderen Sektoren auf dem Datenträger enthalten.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

Die Größe des optionalen Attributnamens in Zeichen oder 0, wenn kein Attributname vor liegt. Die maximale Länge des Attributnamens beträgt 255 Zeichen.

</dd> <dt>

**NameOffset**
</dt> <dd>

Der Offset des Attributnamens vom Anfang des Attributdatensatzes in Bytes. Wenn das **NameLength-Member** 0 ist, ist dieser Member nicht definiert.

</dd> <dt>

**Flags**
</dt> <dd>

Die Attributflags.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE \_ FLAG \_ COMPRESSION \_ MASK** (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE \_ FLAG \_ SPARSE** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE \_ FLAG \_ ENCRYPTED** (0x4000)
</dt> </dl> </dd> <dt>

**Instanz**
</dt> <dd>

Die eindeutige Instanz für dieses Attribut im Dateidatensatz.

</dd> <dt>

**Form**
</dt> <dd>

Wenn der **FormCode-Member** RESIDENT \_ FORM ist, ist die Union eine **Resident-Struktur.** Wenn **FormCode** NONRESIDENT \_ FORM ist, ist die Union eine **nonresident-Struktur.**

<dl> <dt>

**Wohnsitz**
</dt> <dd> <dl> <dt>

**ValueLength**
</dt> <dd>

Die Größe des Attributwerts in Bytes.

</dd> <dt>

**ValueOffset**
</dt> <dd>

Der Offset zum Wert vom Anfang des Attributdatensatz in Bytes.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl> </dd> <dt>

**Nonresident**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

Die niedrigste virtuelle Clusternummer (VCN), die von diesem Attributdatensatz abgedeckt wird.

</dd> <dt>

**HighestVcn**
</dt> <dd>

Der höchste VCN, der von diesem Attributdatensatz abgedeckt wird.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

Der Offset zum Zuordnungspaararray vom Anfang des Attributdatensatz in Bytes. Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

Die zugeordnete Größe der Datei in Bytes. Dieser Wert ist ein sogar vielfaches der Clustergröße. Dieser Member ist ungültig, wenn **das LowestVcn-Member** ungleich 0 (null) ist.

</dd> <dt>

**FileSize**
</dt> <dd>

Die Dateigröße (höchstes Byte, das gelesen werden kann, plus 1) in Bytes. Dieser Member ist ungültig, wenn **LowestVcn** ungleich 0 (null) ist.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

Die gültige Datenlänge (höchstes initialisiertes Byte plus 1) in Bytes. Dieser Wert wird auf die nächste Clustergrenze gerundet. Dieser Member ist ungültig, wenn **LowestVcn** ungleich 0 (null) ist.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

Die Gesamtsumme, die für die Datei zugeordnet ist (die Summe der zugeordneten Cluster).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass keine zugeordnete Headerdatei für diese -Struktur enthalten ist.

Diese Strukturdefinition ist nur für Hauptversion 3 und Nebenversion 0 oder 1 gültig, wie von [**FSCTL \_ GET NTFS VOLUME DATA \_ \_ \_ gemeldet.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)

Attributdatensätze werden immer an einer Quadwordgrenze ausgerichtet.

Wenn das Attribut nichtresident ist, enthält der Attributdatensatzheader eine Liste von Abrufinformationen, die eine Zuordnung zwischen VCN und logischer Clusternummer (LOGICAL Cluster Number, LCN) für das Attribut ermöglicht. Wenn die Abrufinformationen nicht in das Basisdateisegment passen, können sie selbst in einem externen Dateidatensatzsegment gespeichert werden. Wenn er immer noch nicht in ein externes Dateidatensatzsegment passt, gibt es eine Bereitstellung in der Attributliste, die mehrere Einträge für ein Attribut enthält, das zusätzliche Abrufinformationen erfordert.

Das Zuordnungspaararray wird in komprimierter Form gespeichert und setzt voraus, dass die Informationen dekomprimiert und vom System zwischengespeichert werden. Sie besteht aus einer Reihe von NextVcn-/CurrentLcn-Paaren. Wenn eine Datei z. B. eine einzelne Ausführung von 8 Clustern ab LCN 128 aufweise und die Datei bei LowestVcn 0 beginnt, hat das Array der Zuordnungspaare nur einen Eintrag, also NextVcn=8 und CurrentLcn=128. Das Array ist ein Bytestream, der die Änderungen an den Arbeitsvariablen speichert, wenn es sequenziell verarbeitet wird. Der Bytestream ist wie folgt als nullendpunktr terminierten Datenstrom mit Dreiern zu interpretieren:

count byte = *v* + (*l* \* 16)

Wobei *v* die Anzahl der geänderten VCN-Bytes in niedriger Reihenfolge und *l* die Anzahl der geänderten low-order LCN-Bytes ist.

Der Dekomprimierungsalgorithmus lautet wie folgt:

1.  Initialisieren Sie NextVcn auf `Attribute->LowestVcn` und CurrentLcn auf 0.
2.  Initialisieren Sie den Bytestreamzeiger auf `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Legen Sie CurrentVcn auf NextVcn fest.
4.  Liest das nächste Byte aus dem Stream. Wenn es 0 ist, brechen Sie ab. else extrahieren *Sie v* und *l* wie zuvor beschrieben.
5.  Interpretieren Sie die *nächsten v* Bytes als Menge mit Vorsignieren, bei der zuerst das niedrig geordnete Byte angegeben wird. Entpacken Sie es sign-extended in 64 Bits, und fügen Sie es NextVcn hinzu.
6.  Interpretieren Sie die *nächsten l* Bytes als Menge mit Vorsignieren, und zuerst das niedrig geordnete Byte. Entpacken Sie die Anmeldung in 64 Bits, und fügen Sie sie CurrentLcn hinzu. Wenn dies einen CurrentLcn von 0 erzeugt, werden die VCNs von CurrentVcn zu NextVcn-1 nicht zugewiesen.
7.  Aktualisieren Sie die zwischengespeicherten Zuordnungsinformationen aus CurrentVcn, NextVcn und CurrentLcn.
8.  Fahren Sie mit Schritt 3 fort.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Masterdateitabelle](master-file-table.md)
</dt> </dl>

 

 
