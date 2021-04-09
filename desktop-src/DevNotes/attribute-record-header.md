---
description: Stellt einen Attributdaten Satz dar.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER Struktur
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
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860615"
---
# <a name="attribute_record_header-structure"></a>Attribut \_ Daten Satz- \_ Header Struktur

\[Diese Struktur gilt nur für Version 3 von NTFS-Volumes. Sie kann in zukünftigen Versionen geändert werden.\]

Stellt einen Attributdaten Satz dar.

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

Der Attributtyp Code.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ Informationen**</dt> <dt>0x10</dt> </dl> | Dateiattribute (z. b. "schreibgeschützt" und "Archiv"), Zeitstempel (z. b. Dateierstellung und Letzte Änderung) und die Anzahl der festen Links.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ Liste**</dt> <dt>0x20</dt> </dl>                   | Eine Liste der Attribute, die die Datei bilden, und der Datei Verweis des MFT-Datei Datensatzes, in dem sich die einzelnen Attribute befinden.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ Name**</dt> <dt>0x30</dt> </dl>                                  | Der Name der Datei in Unicode-Zeichen.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Ein 64-Byte-Objekt Bezeichner, der vom Link Überwachungsdienst zugewiesen wird.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ Name**</dt> <dt>0x60</dt> </dl>                            | Die Volumebezeichnung. In der $Volume-Datei vorhanden.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_ Informationen**</dt> <dt>0x70</dt> </dl>       | Die Volumeinformationen. In der $Volume-Datei vorhanden.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | Der Inhalt der Datei.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_**</dt>Stamm <dt>0x90</dt> </dl>                               | Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_ Zuordnung**</dt> <dt>0xa0</dt> </dl>             | Wird verwendet, um die Dateinamen Zuordnung für große Verzeichnisse zu implementieren.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0xb0</dt> </dl>                                            | Ein Bitmapindex für ein großes Verzeichnis.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ Punkt**</dt> <dt>0xC0</dt> </dl>                      | Die Daten des Analyse Punkts.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Die Größe des Attributdaten Satzes in Byte. Dieser Wert gibt die erforderliche Größe für die Daten Satz Variante an und wird immer auf die nächstgelegene Quadword-Grenze gerundet.

</dd> <dt>

**FormCode**
</dt> <dd>

Der Attribut Formular Code.



| Wert                                                                                                                                                                                                                            | Bedeutung                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**Residente \_ Formular**</dt> <dt>0x00</dt> </dl>          | Der Wert ist im Datei Daten Satz enthalten und folgt unmittelbar dem Attributdaten Satz Header.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <dt>**Nicht residente \_ Formular**</dt> <dt>0x01</dt> </dl> | Der Wert ist in anderen Sektoren auf dem Datenträger enthalten.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

Die Größe des optionalen Attribut namens in Zeichen oder 0, wenn kein Attribut Name vorhanden ist. Die maximale Länge des Attribut namens beträgt 255 Zeichen.

</dd> <dt>

**Nameoffset**
</dt> <dd>

Der Offset des Attribut namens vom Anfang des Attributdaten Satzes in Byte. Wenn der **namelength** -Member 0 ist, ist dieser Member nicht definiert.

</dd> <dt>

**Flags**
</dt> <dd>

