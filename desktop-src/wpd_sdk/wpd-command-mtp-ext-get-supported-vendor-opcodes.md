---
description: Der WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Supported \_ Vendor \_ Opcodes sendet einen MTP-Befehls Block. Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369168"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Supported \_ Vendor \_ Opcodes Befehl

Der **WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Supported \_ Vendor \_ Opcodes** sendet einen MTP-Befehls Block. Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**

## <a name="parameters"></a>Parameter

Dieser Befehl weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                | VarType | BESCHREIBUNG                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Hersteller \_ Vorgangs \_ Codes** | VT \_ UI4 | Erforderlich. Eine **iportabledevicepropvariantcollection** , die alle vom Hersteller erweiterten Vorgangs Codes enthält. |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mithilfe von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wpdmtpextensions. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 




