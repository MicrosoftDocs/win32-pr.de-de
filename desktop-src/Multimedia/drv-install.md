---
title: DRV_INSTALL Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er installiert ist. Der Treiber sollte alle benötigten Registrierungsschlüssel und-Werte erstellen und initialisieren und überprüfen, ob die unterstützenden Treiber und Hardware installiert und ordnungsgemäß konfiguriert sind.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957166"
---
# <a name="drv_install-message"></a>DRV- \_ Installations Meldung

Benachrichtigt den Treiber, dass er installiert ist. Der Treiber sollte alle benötigten Registrierungsschlüssel und-Werte erstellen und initialisieren und überprüfen, ob die unterstützenden Treiber und Hardware installiert und ordnungsgemäß konfiguriert sind.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*
</dt> <dd>

Der Bezeichner des installierbaren Treibers. Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle der installierbaren Treiber Instanz.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur oder **null**. Wenn eine Struktur angegeben wird, enthält Sie die Namen des Registrierungsschlüssels und des Werts, der dem Treiber zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück:



| Anforderung | Wert |
|-----------------|--------------------------------------------------------------------------------------------|
| drvcnf \_ OK      | Die Installation ist erfolgreich. Es ist keine weitere Aktion erforderlich.                             |
| drvcnf \_ Abbrechen  | Die Installation ist fehlgeschlagen.                                                                  |
| "drvcnf" \_ neu starten | Die Installation ist erfolgreich, wird jedoch erst wirksam, wenn das System neu gestartet wird. |



 

## <a name="remarks"></a>Bemerkungen

Der *lParam1* -Parameter wird nicht verwendet.

Einige installierbare Treiber fügen Konfigurationsinformationen an den Wert an, der dem Registrierungs Wert zugewiesen ist, der dem Treiber zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Installierbare Treiber](installable-drivers.md)
</dt> <dt>

[Installierbare Treiber Meldungen](installable-driver-messages.md)
</dt> </dl>

 

