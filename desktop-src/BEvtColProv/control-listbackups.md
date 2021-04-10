---
description: Gibt die Liste der gespeicherten Sicherungs Konfigurationsdateien zurück, die wieder hergestellt werden können.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Listbackups-Methode der Steuerelement Klasse
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
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125839"
---
# <a name="listbackups-method-of-the-control-class"></a>Listbackups-Methode der Steuerelement Klasse

Gibt die Liste der gespeicherten Sicherungs Konfigurationsdateien zurück, die wieder hergestellt werden können.

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

*Originaltimestamplow* \[ vorgenommen\]
</dt> <dd>

Der Zeitstempel, zu dem die aktuelle Konfiguration festgelegt wurde (wenn Sie von einer Sicherung wieder hergestellt wird, enthält den ursprünglichen Zeitstempel). Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Originaltimestamphigh* \[ vorgenommen\]
</dt> <dd>

Der Zeitstempel, zu dem die aktuelle Konfiguration festgelegt wurde (wenn Sie von einer Sicherung wieder hergestellt wird, enthält den ursprünglichen Zeitstempel). Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Dateien* \[ vorgenommen\]
</dt> <dd>

Die Liste der verfügbaren Sicherungsdateien, von der neuesten zum ältesten.

</dd> <dt>

*Filestimestamplow* \[ vorgenommen\]
</dt> <dd>

Für jede Sicherungsdatei der Zeitstempel, zu dem die Konfiguration festgelegt wurde. Dies ist der niedrige Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Filestimestamphigh* \[ vorgenommen\]
</dt> <dd>

Für jede Sicherungsdatei der Zeitstempel, zu dem die Konfiguration festgelegt wurde. Dies ist der große Teil von [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

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

 

