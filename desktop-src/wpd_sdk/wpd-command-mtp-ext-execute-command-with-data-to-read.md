---
description: Mit dem WPD- \_ Befehl \_ MTP \_ Ext \_ Execute \_ Command \_ with \_ Data \_ to \_ Read Command wird ein MTP-Befehls Block gesendet, dem eine Daten Phase folgt. (Die Daten werden vom Gerät an den Host gesendet.)
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ Befehl (wpdmtpextensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372627"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>WPD- \_ Befehl \_ MTP \_ ext Befehl \_ zum Ausführen \_ von Befehlen \_ mit \_ Daten \_ zum \_ Lesen

**Mit dem WPD- \_ Befehl \_ MTP \_ Ext \_ Execute \_ Command \_ with \_ Data \_ to \_ Read** Command wird ein MTP-Befehls Block gesendet, dem eine Daten Phase folgt. (Die Daten werden vom Gerät an den Host gesendet.)

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



| Ergebnis                                                       | VarType    | BESCHREIBUNG                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ \_ gesamte \_ Daten \_ Größe übertragen**     | VT \_ UI8    | Erforderlich. Gibt die Gesamtgröße der Daten (in Bytes) zurück, ausgenommen der vom Gerät gesendeten Verwaltungsaufwand. Wenn das Gerät eine unbekannte DataSize (0xFFFFFFFF) meldet, sollte der Treiber die " **lesedata** " wiederholt aufzurufen, bis ein kurzer Block empfangen wird. |
| **WPD- \_ Eigenschaft \_ MTP \_ Ext \_ optimale \_ Übertragungs \_ Puffer \_ Größe** | VT \_ UI4    | Dies ist optional. Gibt die optimale Größe des Übertragungs Puffers zurück.                                                                                                                                                                          |
| **WPD- \_ Eigenschaften- \_ MTP-Ext- \_ \_ Übertragungs \_ Kontext**               | VT \_ LPWSTR | Erforderlich. Gibt den Kontext Bezeichner für nachfolgende Datenübertragungen an.                                                                                                                                                           |



 

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

 

 




