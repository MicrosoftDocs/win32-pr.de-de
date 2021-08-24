---
description: Der BEFEHL WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO WRITE sendet \_ einen \_ \_ \_ \_ \_ MTP-Befehlsblock, auf den eine Datenphase folgt. Die Daten werden vom Host an das Gerät gesendet.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE-Befehl (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae0e50ad2fad9967252d9a21c1e864d056338a3e3a2b82f4c29d951a722953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806310"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>WPD \_ COMMAND \_ MTP \_ EXT \_ EXECUTE \_ COMMAND \_ WITH \_ DATA \_ TO \_ WRITE Command

Der **BEFEHL WPD \_ COMMAND \_ MTP EXT EXECUTE COMMAND \_ WITH DATA TO \_ \_ \_ \_ \_ \_ WRITE** sendet einen MTP-Befehlsblock, auf den eine Datenphase folgt. Die Daten werden vom Host an das Gerät gesendet.

## <a name="command-category"></a>Befehlskategorie

**MTP \_ \_ \_ \_ EXT-ANBIETERVORGÄNGE \_ DER WPD-KATEGORIE**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                                | VarType | Beschreibung                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ – \_ MTP-EXT-VORGANGSCODE \_ \_**             | VT \_ UI4 | Erforderlich. Identifiziert einen vom Anbieter erweiterten MTP-Vorgangscode.                                                                              |
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT OPERATION \_ \_ PARAMS**           | VT \_ UI4 | Erforderlich. Eine **IPortableDevicePropVariantCollection-Auflistung,** die die erforderlichen Parameter für den Herstellervorgangscode identifiziert. |
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER TOTAL DATA \_ \_ \_ \_ SIZE** | VT \_ UI8 | Required.Gibt die Gesamtdatengröße in Bytes an, ohne jeglichen Mehraufwand, der an das Gerät gesendet werden soll.                                         |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                       | VarType    | Beschreibung                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT OPTIMALE \_ \_ \_ \_ ÜBERTRAGUNGSPUFFERGRÖßE** | VT \_ UI4    | Erforderlich. Gibt die optimale Größe des Übertragungspuffers an.                       |
| **\_WPD-EIGENSCHAFT \_ MTP \_ EXT TRANSFER \_ \_ CONTEXT**               | VT \_ LPWSTR | Optional. Ein Kontextbezeichner, den der Treiber für nachfolgende Datenübertragungen verwendet. |



 

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

 

 




