---
description: Der BEFEHL WPD \_ COMMAND \_ MTP \_ EXT END DATA TRANSFER schließt eine \_ \_ \_ Datenübertragung ab und liest die Antwort vom Gerät.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER-Befehl (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc064d1de151e8b3ebd54245249d8bf9ffa8ecbd41bbe61c36768add4329f092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026774"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>\_WPD-BEFEHL \_ MTP \_ EXT END \_ DATA \_ \_ TRANSFER-Befehl

Der **BEFEHL WPD \_ COMMAND \_ MTP EXT END DATA \_ \_ \_ \_ TRANSFER** schließt eine Datenübertragung ab und liest die Antwort vom Gerät. Die Übertragung wird entweder mit dem BEFEHL [**WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO \_ \_ \_ \_ \_ \_ READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) oder mit dem Befehl [**WPD COMMAND \_ \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO \_ \_ \_ \_ \_ \_ WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) initiiert.

## <a name="command-category"></a>Befehlskategorie

**MTP \_ \_ \_ \_ EXT-ANBIETERVORGÄNGE \_ DER WPD-KATEGORIE**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                      | VarType    | Beschreibung                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER \_ \_ CONTEXT** | VT \_ LPWSTR | Erforderlich. Identifiziert den Kontext, der von einem früheren Methodenaufruf zurückgegeben wird. |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                        | VarType | Beschreibung                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **MTP \_ \_ \_ \_ EXT-ANTWORTCODE \_ FÜR WPD-EIGENSCHAFT**   | VT \_ UI4 | Erforderlich.Der Antwortcode an den Vorgangscode des Anbieters.                                                                                |
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT RESPONSE \_ \_ PARAMS** | VT \_ UI4 | Optional. Eine **IPortableDevicePropVariantCollection-Auflistung,** die alle Antwortparameter identifiziert. Diese Auflistung kann leer sein. |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mit [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

