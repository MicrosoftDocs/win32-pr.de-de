---
description: Die \_ Bits-Flag-Konstanten von linedevcapflags sind eine Auflistung von booleschen Werten, in denen verschiedene Zeilen Gerätefunktionen beschrieben werden.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: LINEDEVCAPFLAGS_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359794"
---
# <a name="linedevcapflags_-constants"></a>Linedevcapflags- \_ Konstanten

Die Bits-Flag-Konstanten von **linedevcapflags \_** sind eine Auflistung von booleschen Werten, in denen verschiedene Zeilen Gerätefunktionen beschrieben werden.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**linedevcapflags \_ callhub**
</dt> <dd> <dl> <dt>



Gibt an, ob callhubs in dieser Zeile unterstützt werden. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**linedevcapflags \_ callhubtracking**
</dt> <dd> <dl> <dt>



Gibt an, ob die callhub-Nachverfolgung in dieser Zeile unterstützt wird Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**linedevcapflags- \_ closedrop**
</dt> <dd> <dl> <dt>



Gibt an, was geschieht, wenn eine geöffnete Zeile geschlossen wird, während die Anwendung Aufrufe aktiv in der Zeile ausgeführt hat. **True** gibt an, dass der Dienstanbieter alle aktiven Aufrufe in der Zeile löscht (löscht), wenn die letzte Anwendung, die die Zeile geöffnet hat, mit [**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)geschlossen wird. **False** gibt an, dass der Dienstanbieter in solchen Fällen keine aktiven Aufrufe löscht. Stattdessen bleiben die Aufrufe aktiv und Steuern externe Geräte. Ein Dienstanbieter legt dieses Bit in der Regel auf " **false** " fest, wenn es ein anderes Gerät gibt, das den Anruf aufrechterhalten kann. Wenn z. b. eine analoge Linie den Computer aufweist und die Telefonnummer in einer Partei Konfiguration direkt mit Ihnen verbunden ist, hält das OFFHOOK-Telefon den Anruf automatisch an, selbst nachdem der Computer eingeschaltet ist.

Anwendungen sollten dieses Flag überprüfen, um zu bestimmen, ob der Benutzer gewarnt werden soll (im Dialogfeld OK/Abbrechen), dass aktive Aufrufe verloren gehen.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**linedevcapflags \_ crossaddrconf**
</dt> <dd> <dl> <dt>



Gibt an, ob Aufrufe an verschiedene Adressen in dieser Zeile übertragen werden können.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**linedevcapflags- \_ dialabrechnung**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**linedevcapflags- \_ dialdialtone**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**linedevcapflags- \_ dialquiet**
</dt> <dd> <dl> <dt>



Diese Flags geben an, ob der deklarable String-Modifizierer "$", "@" oder "W" für ein bestimmtes Zeilen Gerät unterstützt wird. Dies ist **true** , wenn der-Modifizierer unterstützt wird. andernfalls **false**. Das "?" (der Benutzer wird aufgefordert, den Wähl Vorgang fortzusetzen) wird nie von einem liniengerät unterstützt. Diese Flags ermöglichen es einer Anwendung, nach oben zu ermitteln, welche modifiziererer zur Generierung eines lineerr führen würden. Die Anwendung hat die Wahl, dass für nicht unterstützte Zeichen oder die "RAW"-Zeichenfolge aus [**linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) als Teil von Funktionen wie [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) oder [**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial) vorab überprüft werden kann, und ermöglicht der Funktion, einen Fehler zu generieren, um zu erkennen, welcher nicht unterstützte Modifizierer zuerst in der Zeichenfolge auftritt.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**linedevcapflags \_ highlevcomp**
</dt> <dd> <dl> <dt>



Gibt an, ob in dieser Zeile allgemeine Kompatibilitäts Informationselemente unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**linedevcapflags \_ lowlevcomp**
</dt> <dd> <dl> <dt>



Gibt an, ob Kompatibilitäts Informationselemente auf niedriger Ebene in dieser Zeile unterstützt werden.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**linedevcapflags \_ MediaControl**
</dt> <dd> <dl> <dt>



Gibt an, ob Medien Steuerungs Vorgänge für Aufrufe in dieser Zeile verfügbar sind.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**linedevcapflags- \_ MSP**
</dt> <dd> <dl> <dt>



Gibt an, ob der Zeile ein Medien Dienstanbieter (MSP) zugeordnet ist. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**linedevcapflags \_ multipleaddr**
</dt> <dd> <dl> <dt>



Gibt an, ob [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)oder [**TSPI \_ linedial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) mehrere Adressen gleichzeitig behandeln kann (wie bei umgekehrtem Multiplexing).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**"linedevcapflags" \_ privateobjects**
</dt> <dd> <dl> <dt>



Gibt an, ob [anbieterspezifische Schnittstellen](./provider-specific-interfaces.md) implementiert wurden. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

