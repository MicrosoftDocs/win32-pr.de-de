---
description: In diesem Abschnitt wird das Format der Datensätze für jedes der Datensatztoken beschrieben. Die Informationen sind in die folgenden Abschnitte unterteilt.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Tokendatensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456ee591f15cac6e6a3d2fecaad3dfca9f0709b39a63d20fe198e591a199f4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797422"
---
# <a name="token-records"></a>Tokendatensätze

In diesem Abschnitt wird das Format der Datensätze für jedes der Datensatztoken beschrieben. Die Informationen sind in die folgenden Abschnitte unterteilt.

-   [\_TOKENNAME](/windows)
-   [\_TOKENZEICHENFOLGE](/windows)
-   [TOKEN \_ INTEGER](/windows)
-   [\_TOKEN-GUID](/windows)
-   [TOKEN \_ INTEGER \_ LIST](/windows)
-   [TOKEN \_ FLOAT \_ LIST](/windows)

## <a name="token_name"></a>\_TOKENNAME

Ein Datensatz variabler Länge. Auf das Token folgt ein Count-Wert, der die Anzahl von Bytes angibt, die im Feld name folgen. Ein ASCII-Name der Längenanzahl schließt den Datensatz ab.



| Feld | type       | Größe (Byte) | Inhalte                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | \_Tokenname                    |
| count | DWORD      | 4            | Länge des Namensfelds in Bytes |
| name  | BYTE-Array | count        | ASCII-Name                     |



 

## <a name="token_string"></a>\_TOKENZEICHENFOLGE

Ein Datensatz variabler Länge. Auf das Token folgt ein Count-Wert, der die Anzahl von Bytes angibt, die im Zeichenfolgenfeld folgen. Eine ASCII-Zeichenfolge mit Längenanzahl setzt den Datensatz fort, der durch ein abschließendes Token abgeschlossen wird. Die Auswahl des Abschlusszeichens wird durch Syntaxprobleme bestimmt, die an anderer Stelle erläutert werden.



| Feld      | type       | Größe (Byte) | Inhalte                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | \_Tokenzeichenfolge                    |
| count      | DWORD      | 4            | Länge des Zeichenfolgenfelds in Bytes  |
| Schnur     | BYTE-Array | count        | ASCII-Zeichenfolge                     |
| Terminator | DWORD      | 4            | tOKEN \_ SEMIKOLON oder \_ TOKEN-KOMMA |



 

## <a name="token_integer"></a>TOKEN \_ INTEGER

Ein Datensatz fester Länge. Auf das Token folgt der erforderliche ganzzahlige Wert.



| Feld | type  | Größe (Byte) | Inhalte       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | tOKEN \_ INTEGER |
| Wert | DWORD | 4            | Einzelne ganze Zahl |



 

## <a name="token_guid"></a>\_TOKEN-GUID

Ein Datensatz fester Länge. Auf das Token folgen die vier Datenfelder, die durch den OSF DCE-Standard definiert sind.



| Feld | type       | Größe (Byte) | Inhalte          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | tOKEN \_ GUID       |
| Data1 | DWORD      | 4            | UUID-Datenfeld 1 |
| Data2 | WORD       | 2            | UUID-Datenfeld 2 |
| Data3 | WORD       | 2            | UUID-Datenfeld 3 |
| Data4 | BYTE-Array | 8            | UUID-Datenfeld 4 |



 

## <a name="token_integer_list"></a>TOKEN \_ INTEGER \_ LIST

Ein Datensatz variabler Länge. Auf das Token folgt ein Count-Wert, der die Anzahl der im Listenfeld folgenden ganzen Zahlen angibt. Aus Effizienzgewährungsgewährungen sollten aufeinanderfolgende ganzzahlige Listen in einer einzelnen Liste zusammengesetzt werden.



| Feld | type  | Größe (Byte) | Inhalte                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | tOKEN \_ INTEGER \_ LISt             |
| count | DWORD | 4            | Anzahl von ganzen Zahlen im Listenfeld |
| list  | DWORD | 4 x Anzahl    | Ganzzahlige Liste                     |



 

## <a name="token_float_list"></a>TOKEN \_ FLOAT \_ LIST

Ein Datensatz variabler Länge. Auf das Token folgt ein Count-Wert, der die Anzahl der floats oder doubles angibt, die im Listenfeld folgen. Die Größe des Gleitkommawerts (float oder double) wird durch den Wert der float-Größe bestimmt, der im Dateiheader angegeben ist. Zur Effizienz sollten aufeinander folgende TOKEN \_ FLOAT \_ LISTs in einer einzigen Liste zusammengesetzt werden.



| Feld | type               | Größe (Byte)   | Inhalte                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | tOKEN \_ FLOAT \_ LISt                        |
| count | DWORD              | 4              | Anzahl der Gleitkommazahlen oder Doubles im Listenfeld |
| list  | float/double-Array | 4 oder 8 x Anzahl | Float- oder Double-Liste                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Binärcodierung](binary-encoding.md)
</dt> </dl>

 

 
