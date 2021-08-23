---
description: Stellen Sie die aktive Konfiguration des Collectors aus der vorherigen Sicherungsdatei wieder her (bestimmt durch Zurückgehen vom aktuellen ursprünglichen Zeitstempel).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Rückgängig-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: e46649473da31fac09c65fcecaf44e91eba049c7ddce089d7f3c5ba9de2f8e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589040"
---
# <a name="undo-method-of-the-control-class"></a>Rückgängig-Methode der Control-Klasse

Stellen Sie die aktive Konfiguration des Collectors aus der vorherigen Sicherungsdatei wieder her (bestimmt durch Zurückgehen vom aktuellen ursprünglichen Zeitstempel). Wenn die Konfiguration gerade festgelegt wurde, bedeutet dies, dass diese Änderung rückgängig gemacht wird. Die aufeinanderfolgenden Aufrufe werden auf die früheren und früheren Konfigurationen rückgängig machen. Gibt bei Erfolg 1 und bei Fehler 0 zurück.

## <a name="syntax"></a>Syntax


```mof
Uint32 Undo(
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

*OldTimestampLow* \[ In\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die vorherige Konfiguration festgelegt wurde. Wenn nicht 0, aktiviert die Atomaritätsprüfung: Die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h. die Konfiguration wurde zwischendurch nicht geändert). Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ In\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die vorherige Konfiguration festgelegt wurde. Wenn nicht 0, aktiviert die Atomaritätsprüfung: Die neue Konfiguration wird nur angewendet, wenn der Zeitstempel der alten Konfiguration übereinstimmt (d. h. die Konfiguration wurde zwischendurch nicht geändert). Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

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

Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde. Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

Der ursprüngliche Zeitstempel, zu dem die wiederhergestellte Konfiguration zum ersten Mal festgelegt wurde. Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

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

Der Typ des Fehlers: Beachten Sie, dass "0" oder "nicht vorhanden" auf Erfolg hinweist.

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
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

