---
description: Die LINEDEVCAPFLAGS-Bitflagkonstanten sind eine Sammlung boolescher Konstanten, die verschiedene Funktionen \_ des Liniengeräts beschreiben.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: LINEDEVCAPFLAGS_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d54acf1855bc09d9b2160e1ae681b25ff1de8ce310049fd4aabf4af6f8f2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761717"
---
# <a name="linedevcapflags_-constants"></a>LINEDEVCAPFLAGS-Konstanten \_

Die **\_ LINEDEVCAPFLAGS-Bitflagkonstanten** sind eine Sammlung boolescher Konstanten, die verschiedene Funktionen des Liniengeräts beschreiben.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



Gibt an, ob Aufrufhubs in dieser Zeile unterstützt werden. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Gibt an, ob die Anrufhubnachverfolgung in dieser Zeile unterstützt wird. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



Gibt an, was geschieht, wenn eine geöffnete Zeile geschlossen wird, während die Anwendung aktiv in der Zeile aufruft. True **gibt an,** dass der Dienstanbieter alle aktiven Aufrufe in der Zeile löscht (löscht), wenn die letzte Anwendung, die die Zeile geöffnet hat, sie mit [**lineClose schließt.**](/windows/desktop/api/Tapi/nf-tapi-lineclose) False **gibt** an, dass der Dienstanbieter in solchen Fällen keine aktiven Aufrufe verwirf. Stattdessen bleiben die Aufrufe aktiv und werden von externen Geräten kontrolliert. Ein Dienstanbieter legt dieses Bit in der Regel auf **FALSE** fest, wenn es ein anderes Gerät gibt, das den Anruf aktiv halten kann, z. B. wenn eine analoge Leitung den Computer und das Telefon in einer Party-Line-Konfiguration direkt mit ihnen verbinden, hält das Offhooktelefon den Anruf automatisch aktiv, auch wenn der Computer ausgeschaltet ist.

Anwendungen sollten dieses Flag überprüfen, um zu bestimmen, ob der Benutzer (mit einem Dialogfeld OK/Abbrechen) ge warnen soll, dass aktive Aufrufe verloren gehen.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



Gibt an, ob Aufrufe an verschiedenen Adressen in dieser Zeile in einer Konferenz verwendet werden können.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Diese Flags geben an, ob der modifizierbare Zeichenfolgenmodifizierer "$", "@" oder "W" für ein bestimmtes Zeilengerät unterstützt wird. Er ist **TRUE,** wenn der Modifizierer unterstützt wird. andernfalls **FALSE**. Das "?" (Auffordern des Benutzers zum Fortsetzen des Wählens) wird von einem Liniengerät nie unterstützt. Mit diesen Flags kann eine Anwendung im Vorfeld bestimmen, welche Modifizierer zur Generierung eines LINEERR führen würden. Die Anwendung kann vor dem Scannen von Wählzeichenfolgen für nicht unterstützte Zeichen wählen oder die "rohe" Zeichenfolge von [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) direkt an den Anbieter als Teil von Funktionen wie [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) oder [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) übergeben und die Funktion einen Fehler generieren lassen, um ihm mitteilen zu können, welcher nicht unterstützte Modifizierer zuerst in der Zeichenfolge auftritt.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**
</dt> <dd> <dl> <dt>



Gibt an, ob Kompatibilitätsinformationselemente auf hoher Ebene in dieser Zeile unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**
</dt> <dd> <dl> <dt>



Gibt an, ob Kompatibilitätsinformationselemente auf niedriger Ebene in dieser Zeile unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



Gibt an, ob Mediensteuerungsvorgänge für Aufrufe in dieser Zeile verfügbar sind.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**
</dt> <dd> <dl> <dt>



Gibt an, ob der Zeile ein Media Service Provider (MSP) zugeordnet ist. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



Gibt an, ob [**lineMakeCall,**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) [**lineDial,**](/windows/desktop/api/Tapi/nf-tapi-linedial) [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)oder [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) mehrere Adressen gleichzeitig behandeln können (wie beim umgekehrten Multiplexing).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**
</dt> <dd> <dl> <dt>



Gibt [an, ob anbieterspezifische Schnittstellen](./provider-specific-interfaces.md) implementiert wurden. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

