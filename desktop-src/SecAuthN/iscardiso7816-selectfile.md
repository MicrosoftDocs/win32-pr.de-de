---
description: Die selectfile-Methode erstellt einen APDU-Befehl (Application Protocol Data Unit), mit dem eine aktuelle elementare Datei innerhalb eines logischen Kanals festgelegt wird. Nachfolgende Befehle können implizit über den logischen Kanal auf die aktuelle Datei verweisen.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816:: selectfile-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216211"
---
# <a name="iscardiso7816selectfile-method"></a>ISCardISO7816:: selectfile-Methode

\[Die **selectfile** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **selectfile** -Methode erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), mit dem eine aktuelle elementare Datei innerhalb eines logischen Kanals festgelegt wird. Nachfolgende Befehle können implizit über den logischen Kanal auf die aktuelle Datei verweisen.

Wenn Sie ein Verzeichnis (DF) im Kartendatei Speicher auswählen, d. –. das Stammverzeichnis (MF) des Dateispeicher –, wird es zur aktuellen DF. Nach einer solchen Auswahl kann über diesen logischen Kanal auf eine implizite aktuelle elementare Datei verwiesen werden.

Wenn Sie eine elementare Datei auswählen, werden die ausgewählte Datei und deren übergeordnetes Element als aktuelle Dateien festgelegt.

Nachdem die Antwort zurückgesetzt wurde, wird der MF implizit über den logischen Standard Kanal ausgewählt, es sei denn, er wurde in den Verlaufs Bytes oder in der ursprünglichen Daten Zeichenfolge anders angegeben.

## <a name="syntax"></a>Syntax


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*byP1* \[ in\]
</dt> <dd>

Auswahl Steuerelement.



| P1 (oberes Byte in Word): 8 7 6 5 4 3 2 1                                                                                                                                                            | Bedeutung                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <dt>**000000xx**</dt><dt></dt> </dl> | Datei-ID auswählen<br/>          |
| <span id="00000000"></span><dl> <dt>**00000000**</dt><dt></dt> </dl>                            | EF, DF oder MF<br/>           |
| <span id="00000001"></span><dl> <dt>**00000001**</dt><dt></dt> </dl>                            | Untergeordnete DF<br/>                |
| <span id="00000010"></span><dl> <dt>**00000010**</dt><dt></dt> </dl>                            | EF unter DF<br/>             |
| <span id="00000011"></span><dl> <dt>**00000011**</dt><dt></dt> </dl>                            | Übergeordnete DF der aktuellen DF<br/> |



 

Wenn P1 = 00 ist, weiß die Karte entweder aufgrund einer bestimmten Codierung der Datei-ID oder aufgrund des Kontexts der Ausführung des Befehls, wenn die ausgewählte Datei das MF, ein DF oder EF ist.

Wenn P1-P2 = 0000, wenn eine Datei-ID bereitgestellt wird, wird Sie in den folgenden Umgebungen eindeutig sein:

-   Unmittelbare untergeordnete Elemente der aktuellen DF
-   Übergeordnete DF
-   Unmittelbare untergeordnete Elemente der übergeordneten DF

Wenn P1-P2 = 0000 und das Datenfeld leer oder gleich 3f00 ist, wählen Sie den MF aus.

Bei P1 = 04 ist das Datenfeld ein DF-Name, der möglicherweise rechts abgeschnitten ist.

Wenn dies unterstützt wird, müssen nachfolgende Befehle desselben Datenfelds DFS auswählen, deren Namen mit dem Datenfeld übereinstimmen (d. h. mit dem Feld "Befehlsdaten" beginnen). Wenn die Karte den Befehl mit einem leeren Datenfeld akzeptiert, können alle oder eine Teilmenge der DFS nacheinander ausgewählt werden.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Auswahl Steuerelement.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Daten für den Vorgang bei Bedarf. andernfalls **null**. Zu den Datentypen, die in diesem Parameter übergeben werden, gehören:

-   Datei-ID
-   Pfad aus dem MF
-   Pfad der aktuellen DF
-   Name der DF

</dd> <dt>

*lbytestoread* \[ in\]
</dt> <dd>

Leer (d. h. 0) oder die maximale Länge der Daten, die als Antwort erwartet werden.

</dd> <dt>

*ppcmd* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.

Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt. Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und über den *ppcmd* -Zeiger zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Es wurde ein fehlerhafter Zeiger übermittelt.<br/>      |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Sofern nicht anders angegeben, ändert die korrekte Ausführung des gekapselten Befehls den Sicherheitsstatus gemäß den folgenden Regeln:

-   Wenn die aktuelle elementare Datei geändert wird oder wenn keine aktuelle elementare Datei vorhanden ist, geht der für eine frühere aktuelle elementare Datei spezifische Sicherheitsstatus verloren.
-   Wenn das aktuelle Dateispeicher Verzeichnis (DF) ein Nachfolger von ist oder mit dem früheren aktuellen DF identisch ist, geht der Sicherheitsstatus, der für die vorherige aktuelle DF spezifisch ist, verloren. Der Sicherheitsstatus, der für alle gemeinsamen Vorgänger der vorherigen und neuen aktuellen DF gilt, wird beibehalten.

Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert<br/>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
