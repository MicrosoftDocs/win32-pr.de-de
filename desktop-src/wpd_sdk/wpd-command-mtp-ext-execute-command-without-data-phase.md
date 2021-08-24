---
description: Der \_ WPD-BEFEHL \_ MTP \_ EXT EXECUTE COMMAND WITHOUT DATA PHASE sendet einen \_ \_ \_ \_ \_ MTP-Befehlsblock. Diesem Befehl ist keine nachfolgende Datenphase zugeordnet.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE -Befehl (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c4d1d5af4d1e4e712f3a39dd5cbb296133bb16f4de3b677da4a45fa7bbc204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806300"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>WPD-BEFEHL \_ \_ MTP \_ EXT EXECUTE COMMAND WITHOUT DATA PHASE \_ \_ \_ \_ \_ Command

Der **\_ WPD-BEFEHL \_ MTP \_ EXT EXECUTE COMMAND WITHOUT DATA \_ \_ \_ \_ \_ PHASE** sendet einen MTP-Befehlsblock. Diesem Befehl ist keine nachfolgende Datenphase zugeordnet.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ CATEGORY \_ MTP \_ EXT \_ VENDOR \_ OPERATIONS**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                      | VarType | Beschreibung                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ MTP \_ \_ EXT-VORGANGSCODE \_**   | VT \_ UI4 | Erforderlich. Identifiziert einen vom Anbieter erweiterten MTP-Vorgangscode.                                                                    |
| **\_WPD-EIGENSCHAFT: \_ MTP \_ \_ EXT-VORGANGS-PARAMS \_** | VT \_ UI4 | Erforderlich. Eine **IPortableDevicePropVariantCollection,** die die erforderlichen Parameter für den Herstellerbetriebscode identifiziert. |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                        | VarType | Beschreibung                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ MTP \_ \_ EXT-ANTWORTCODE \_**   | VT \_ UI4 | Erforderlich. Der Antwortcode für den Vorgangscode des Herstellers.                                                                      |
| **\_WPD-EIGENSCHAFT: \_ MTP \_ \_ EXT-ANTWORT-PARAMS \_** | VT \_ UI4 | Optional. Eine **IPortableDevicePropVariantCollection,** die alle Antwortparameter identifiziert. Diese Auflistung ist möglicherweise leer. |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mithilfe von [**IPortableDevice::SendCommand aufgerufen werden.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 




