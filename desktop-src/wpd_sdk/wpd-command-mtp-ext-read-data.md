---
description: Der BEFEHL WPD COMMAND MTP EXT READ DATA ruft Daten vom Gerät ab, nachdem der \_ \_ BEFEHL \_ \_ \_ WPD COMMAND \_ \_ MTP EXT EXECUTE COMMAND \_ WITH DATA TO READ ausgeführt \_ \_ \_ \_ \_ \_ wurde.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA Befehl (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5aeee37e1922f91e9a9fac7881369364d01340893829678a5651f89ed428440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927950"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>\_WPD-BEFEHL \_ MTP \_ EXT READ \_ \_ DATA-Befehl

Der **BEFEHL WPD \_ COMMAND \_ MTP EXT READ \_ \_ \_ DATA** ruft Daten vom Gerät ab, nachdem der **BEFEHL WPD COMMAND \_ \_ MTP EXT EXECUTE COMMAND \_ WITH DATA TO \_ \_ \_ \_ \_ \_ READ** ausgeführt wurde.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ CATEGORY \_ MTP \_ EXT \_ VENDOR \_ OPERATIONS**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                                   | VarType             | Beschreibung                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER \_ \_ CONTEXT**              | VT \_ LPWSTR          | Erforderlich. Identifiziert den Kontext, der durch den vorherigen Aufruf des Geräts zurückgegeben wurde. |
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER NUM BYTES TO \_ \_ \_ \_ \_ READ** | VT \_ UI4             | Erforderlich. Gibt die Anzahl der zu lesenden Bytes an.                                       |
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER \_ \_ DATA**                 | VT \_ VECTOR \| VT \_ UI1 | Erforderlich. Identifiziert den Puffer, in den die Gerätedaten kopiert werden.                  |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                  | VarType             | Beschreibung                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER NUM BYTES \_ \_ \_ \_ READ** | VT \_ UI4             | Erforderlich. Gibt die Anzahl der vom Gerät empfangenen Bytes an. |
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER \_ \_ DATA**             | VT \_ VECTOR \| VT \_ UI1 | Erforderlich. Der Puffer, der die Gerätedaten enthält.               |



 

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

 

 




