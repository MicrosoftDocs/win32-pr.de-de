---
description: Der WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command \_ mit dem \_ \_ Befehl Daten zum \_ Schreiben sendet einen MTP-Befehls Block, dem eine Daten Phase folgt. Die Daten werden vom Host an das Gerät gesendet.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371436"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>WPD- \_ Befehl \_ MTP \_ ext Execute- \_ \_ Befehl \_ mit \_ Daten \_ zum Schreiben des \_ Befehls

Der **WPD-Befehl \_ \_ MTP \_ Ext \_ Execute \_ Command mit dem Befehl \_ \_ Daten \_ zum \_ Schreiben** sendet einen MTP-Befehls Block, dem eine Daten Phase folgt. Die Daten werden vom Host an das Gerät gesendet.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                                | VarType | BESCHREIBUNG                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Vorgangs \_ Code**             | VT \_ UI4 | Erforderlich. Identifiziert einen vom Hersteller erweiterten MTP-Vorgangs Code.                                                                              |
| **WPD- \_ Eigenschaft \_ MTP-Ext- \_ \_ Vorgang \_ , Parameter**           | VT \_ UI4 | Erforderlich. Eine **iportabledevicepropvariantcollection** -Auflistung, die die erforderlichen Parameter für den Vorgangs Code des Herstellers identifiziert. |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ \_ gesamte \_ Daten \_ Größe übertragen** | VT \_ UI8 | Erforderlich. gibt die Gesamtgröße der Daten in Bytes an, die an das Gerät gesendet werden.                                         |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                       | VarType    | BESCHREIBUNG                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ optimale \_ Übertragungs \_ Puffer \_ Größe** | VT \_ UI4    | Erforderlich. Gibt die optimale Größe des Übertragungs Puffers an.                       |
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**               | VT \_ LPWSTR | Dies ist optional. Ein Kontext Bezeichner, der vom Treiber für nachfolgende Datenübertragungen verwendet wird. |



 

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

 

 




