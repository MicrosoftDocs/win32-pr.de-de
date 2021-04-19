---
description: Der Befehl " \_ MTP ext-Schreib Daten schreiben" des WPD-Befehls \_ \_ \_ \_ sendet Daten an das Gerät, nachdem der Befehl " \_ MTP ext ausführen" des Befehls " \_ MTP \_ ext ausführen" \_ mit dem \_ Befehl " \_ \_ Daten \_ \_
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: WPD_COMMAND_MTP_EXT_WRITE_DATA Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368655"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a>WPD- \_ Befehl \_ MTP \_ ext-Befehl zum Schreiben von \_ \_ Daten

Der Befehl " **\_ \_ MTP \_ Ext- \_ Schreib \_ Daten schreiben" des WPD-Befehls** sendet Daten an das Gerät, nachdem der Befehl " **MTP ext ausführen" des Befehls " \_ \_ MTP \_ ext ausführen" \_ \_ \_ mit \_ \_ \_** dem Befehl "Daten

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ MTP \_ Ext- \_ Anbieter \_ Vorgänge**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                                    | VarType             | BESCHREIBUNG                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**               | VT \_ LPWSTR          | Erforderlich. Gibt den Kontext an, der durch den vorherigen-Anrufe des Geräts zurückgegeben wurde. |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ überträgt \_ NUM \_ Bytes \_ zum \_ schreiben** | VT \_ UI4             | Erforderlich. Gibt die Anzahl der zu schreibenden Bytes an.                                      |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragungs \_ Daten**                  | VT \_ Vector \| VT \_ UI1 | Erforderlich. Identifiziert den Puffer, in den die Gerätedaten kopiert werden.                  |



 

## <a name="return-value"></a>Rückgabewert

Der Treiber gibt die folgenden Ergebnisse zurück.



| Ergebnis                                                     | VarType | BESCHREIBUNG                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Übertragung \_ NUM \_ Bytes \_ geschrieben** | VT \_ UI4 | Erforderlich. Gibt die Anzahl der Bytes an, die an das Gerät gesendet werden. |



 

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

 

 




