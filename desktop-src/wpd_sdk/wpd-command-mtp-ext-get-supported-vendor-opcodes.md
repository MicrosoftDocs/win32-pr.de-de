---
description: Der BEFEHL WPD \_ COMMAND \_ MTP \_ EXT GET SUPPORTED \_ VENDOR \_ \_ \_ OPCODES sendet einen MTP-Befehlsblock. Diesem Befehl ist keine nachfolgende Datenphase zugeordnet.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES Befehl (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b0ab00fc3ada963e56dced49f97d3c1dbca578dfc5c1cded4735f9df947ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927970"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>WPD-BEFEHL \_ \_ MTP \_ EXT GET SUPPORTED \_ VENDOR \_ \_ \_ OPCODES Command

Der **BEFEHL WPD \_ COMMAND \_ MTP EXT GET SUPPORTED \_ \_ VENDOR \_ \_ \_ OPCODES** sendet einen MTP-Befehlsblock. Diesem Befehl ist keine nachfolgende Datenphase zugeordnet.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ CATEGORY \_ MTP \_ EXT \_ VENDOR \_ OPERATIONS**

## <a name="parameters"></a>Parameter

Dieser Befehl weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                | VarType | Beschreibung                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT VENDOR \_ OPERATION \_ \_ CODES** | VT \_ UI4 | Erforderlich. Eine **IPortableDevicePropVariantCollection,** die alle vom Anbieter erweiterten Vorgangscodes enthält. |



 

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

 

 




