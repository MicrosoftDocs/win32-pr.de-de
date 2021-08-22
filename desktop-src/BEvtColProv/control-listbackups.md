---
description: Gibt die Liste der gespeicherten Sicherungskonfigurationsdateien zurück, die wiederhergestellt werden können.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: ListBackups-Methode der Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: ba6a3f042a6bd8f01e4bede00e22bda95ca28ebe7cc2beb33a12c6b49deba6bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589120"
---
# <a name="listbackups-method-of-the-control-class"></a>ListBackups-Methode der Control-Klasse

Gibt die Liste der gespeicherten Sicherungskonfigurationsdateien zurück, die wiederhergestellt werden können.

## <a name="syntax"></a>Syntax


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OriginalTimestampLow* \[ out\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die aktuelle Konfiguration festgelegt wurde (wenn sie aus der Sicherung wiederhergestellt wurde, enthält den ursprünglichen Zeitstempel). Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

Der Zeitstempel des Zeitpunkts, zu dem die aktuelle Konfiguration festgelegt wurde (wenn sie aus der Sicherung wiederhergestellt wurde, enthält den ursprünglichen Zeitstempel). Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Dateien* \[ out\]
</dt> <dd>

Die Liste der verfügbaren Sicherungsdateien in der Reihenfolge von der neuesten bis zur ältesten.

</dd> <dt>

*FilesTimestampLow* \[ out\]
</dt> <dd>

Für jede Sicherungsdatei der Zeitstempel des Zeitpunkts, zu dem die Konfiguration festgelegt wurde. Dies ist der untere Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*FilesTimestampHigh* \[ out\]
</dt> <dd>

Für jede Sicherungsdatei der Zeitstempel des Zeitpunkts, zu dem die Konfiguration festgelegt wurde. Dies ist der hohe Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

