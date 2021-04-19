---
description: Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her, die durch einen Zeitstempel ausgewählt wird.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Restorefromtime-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339711"
---
# <a name="restorefromtime-method-of-the-control-class"></a>Restorefromtime-Methode der Control-Klasse

Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her, die durch einen Zeitstempel ausgewählt wird.

## <a name="syntax"></a>Syntax


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Targettimestamplow* \[ in\]
</dt> <dd>

Stellen Sie die Sicherungsdatei mit diesem Zeitstempel wieder her. Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Targettimestamphigh* \[ in\]
</dt> <dd>

Stellen Sie die Sicherungsdatei mit diesem Zeitstempel wieder her. Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Oldtimestamplow* \[ in\]
</dt> <dd>

Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde. Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert). Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Oldtimestamphigh* \[ in\]
</dt> <dd>

Der Zeitstempel, zu dem die vorherige Konfiguration festgelegt wurde. Wenn nicht 0, aktiviert die atomizitäts Überprüfung: die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h., die Konfiguration wurde nicht in between geändert). Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Newtimestamplow* \[ vorgenommen\]
</dt> <dd>

Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde. Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Newtimestamphigh* \[ vorgenommen\]
</dt> <dd>

Der Zeitstempel, zu dem die neue Konfiguration festgelegt wurde,, wenn der-Befehl erfolgreich ausgeführt wurde. Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Originaltimestamplow* \[ vorgenommen\]
</dt> <dd>

Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde. Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Originaltimestamphigh* \[ vorgenommen\]
</dt> <dd>

Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde. Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ vorgenommen\]
</dt> <dd>

Die Text Zeichenfolge mit einer Erläuterung des Fehlers.

</dd> <dt>

*Warningstring* \[ vorgenommen\]
</dt> <dd>

Die Text Zeichenfolge mit Warnungen.

</dd> <dt>

*InfoString* \[ vorgenommen\]
</dt> <dd>

Die Text Zeichenfolge mit Informationen zur Konfiguration.

</dd> <dt>

*ErrorType* \[ vorgenommen\]
</dt> <dd>

Der Typ des Fehlers: Beachten Sie, dass 0 oder nicht vorhanden den Erfolg angibt.

<dt>

0
</dt> <dd>

Erfolg.

</dd> <dt>

1
</dt> <dd>

Ungültiges Argument Format

</dd> <dt>

2
</dt> <dd>

Ungültiger Argument Wert

</dd> <dt>

3
</dt> <dd>

Fehler beim Öffnen der Ressource (Socket).

</dd> <dt>

4
</dt> <dd>

Persistenz (Datei Schreibfehler)

</dd> <dt>

5
</dt> <dd>

Unteilbarkeit-Fehler (der alte Zeitstempel entsprach nicht.)

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

<dl> <dt>


</dt> <dd>

0

Fehler

</dd> <dt>


</dt> <dd>

1

Erfolg

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>Booteventcollector WMI. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

