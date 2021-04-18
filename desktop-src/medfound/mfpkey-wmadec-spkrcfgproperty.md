---
description: Gibt die Sprecher Konfiguration auf dem Client Computer an.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: MFPKEY_WMADEC_SPKRCFG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528568"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>Mfpkey \_ wmadec \_ spkrcfg (Eigenschaft)

Gibt die Sprecher Konfiguration auf dem Client Computer an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmacspeakerconfig

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

Es wird keine bestimmte Sprecher Konfiguration angenommen.

## <a name="remarks"></a>Bemerkungen

Sie sollten diesen Wert auf eine der Konstanten oder Werte in der folgenden Tabelle festlegen. Die Konstanten sind in Microsoft DirectSound definiert und werden hier zur Verfügung gestellt. Um diese Konstanten Namen für den Compiler aufzulösen, müssen Sie DSound. h einschließen.



| Konstante             | Wert      | BESCHREIBUNG                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| dsspeaker- \_ directout | 0x00000000 | Die Audiodaten werden direkt durchlaufen, ohne für Referenten konfiguriert zu werden. |
| dsspeaker- \_ Telefon | 0x00000001 | Der Client Computer ist mit einem Kopfhörer ausgestattet.                             |
| dsspeaker \_ Mono      | 0x00000002 | Der Client Computer ist mit einem monoaural-Redner ausgestattet.                    |
| dsspeaker \_ Quad      | 0x00000003 | Der Client Computer ist mit quadratischen sprechenden Referenten ausgestattet.                  |
| dsspeaker- \_ Stereo    | 0x00000004 | Der Client Computer ist mit Stereo Referenten ausgestattet.                        |
| Umschließen von dsspeaker \_  | 0x00000005 | Der Client Computer ist mit vier-Kanal-umschließenden sprechenden ausgestattet.   |
| Dsspeaker \_ 5point1   | 0x00000006 | Der Client Computer ist mit fünf Referenten und einem Subwoofer ausgestattet.          |
| Dsspeaker \_ 7point1   | 0x00000007 | Der Client Computer ist mit sieben Referenten und einem Subwoofer ausgestattet.         |



 

Der für diese Eigenschaft festgelegte Wert bestimmt die Ausgabeformate, die vom Codec für Multichannel-Audiodaten aufgelistet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




