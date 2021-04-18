---
description: In diesem Abschnitt wird das Format der Datensätze für die einzelnen Datensatz-Token-Token beschrieben. Die Informationen sind in die folgenden Abschnitte unterteilt.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Tokendatensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344800"
---
# <a name="token-records"></a>Tokendatensätze

In diesem Abschnitt wird das Format der Datensätze für die einzelnen Datensatz-Token-Token beschrieben. Die Informationen sind in die folgenden Abschnitte unterteilt.

-   [\_Tokenname](/windows)
-   [Token- \_ Zeichenfolge](/windows)
-   [Token- \_ Ganzzahl](/windows)
-   [\_tokenguid](/windows)
-   [\_Liste der tokeninteger \_](/windows)
-   [Liste der Token- \_ float \_](/windows)

## <a name="token_name"></a>\_Tokenname

Ein Datensatz variabler Länge. Auf das Token folgt ein count-Wert, der die Anzahl von Bytes angibt, die im Feld Name befolgt werden. Ein ASCII-Name der Längen Anzahl schließt den Datensatz ab.



| Feld | type       | Größe (Byte) | Inhalte                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | \_Tokenname                    |
| count | DWORD      | 4            | Länge des Namens Felds in Bytes |
| name  | Bytearray | count        | ASCII-Name                     |



 

## <a name="token_string"></a>Token- \_ Zeichenfolge

Ein Datensatz variabler Länge. Auf das Token folgt ein count-Wert, der die Anzahl der Bytes angibt, die im Feld "Zeichenfolge" befolgt werden. Eine ASCII-Zeichenfolge der Längen Anzahl setzt den Datensatz fort, der durch ein abschließendes Token abgeschlossen wird. Die Auswahl des Abschluss Zeichens wird durch Syntax Probleme bestimmt, die an anderer Stelle erläutert werden.



| Feld      | type       | Größe (Byte) | Inhalte                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | Token- \_ Zeichenfolge                    |
| count      | DWORD      | 4            | Länge des Zeichen folgen Felds in Bytes  |
| Schnür     | Bytearray | count        | ASCII-Zeichenfolge                     |
| chter | DWORD      | 4            | \_tokensemikolon oder \_ tokenkomma |



 

## <a name="token_integer"></a>Token- \_ Ganzzahl

Ein Datensatz mit fester Länge. Auf das Token folgt der ganzzahlige Wert.



| Feld | type  | Größe (Byte) | Inhalte       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | tOKEN- \_ Ganzzahl |
| Wert | DWORD | 4            | Einzelne Ganzzahl |



 

## <a name="token_guid"></a>\_tokenguid

Ein Datensatz mit fester Länge. Auf das Token folgen die vier Datenfelder, die vom OSF-DCE-Standard definiert werden.



| Feld | type       | Größe (Byte) | Inhalte          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | \_tokenguid       |
| Data1 | DWORD      | 4            | UUID-Datenfeld 1 |
| Data2 | WORD       | 2            | UUID-Datenfeld 2 |
| Data3 | WORD       | 2            | UUID-Datenfeld 3 |
| Data4 | Bytearray | 8            | UUID-Datenfeld 4 |



 

## <a name="token_integer_list"></a>\_Liste der tokeninteger \_

Ein Datensatz variabler Länge. Auf das Token folgt ein count-Wert, der die Anzahl von ganzen Zahlen angibt, die im Listenfeld befolgt werden. Aus Effizienzgründen sollten aufeinanderfolgende ganzzahlige Listen in einer einzigen Liste zusammengefügt werden.



| Feld | type  | Größe (Byte) | Inhalte                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | \_Liste der tokeninteger \_             |
| count | DWORD | 4            | Anzahl von ganzen Zahlen im Listenfeld |
| list  | DWORD | 4 x-Anzahl    | Ganzzahlige Liste                     |



 

## <a name="token_float_list"></a>Liste der Token- \_ float \_

Ein Datensatz variabler Länge. Auf das Token folgt ein count-Wert, der die Anzahl der Gleit Komma Zahlen oder Double-Werte angibt, die im Listenfeld nachverfolgt werden. Die Größe des Gleit Komma Werts (float oder Double) wird durch den Wert von float sizespecified im Dateiheader bestimmt. Aus Effizienzgründen sollten aufeinander folgende tokenzugriffslisten \_ \_ in einer einzigen Liste zusammengefügt werden.



| Feld | type               | Größe (Byte)   | Inhalte                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | Liste der tOKEN- \_ float \_                        |
| count | DWORD              | 4              | Anzahl von Gleit Komma-oder Double-Werte im Listenfeld |
| list  | float/double-Array | 4 oder 8 x Anzahl | Float-oder Double-Liste                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Binärcodierung](binary-encoding.md)
</dt> </dl>

 

 
