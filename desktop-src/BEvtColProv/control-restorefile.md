---
description: Stellen Sie die aktive Konfiguration des Collectors aus einer Sicherungsdatei wieder her.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: RestoreFile-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 148b35199822c98ca03041561f402dc5acaadddf067b9eeecd80e9b32e325db2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589110"
---
# <a name="restorefile-method-of-the-control-class"></a>RestoreFile-Methode der Control-Klasse

Stellen Sie die aktive Konfiguration des Collectors aus einer Sicherungsdatei wieder her.

## <a name="syntax"></a>Syntax


```mof
Uint32 RestoreFile(
  [in]  string File,
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

*Datei* \[ In\]
</dt> <dd>

Name der wiederherzustellenden Sicherungsdatei aus der liste, die von ListBackups() zurückgegeben wird.

</dd> <dt>

*OldTimestampLow* \[ In\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die vorherige Konfiguration festgelegt wurde. Wenn nicht 0, wird die Atomaritätsprüfung aktiviert: Die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration entspricht (d. h., die Konfiguration wurde dazwischen nicht geändert). Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ In\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die vorherige Konfiguration festgelegt wurde. Wenn nicht 0, wird die Atomaritätsprüfung aktiviert: Die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration entspricht (d. h., die Konfiguration wurde dazwischen nicht geändert). Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampLow* \[ out\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die neue Konfiguration festgelegt wurde, wenn der Aufruf erfolgreich war. Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die neue Konfiguration festgelegt wurde, wenn der Aufruf erfolgreich war. Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampLow* \[ out\]
</dt> <dd>

Der ursprüngliche Zeitstempel des Zeitpunkts, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde. Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

Der ursprüngliche Zeitstempel des Zeitpunkts, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde. Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Die Textzeichenfolge mit Erläuterung des Fehlers.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

Die Textzeichenfolge mit Warnungen.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

Die Textzeichenfolge mit Informationen zur Konfiguration.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

Der Typ des Fehlers: Beachten Sie, dass "0" oder "absent" für erfolg steht.

<dt>

0
</dt> <dd>

Erfolg.

</dd> <dt>

1
</dt> <dd>

Fehlerhaftes Argumentformat

</dd> <dt>

2
</dt> <dd>

Fehlerhafter Argumentwert

</dd> <dt>

3
</dt> <dd>

Fehler beim Öffnen der Ressource (Socket)

</dd> <dt>

4
</dt> <dd>

Persistenzfehler (Dateischreiben)

</dd> <dt>

5
</dt> <dd>

Atomaritätsfehler (der alte Zeitstempel hat nicht überein")

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

