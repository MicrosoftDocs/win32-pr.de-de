---
description: Der BEFEHL WPD \_ COMMAND \_ MTP \_ EXT GET VENDOR EXTENSION DESCRIPTION ruft die \_ \_ \_ \_ Beschreibungszeichenfolge der Anbietererweiterung ab. Diese Zeichenfolge wird durch ein DeviceInfo-Dataset definiert.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION-Befehl (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31622676161065ec685640789bc51eef64165542a9ebe4c9367ea1a03195e7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193509"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>\_WPD-BEFEHL \_ MTP \_ EXT GET VENDOR EXTENSION DESCRIPTION \_ \_ \_ \_ Befehl

Der **BEFEHL WPD \_ COMMAND \_ MTP EXT GET VENDOR \_ \_ EXTENSION \_ \_ \_ DESCRIPTION** ruft die Beschreibungszeichenfolge der Anbietererweiterung ab. Diese Zeichenfolge wird durch ein **DeviceInfo-Dataset** definiert.

## <a name="command-category"></a>Befehlskategorie

**MTP \_ \_ \_ \_ EXT-ANBIETERVORGÄNGE \_ DER WPD-KATEGORIE**

## <a name="parameters"></a>Parameter

Dieser Befehl weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                      | VarType    | BESCHREIBUNG                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **BESCHREIBUNG DER \_ WPD-EIGENSCHAFT \_ MTP \_ EXT VENDOR \_ EXTENSION \_ \_ DESCRIPTION** | VT \_ LPWSTR | Erforderlich. Gibt die Beschreibungszeichenfolge der Anbietererweiterung an. |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mit [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 




