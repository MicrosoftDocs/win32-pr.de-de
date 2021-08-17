---
description: Die \_ LINEMEDIAMODE-Konstanten beschreiben Medientypen (oder Modi) einer Kommunikationssitzung oder eines Kommunikationsaufrufs.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: LINEMEDIAMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c11e40a81fffc967afd534ce6de591b524d835cbe97a919903bd97b1eeb4daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140013"
---
# <a name="linemediamode_-constants"></a>\_LINEMEDIAMODE-Konstanten

Die **\_ LINEMEDIAMODE-Konstanten** beschreiben Medientypen (oder Modi) einer Kommunikationssitzung oder eines Kommunikationsaufrufs.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



Sprachenergie wurde beim Anruf erkannt, und die Stimme wird lokal von einer automatisierten Anwendung wie einer Antwortcomputeranwendung verarbeitet. Wenn ein Dienstanbieter bei einem eingehenden Anruf nicht zwischen interaktiver und automatisierter Stimme unterscheiden kann, wird der Anruf als interaktive Stimme berichtet.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**
</dt> <dd> <dl> <dt>



Eine Datenmodemsitzung für den Aufruf. Aktuelle Modemprotokolle erfordern die aufgerufene Station, um den Handshake zu initiieren. Bei einem eingehenden Datenmodemaufruf kann die Anwendung in der Regel keine positive Erkennung machen. Wie der Dienstanbieter diese Entscheidung trifft, ist seine Wahl. Beispielsweise kann eine Stille kurz nach der Beantwortung eines eingehenden Anrufs als Heuristik verwendet werden, um zu entscheiden, dass dies ein Datenmodemaufruf sein könnte.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Eine ADSI-Sitzung (Analog Display Services Interface) für den Aufruf. ADSI erweitert Sprachanrufe um alphanumerische Informationen, die auf das Telefon heruntergeladen werden, und die Verwendung von soft buttons auf dem Telefon.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**
</dt> <dd> <dl> <dt>



Ein digitaler Datenstrom im nicht angegebenen Format.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**
</dt> <dd> <dl> <dt>



Ein Fax der Gruppe 3 wird über den Anruf gesendet oder empfangen.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**
</dt> <dd> <dl> <dt>



Ein Fax der Gruppe 4 wird über den Anruf gesendet oder empfangen.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**
</dt> <dd> <dl> <dt>



Sprachenergie wurde beim Anruf erkannt, und der Anruf wird als interaktiver Sprachanruf mit Menschen an beiden Enden verarbeitet.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ MIXED**
</dt> <dd> <dl> <dt>



Eine gemischte Sitzung für den Aufruf. Mixed ist einer der ISDN-Telematikdienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



Eine TDD-Sitzung (Telefoniegeräte für den Gehörlosen) für den Anruf.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**
</dt> <dd> <dl> <dt>



Eine Teletexsitzung für den Aufruf. Teletex ist einer der telematischen Dienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE \_ TELEX**
</dt> <dd> <dl> <dt>



Eine Telexsitzung für den Anruf. Telex ist einer der telematischen Dienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE-VIDEO \_**
</dt> <dd> <dl> <dt>



Der Medientyp des Aufrufs ist Video. (TAPI-Versionen 2.1 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



Eine Videotexsitzung für den Aufruf. Videotex ist einer der telematischen Dienste.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**
</dt> <dd> <dl> <dt>



Der Medientyp des Anrufs ist VoiceView. (TAPI-Versionen 1.4 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Ein Medienstream ist vorhanden, aber sein Modus ist derzeit nicht bekannt und kann später bekannt werden. Dies entspricht einem Aufruf mit einem nicht klassifizierten Medientyp. In typischen analogen Telefonieumgebungen ist der Medientyp eines eingehenden Anrufs möglicherweise unbekannt, bis der Anruf beantwortet und der Medienstream gefiltert wurde, um eine Bestimmung zu treffen.

Wenn das Unbekannte Medienmodusflag festgelegt ist, können auch andere Medienflags festgelegt werden. Dies wird verwendet, um zu signalisieren, dass das Medium unbekannt ist, es sich aber wahrscheinlich um einen der anderen ausgewählten Medientypen handelt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Alle 32 Bits sind reserviert.

Beachten Sie, dass Bearermodus und Medientyp unterschiedliche Begriffe sind. Der Bearermodus eines Anrufs ist ein Hinweis auf die Qualität der Telefonverbindung, die in erster Linie vom Netzwerk bereitgestellt wird. Der Medientyp eines Aufrufs ist ein Hinweis auf den Typ des Informationsstreams, der über diesen Aufruf ausgetauscht wird. Fax oder Datenmodem der Gruppe 3 sind Medientypen, die einen Anruf mit einem 3,1-kHz-Stimm bearermodus verwenden.

Aus Gründen der Abwärtskompatibilität ist der Dienstanbieter dafür verantwortlich, die ausgehandelte API-Version in der Zeile zu untersuchen und diesen LINEMEDIAMODE-Wert nicht zu verwenden, wenn er für die ausgehandelte Version nicht \_ unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




