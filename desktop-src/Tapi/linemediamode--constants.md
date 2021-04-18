---
description: Die linemediamode- \_ Konstanten beschreiben Medientypen (oder Modi) einer Kommunikationssitzung oder eines Aufrufes.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: LINEMEDIAMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354706"
---
# <a name="linemediamode_-constants"></a>Linemediamode- \_ Konstanten

Die **linemediamode \_** -Konstanten beschreiben Medientypen (oder Modi) einer Kommunikationssitzung oder eines Aufrufes.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**linemediamode \_ automatedvoice**
</dt> <dd> <dl> <dt>



Beim Anruf wurde Voice Energy erkannt, und die Stimme wird lokal von einer automatisierten Anwendung wie z. b. mit einer antwortenden Computeranwendung behandelt. Wenn ein Dienstanbieter bei einem eingehenden Anruf nicht zwischen interaktiver und automatisierter Stimme unterscheiden kann, wird der Anruf als interaktive Stimme gemeldet.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**linemediamode \_ datamoder**
</dt> <dd> <dl> <dt>



Eine Datenmodem Sitzung für den-Befehl. Aktuelle Modem Protokolle erfordern, dass die aufgerufene Station den Handshake initiiert. Für einen eingehenden Datenmodem Anrufe kann die Anwendung normalerweise keine positive Erkennung durchführen. Wie der Dienstanbieter diese Bestimmung trifft, ist seine Wahl. So kann z. b. ein Ruhe Zeitraum nur nach dem Beantworten eines eingehenden Aufrufes als Heuristik verwendet werden, um zu entscheiden, dass dies ein Datenmodem Anruf sein könnte.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**linemediamode \_ ADSI**
</dt> <dd> <dl> <dt>



Eine ADSI-Sitzung (Analog Display Services Interface) für den-Befehl. ADSI erweitert Sprachanrufe mit alphanumerischen Informationen, die auf das Telefon heruntergeladen wurden, und verwendet weiche Schaltflächen auf dem Telefon.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**linemediamode \_ digitaldata**
</dt> <dd> <dl> <dt>



Ein digitaler Datenstrom des nicht angegebenen Formats.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**Linemediamode \_ G3FAX**
</dt> <dd> <dl> <dt>



Ein Fax der Gruppe 3 wird über den-Befehl gesendet oder empfangen.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**Linemediamode \_ G4FAX**
</dt> <dd> <dl> <dt>



Ein Fax der Gruppe 4 wird über den-Befehl gesendet oder empfangen.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**linemediamode \_ interactivevoice**
</dt> <dd> <dl> <dt>



Beim Anruf wurde Voice Energy erkannt, und der Anruf wird als interaktiver Sprachanruf mit Menschen an beiden Enden behandelt.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**"linemediamode" \_ gemischt**
</dt> <dd> <dl> <dt>



Eine gemischte Sitzung beim-Rückruf. Gemischt ist einer der ISDN-telematischen Dienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**linemediamode- \_ TDD**
</dt> <dd> <dl> <dt>



Eine TDD-Sitzung (Telefoniegeräte für gehörlos) für den-Befehl.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**linemediamode- \_ Teletex**
</dt> <dd> <dl> <dt>



Eine Teletex-Sitzung des Aufrufs. Der Teletex ist einer der telematischen Dienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**linemediamode \_ Telex**
</dt> <dd> <dl> <dt>



Eine Telex-Sitzung für den-Befehl. Telex ist einer der telematischen Dienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**linemediamode- \_ Video**
</dt> <dd> <dl> <dt>



Der Medientyp des Aufrufes ist Video. (TAPI-Versionen 2,1 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**linemediamode- \_ Videotex**
</dt> <dd> <dl> <dt>



Eine Videotex-Sitzung des Aufrufs. Videotex ist eine der telematischen Dienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**linemediamode \_ VoiceView**
</dt> <dd> <dl> <dt>



Der Medientyp des Aufrufes ist VoiceView. (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**linemediamode \_ unbekannt**
</dt> <dd> <dl> <dt>



Ein Mediendaten Strom ist vorhanden, aber sein Modus ist zurzeit nicht bekannt und kann später bekannt werden. Dies entspricht einem-Befehl mit einem nicht klassifizierten Medientyp. In typischen analogen Telefonieumgebungen ist der Medientyp eines eingehenden Anrufes möglicherweise unbekannt, bis der-Befehl beantwortet wurde und der Mediendaten Strom gefiltert wurde, um eine Entscheidung zu treffen.

Wenn das unbekannte Medien Modus-Flag festgelegt ist, können auch andere medienflags festgelegt werden. Dies wird verwendet, um anzugeben, dass das Medium unbekannt ist, aber wahrscheinlich einem der anderen ausgewählten Medientypen entspricht.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle 32 Bits sind reserviert.

Beachten Sie, dass bearermodus und Medientyp unterschiedliche Vorstellungen sind. Der bearermodus eines Aufrufes ist ein Hinweis auf die Qualität der Telefonverbindung, die in erster Linie vom Netzwerk bereitgestellt wird. Der Medientyp eines Aufrufes ist ein Hinweis auf den Typ des Informationsdaten Stroms, der über diesen Befehl ausgetauscht wird. Gruppe 3: Fax-oder Datenmodem sind Medientypen, die einen Anruf mit einem 3,1 kHz-sprach Träger Modus verwenden.

Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diesen linemediamode-Wert nicht zu verwenden, wenn er von \_ der ausgehandelten Version nicht unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




