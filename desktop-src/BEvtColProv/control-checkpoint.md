---
description: Wenn die aktuelle Konfiguration ein Ergebnis der Rückgängig-/Wiederholungs-/Wiederherstellungsfunktion ist, markiert sie so, als ob sie explizit festgelegt wurde, sodass der Verlauf die Zeit bei der Festlegung beibehalten und bei der nächsten Konfigurationsänderung eine Sicherungsdatei für sie erstellt wird.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Checkpoint-Methode der Control-Klasse (Srrestoreptapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: ff71086703e409331e420fd064f73ff2406ec4e5167ea97da78b2afc498bf244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579850"
---
# <a name="checkpoint-method-of-the-control-class"></a>Checkpoint-Methode der Control-Klasse

Wenn die aktuelle Konfiguration ein Ergebnis der Rückgängig-/Wiederholungs-/Wiederherstellungsfunktion ist, markiert sie so, als ob sie explizit festgelegt wurde, sodass der Verlauf die Zeit bei der Festlegung beibehalten und bei der nächsten Konfigurationsänderung eine Sicherungsdatei für sie erstellt wird. Wenn die aktuelle Konfiguration bereits explizit festgelegt wurde, hat keine Auswirkungen.

## <a name="syntax"></a>Syntax


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldTimestampLow* \[ In\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die aktuelle Konfiguration festgelegt wurde. Wenn nicht 0, aktiviert die Atomaritätsprüfung: Die Aktion wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h. die Konfiguration wurde zwischendurch nicht geändert). Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ In\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die aktuelle Konfiguration festgelegt wurde. Wenn nicht 0, aktiviert die Atomaritätsprüfung: Die Aktion wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h. die Konfiguration wurde zwischendurch nicht geändert). Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Die Textzeichenfolge mit Erklärung des Fehlers.

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

Der Typ des Fehlers. Beachten Sie, dass "0" oder "fehlt" auf Erfolg hinweist.

<dt>

0
</dt> <dd>

Erfolg.

</dd> <dt>

1
</dt> <dd>

Ungültiges Argumentformat

</dd> <dt>

2
</dt> <dd>

Ungültiger Argumentwert

</dd> <dt>

3
</dt> <dd>

Fehler beim Öffnen der Ressource (Socket)

</dd> <dt>

4
</dt> <dd>

Persistenzfehler (Dateischreibfehler)

</dd> <dt>

5
</dt> <dd>

Atomicity-Fehler (der alte Zeitstempel stimmte nicht überein)

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
| Namespace<br/>                | \\Stamm-Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| Header<br/>                   | <dl> <dt>Srrestoreptapi.h</dt> </dl>          |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

