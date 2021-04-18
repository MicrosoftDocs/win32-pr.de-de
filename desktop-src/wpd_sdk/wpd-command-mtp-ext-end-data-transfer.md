---
description: Mit dem Befehl "MTP ext" der WPD \_ -Befehl " \_ \_ \_ End \_ Data Transfer" wird \_ eine Datenübertragung und eine Lese Antwort vom Gerät abgeschlossen.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354738"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>WPD- \_ Befehl \_ MTP ext Befehl zum Beenden der \_ \_ \_ Daten \_ Übertragung

Mit dem Befehl " **MTP ext" der WPD- \_ Befehl " \_ \_ \_ End \_ Data \_ Transfer** " wird eine Datenübertragung und eine Lese Antwort vom Gerät abgeschlossen. Die Übertragung wird entweder durch den [**WPD- \_ Befehl \_ MTP \_ Ext \_ Execute \_ Command \_ mit \_ Daten \_ zum \_ Lesen**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) -Befehl oder den [**WPD- \_ Befehl \_ MTP \_ Ext \_ Execute Command mit dem Befehl \_ \_ \_ \_ zum \_ Schreiben von Daten**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) initiiert.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                      | VarType    | BESCHREIBUNG                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext** | VT \_ LPWSTR | Erforderlich. Identifiziert den Kontext, der von einem früheren Methoden Aufrufwert zurückgegeben wird. |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                        | VarType | BESCHREIBUNG                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Antwort \_ Code**   | VT \_ UI4 | Erforderlich. der Antwort Code für den Vorgangs Code des Herstellers.                                                                                |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Antwort \_ Parameter** | VT \_ UI4 | Dies ist optional. Eine **iportabledevicepropvariantcollection** -Auflistung, die alle Antwort Parameter identifiziert. Diese Auflistung kann leer sein. |



 

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

 