Die Attributflags.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Attribut \_ Flag- \_ Komprimierungs \_ Maske** (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Attribut \_ \_Sparse-Flag** (0X8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Attribut \_ Flag \_ verschlüsselt** (0x4000)
</dt> </dl> </dd> <dt>

**Instanz**
</dt> <dd>

Die eindeutige Instanz für dieses Attribut im Datei Daten Satz.

</dd> <dt>

**Form**
</dt> <dd>

Wenn sich der **FormCode** -Member in einem Residenten \_ Formular befindet, ist die Union eine **residente** Struktur. Wenn **FormCode** nicht residente \_ Form ist, ist die Union eine **nicht residente** Struktur.

<dl> <dt>

**Bewohnten**
</dt> <dd> <dl> <dt>

**Valuelength**
</dt> <dd>

Die Größe des Attribut Werts in Bytes.

</dd> <dt>

**Valueoffset**
</dt> <dd>

Der Offset bis zum Wert vom Anfang des Attributdaten Satzes in Byte.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl> </dd> <dt>

**Nicht residente**
</dt> <dd> <dl> <dt>

**Lowestvcn**
</dt> <dd>

Die niedrigste virtuelle Cluster Nummer (VCN), die von diesem Attributdaten Satz abgedeckt wird.

</dd> <dt>

**Highestvcn**
</dt> <dd>

Die höchste VCN, die von diesem Attributdaten Satz abgedeckt wird.

</dd> <dt>

**Mappingpaare**
</dt> <dd>

Der Offset für das Array der Zuordnungspaare vom Anfang des Attributdaten Satzes (in Bytes). Weitere Informationen finden Sie in den Hinweisen.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> <dt>

**Zu"zuder Länge"**
</dt> <dd>

Die zugeordnete Größe der Datei in Bytes. Dieser Wert ist ein gleich Vielfaches der Clustergröße. Dieser Member ist ungültig, wenn der **lowestvcn** -Member ungleich NULL ist.

</dd> <dt>

**FileSize**
</dt> <dd>

Die Dateigröße (das höchste Byte, das gelesen werden kann, plus 1) in Bytes. Dieser Member ist ungültig, wenn **lowestvcn** ungleich 0 (null) ist.

</dd> <dt>

**Validdatalength**
</dt> <dd>

Die gültige Daten Länge (das höchste initialisierte Byte plus 1) in Bytes. Dieser Wert wird auf die nächste Cluster Grenze gerundet. Dieser Member ist ungültig, wenn **lowestvcn** ungleich 0 (null) ist.

</dd> <dt>

**Total zugeordnet**
</dt> <dd>

Die Gesamtmenge, die für die Datei zugewiesen wurde (die Summe der zugewiesenen Cluster).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass es für diese Struktur keine zugeordnete Header Datei gibt.

Diese Struktur Definition ist nur für die Hauptversion 3 und die neben Version 0 oder 1 gültig, wie von [**FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)berichtet.

Attributdaten Sätze werden immer an einer Quadword-Grenze ausgerichtet.

Wenn das Attribut nicht Resident ist, enthält der Attributdaten Satz Header eine Liste mit Abruf Informationen, die eine Zuordnung zwischen VCN und logischer Cluster Nummer (LCN) für das Attribut bereitstellt. Wenn die Abruf Informationen nicht in das Basisdatei Segment passen, können Sie in einem externen Datei Daten Satz Segment eigenständig gespeichert werden. Wenn es immer noch nicht in ein externes Datei Daten Satz Segment passt, gibt es eine Bereitstellung in der Attribut Liste, die mehrere Einträge für ein Attribut enthält, das zusätzliche Abruf Informationen erfordert.

Das Array der Zuordnungspaare wird in komprimierter Form gespeichert und geht davon aus, dass die Informationen dekomprimiert und vom System zwischengespeichert werden. Sie besteht aus einer Reihe von nextvcn/currentlcn-Paaren. Wenn eine Datei z. b. eine einzelne Ausführen von 8 Clustern, beginnend bei LCN 128, und die Datei bei lowestvcn 0 startet, verfügt das Array der Zuordnungspaare nur über einen Eintrag (nextvcn = 8 und currentlcn = 128). Das Array ist ein Bytestream, der die Änderungen an den Arbeits Variablen speichert, wenn Sie sequenziell verarbeitet werden. Der Bytestream muss wie folgt als ein null terminierter Stream von drei-ELN interpretiert werden:

count Byte = *v* + (*l* \* 16)

Dabei ist *v* die Anzahl der geänderten VCN-Bytes mit niedriger Ordnung und *l* die Anzahl der geänderten LCN-Bytes mit niedriger Reihenfolge.

Der Dekomprimierungs Algorithmus lautet wie folgt:

1.  Initialisieren Sie nextvcn auf `Attribute->LowestVcn` und currentlcn auf 0.
2.  Initialisieren Sie den bytestreamzeiger auf `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Legen Sie currentvcn auf nextvcn fest.
4.  Liest das nächste Byte aus dem Datenstrom. Wenn der Wert 0 ist, dann unterbrechen. Extrahieren Sie andernfalls *v* und *l* wie zuvor beschrieben.
5.  Interpretieren Sie die nächsten *v* Bytes als signierte Menge mit dem nieder wertigen Byte zuerst. Entpacken Sie die Anmelde Informationen in 64 Bits, und fügen Sie Sie nextvcn hinzu.
6.  Interpretieren Sie die nächsten *l* -Bytes als signierte Menge mit dem nieder wertigen Byte First. Entpacken Sie Sign-Extended in 64 Bits, und fügen Sie es currentlcn hinzu. Wenn dies eine currentlcn von 0 ergibt, wird der vcns von currentvcn zu nextvcn – 1 nicht zugeordnet.
7.  Aktualisieren Sie die zwischengespeicherten Mapping-Informationen von currentvcn, nextvcn und currentlcn.
8.  Fahren Sie mit Schritt 3 fort.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Master Dateitabelle](master-file-table.md)
</dt> </dl>

 

 
