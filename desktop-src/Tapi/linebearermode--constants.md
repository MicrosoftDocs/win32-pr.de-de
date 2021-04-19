---
description: Die \_ Bit-Flag-Konstanten linebearermode beschreiben verschiedene bearermodi eines Aufrufes.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: LINEBEARERMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367110"
---
# <a name="linebearermode_-constants"></a>Linebearermode- \_ Konstanten

Die Bit-Flag-Konstanten **linebearermode \_ beschreiben verschiedene bearermodi** eines Aufrufes. Wenn eine Anwendung einen-Befehl aufruft, kann Sie einen bestimmten bearermodus anfordern. Diese Modi werden verwendet, um eine bestimmte Dienst Qualität für die angeforderte Verbindung vom zugrunde liegenden Telefon Netzwerk auszuwählen. Bearermodi, die in einer bestimmten Zeile verfügbar sind, sind eine Geräte Funktion der Zeile.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**linebearermode- \_ altredner Daten**
</dt> <dd> <dl> <dt>



Die Alternative Übertragung von Sprache oder uneingeschränkten Daten beim gleichen-Rückruf (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**linebearermode- \_ Daten**
</dt> <dd> <dl> <dt>



Die uneingeschränkte Datenübertragung beim-Befehl. Die Datenrate wird separat angegeben.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**linebearermode- \_ Multiuse**
</dt> <dd> <dl> <dt>



Der von ISDN definierte Multiuse-Modus.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**linebearermode- \_ noncallsignsignalisierung**
</dt> <dd> <dl> <dt>



Dies entspricht einer nicht dem Rückruf zugeordneten Signalverbindung von der Anwendung zum Dienstanbieter oder Switch (wird von TAPI als Medienstrom behandelt).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**linebearermode- \_ Passthrough**
</dt> <dd> <dl> <dt>



Wenn ein-Befehl in der Passthrough-Anleitung von linebearermode aktiv ist \_ , ermöglicht der Dienstanbieter den direkten Zugriff auf die angefügte Hardware, die von der Anwendung gesteuert werden kann. Dieser Modus wird hauptsächlich von Anwendungen verwendet, die eine temporäre direkte Steuerung von asynchronen Modems aufrufen, auf die über die [Kommunikationsfunktionen](/windows/desktop/DevIO/communications-functions)zugegriffen wird, um spezielle Features zu konfigurieren oder zu verwenden, die andernfalls vom Dienstanbieter nicht unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**linebearermode \_ restricteddata**
</dt> <dd> <dl> <dt>



Bearerdienst für digitale Daten, bei denen nur die nieder wertigen sieben Bits jedes Oktetts Benutzerdaten enthalten können (z. b. für den Wechsel von 56kBit/s-Dienst).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**linebearermode- \_ Sprache**
</dt> <dd> <dl> <dt>



Dies entspricht der "G. 711"-Sprachübertragung für den-Befehl. Das Netzwerk kann Verarbeitungstechniken wie z. b. eine analoge Übertragung, einen Echo Abbruch und Komprimierung/Dekomprimierung verwenden. Die bitintegrität ist nicht sicher. Die Sprache ist nicht für die Unterstützung von Fax-und Modem Medientypen vorgesehen.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**linebearermode- \_ Stimme**
</dt> <dd> <dl> <dt>



Dies ist ein regulärer 3,1 kHz-bearerdienstanbieter-bearerdienst. Die bitintegrität ist nicht sicher. Voice kann Fax-und Modem Medientypen unterstützen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die höherwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die nieder wertigen 16 Bits sind reserviert.

Beachten Sie, dass bearermodus und Medientyp unterschiedliche Vorstellungen sind. Der bearermodus eines Aufrufes ist ein Hinweis auf die Qualität der Telefonverbindung, die in erster Linie vom Netzwerk bereitgestellt wird. Der Medientyp eines Aufrufes ist ein Hinweis auf den Typ des Informationsdaten Stroms, der über diesen Befehl ausgetauscht wird. Gruppe 3: Fax-oder Datenmodem sind Medientypen, die einen Anruf mit einem 3,1 kHz-sprach Träger Modus verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

