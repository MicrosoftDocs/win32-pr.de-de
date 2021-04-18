---
description: Mit dem Befehl "MTP ext-Daten lesen" des WPD- \_ Befehls werden \_ \_ \_ \_ Daten vom Gerät abgerufen, nachdem der Befehl " \_ MTP ext ausführen" des Befehls "WPD-Befehl mit dem Befehl \_ \_ \_ \_ \_ \_ \_ zum Lesen von Daten \_
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358661"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>WPD- \_ Befehl \_ MTP \_ ext-Befehl zum Lesen von \_ \_ Daten

Mit dem Befehl " **\_ \_ MTP \_ Ext \_ \_** -Daten lesen" des WPD-Befehls werden Daten vom Gerät abgerufen, nachdem der Befehl " **\_ \_ MTP \_ Ext \_ Ausführen \_ \_ \_ \_ \_** " des Befehls "WPD-Befehl mit dem Befehl zum Lesen von Daten

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                                   | VarType             | BESCHREIBUNG                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**              | VT \_ LPWSTR          | Erforderlich. Gibt den Kontext an, der durch den vorherigen-Anrufe des Geräts zurückgegeben wurde. |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ überträgt \_ NUM \_ Bytes \_ in den \_ Lesevorgang** | VT \_ UI4             | Erforderlich. Gibt die Anzahl der zu lesenden Bytes an.                                       |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragungs \_ Daten**                 | VT \_ Vector \| VT \_ UI1 | Erforderlich. Identifiziert den Puffer, in den die Gerätedaten kopiert werden.                  |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                  | VarType             | BESCHREIBUNG                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragung \_ NUM \_ Bytes \_ gelesen** | VT \_ UI4             | Erforderlich. Gibt die Anzahl von Bytes an, die vom Gerät empfangen werden. |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragungs \_ Daten**             | VT \_ Vector \| VT \_ UI1 | Erforderlich. Der Puffer, der die Gerätedaten enthält.               |



 

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

 

 




