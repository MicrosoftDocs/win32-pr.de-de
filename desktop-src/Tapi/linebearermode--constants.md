---
description: Die \_ LINEBEARERMODE-Bitflagkonst constants beschreiben verschiedene Bearermodi eines Aufrufs.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: LINEBEARERMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bb03664b6e904cbce7e376eb111675430ea86b8e6880211d76d5b364467097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761764"
---
# <a name="linebearermode_-constants"></a>\_LINEBEARERMODE-Konstanten

Die **\_ LINEBEARERMODE-Bitflagkonst** constants beschreiben verschiedene Bearermodi eines Aufrufs. Wenn eine Anwendung einen Aufruf macht, kann sie einen bestimmten Bearermodus anfordern. Diese Modi werden verwendet, um eine bestimmte Dienstqualität für die angeforderte Verbindung aus dem zugrunde liegenden Telefonnetzwerk auszuwählen. Bearermodi, die in einer bestimmten Zeile verfügbar sind, sind eine Gerätefunktion der Linie.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



Die alternative Übertragung von Sprache oder uneingeschränkten Daten bei demselben Aufruf (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**LINEBEARERMODE-DATEN \_**
</dt> <dd> <dl> <dt>



Die uneingeschränkte Datenübertragung beim Aufruf. Die Datenrate wird separat angegeben.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ MULTIUSE**
</dt> <dd> <dl> <dt>



Der durch ISDN definierte Mehrfachnutzungsmodus.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



Dies entspricht einer nicht aufruf-zugeordneten Signalverbindung zwischen der Anwendung und dem Dienstanbieter oder Switch (von TAPI als Medienstream behandelt).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE-PASSTHROUGH \_**
</dt> <dd> <dl> <dt>



Wenn ein Aufruf in LINEBEARERMODE PASSTHROUGH aktiv ist, gewährt der Dienstanbieter direkten Zugriff auf die angeschlossene Hardware zur Steuerung \_ durch die Anwendung. Dieser Modus wird hauptsächlich von Anwendungen verwendet, die eine temporäre [](/windows/desktop/DevIO/communications-functions)direkte Kontrolle über asynchrone Modems möchten, auf die über die Kommunikationsfunktionen zugegriffen wird, um spezielle Features zu konfigurieren oder zu verwenden, die nicht anderweitig vom Dienstanbieter unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



Bearerdienst für digitale Daten, bei denen nur die niedrigen sieben Bits jedes Oktetts Benutzerdaten enthalten können (z. B. für den Dienst Switched 56kbit/s).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**LINEBEARERMODE \_ SPEECH**
</dt> <dd> <dl> <dt>



Dies entspricht der G.711-Sprachübertragung beim Aufruf. Das Netzwerk kann Verarbeitungstechniken wie analoge Übertragung, Echoabbruch und Komprimierung/Dekomprimierung verwenden. Die Bitintegrität ist nicht gewährleistet. Spracherkennung ist nicht für die Unterstützung von Fax- und Modemmedien vorgesehen.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ VOICE**
</dt> <dd> <dl> <dt>



Dies ist ein regulärer analoger Bearerdienst mit 3,1 kHz. Die Bitintegrität ist nicht gewährleistet. Voice kann Fax- und Modemmedientypen unterstützen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die hochwertigen 16 Bits können für gerätespezifische Erweiterungen zugewiesen werden. Die niedrigen 16 Bits sind reserviert.

Beachten Sie, dass Bearermodus und Medientyp unterschiedliche Begriffe sind. Der Bearermodus eines Anrufs ist ein Hinweis auf die Qualität der Telefonverbindung, die in erster Linie vom Netzwerk bereitgestellt wird. Der Medientyp eines Aufrufs ist ein Hinweis auf den Typ des Informationsstreams, der über diesen Aufruf ausgetauscht wird. Fax oder Datenmodem der Gruppe 3 sind Medientypen, die einen Anruf mit einem 3,1-kHz-Stimm bearermodus verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

