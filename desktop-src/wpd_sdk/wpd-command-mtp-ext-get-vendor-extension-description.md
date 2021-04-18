---
description: Der Befehl WPD \_ \_ -Befehl MTP \_ Ext \_ get \_ Vendor \_ Extension \_ Description Ruft die Beschreibungs Zeichenfolge der Hersteller Erweiterung ab. Diese Zeichenfolge wird durch ein "Debug"-DataSet definiert.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365695"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Vendor \_ Extension Description- \_ Befehl

Der Befehl **WPD- \_ Befehl \_ MTP \_ Ext \_ get \_ Vendor \_ Extension \_ Description** Ruft die Beschreibungs Zeichenfolge der Hersteller Erweiterung ab. Diese **Zeichenfolge wird durch ein "** Debug"-DataSet definiert.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**

## <a name="parameters"></a>Parameter

Dieser Befehl weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                      | VarType    | BESCHREIBUNG                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ Hersteller \_ Erweiterung \_ Beschreibung** | VT \_ LPWSTR | Erforderlich. Gibt die Beschreibungs Zeichenfolge der Hersteller Erweiterung an. |



 

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

 

 




