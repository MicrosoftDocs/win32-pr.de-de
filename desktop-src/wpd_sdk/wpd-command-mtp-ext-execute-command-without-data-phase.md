---
description: Der WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command \_ ohne \_ Daten \_ Phasen Befehl sendet einen MTP-Befehls Block. Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362023"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>WPD- \_ Befehl \_ MTP ext Befehl zum Ausführen des Befehls \_ \_ \_ \_ ohne \_ Daten \_ Phase

Der **WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command \_ ohne \_ Daten \_ Phasen** Befehl sendet einen MTP-Befehls Block. Diesem Befehl ist keine nachfolgende Daten Phase zugeordnet.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                      | VarType | BESCHREIBUNG                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Vorgangs \_ Code**   | VT \_ UI4 | Erforderlich. Identifiziert einen vom Hersteller erweiterten MTP-Vorgangs Code.                                                                    |
| **WPD- \_ Eigenschaft \_ MTP-Ext- \_ \_ Vorgang \_ , Parameter** | VT \_ UI4 | Erforderlich. Ein **iportabledevicepropvariantcollection**-Element, das die erforderlichen Parameter für den Hersteller Vorgangs Code angibt. |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                        | VarType | BESCHREIBUNG                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Antwort \_ Code**   | VT \_ UI4 | Erforderlich. Der Antwort Code für den Vorgangs Code des Herstellers.                                                                      |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Antwort \_ Parameter** | VT \_ UI4 | Dies ist optional. Eine **iportabledevicepropvariantcollection** , die alle Antwort Parameter identifiziert. Diese Auflistung ist möglicherweise leer. |



 

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

 

 




