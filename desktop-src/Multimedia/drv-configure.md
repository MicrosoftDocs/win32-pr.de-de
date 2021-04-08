---
title: DRV_CONFIGURE Meldung (MMSYSTEM. h)
description: Weist den installierbaren Treiber an, sein Konfigurations Dialogfeld anzuzeigen, und ermöglicht es dem Benutzer, neue Einstellungen für die angegebene installierbare Treiber Instanz anzugeben.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957169"
---
# <a name="drv_configure-message"></a>DRV- \_ configure-Meldung

Weist den installierbaren Treiber an, sein Konfigurations Dialogfeld anzuzeigen, und ermöglicht es dem Benutzer, neue Einstellungen für die angegebene installierbare Treiber Instanz anzugeben.

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

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Handle des übergeordneten Fensters. Dieses Fenster wird als übergeordnetes Fenster für das Konfigurations Dialogfeld verwendet.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Adresse einer [**drvconfiginfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) -Struktur oder **null**. Wenn die Struktur angegeben wird, enthält Sie die Namen des Registrierungsschlüssels und des Werts, der dem Treiber zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück:



| Anforderung | Wert |
|-----------------|----------------------------------------------------------------------------------------------------|
| drvcnf \_ OK      | Die Konfiguration ist erfolgreich. Es ist keine weitere Aktion erforderlich.                                    |
| drvcnf \_ Abbrechen  | Der Benutzer hat das Dialogfeld abgebrochen. Es ist keine weitere Aktion erforderlich.                                   |
| "drvcnf" \_ neu starten | Die Konfiguration ist erfolgreich, aber die Änderungen werden erst wirksam, wenn das System neu gestartet wird. |



 

## <a name="remarks"></a>Bemerkungen

Einige installierbare Treiber fügen Konfigurationsinformationen an den Wert an, der dem Registrierungs Wert zugewiesen ist, der dem Treiber zugeordnet ist.

Die \_ \_ Rückgabewerte für den drv-Abbruch-, drv OK-und drv- \_ Neustart sind veraltet. Sie wurden durch drvcnf \_ Cancel, drvcnf \_ OK bzw. drvcnf- \_ Neustart ersetzt.

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

 

