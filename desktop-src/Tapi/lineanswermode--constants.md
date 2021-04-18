---
description: Die Bit-Flag-Konstanten für den linebeantwortermodus \_ beschreiben, wie sich ein vorhandener aktiver-Befehl auf einem Zeilen Gerät durch das beantworten eines anderen Angebots Aufrufes in derselben Zeile auswirkt.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: LINEANSWERMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358771"
---
# <a name="lineanswermode_-constants"></a>Linebeantwortungsmoduskonstanten \_

Die Bit-Flag-Konstanten für den **linebeantwortermodus \_** beschreiben, wie sich ein vorhandener aktiver-Befehl auf einem Zeilen Gerät durch das beantworten eines anderen *Angebots* Aufrufes in derselben Zeile auswirkt.

<dl> <dt>

<span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**Zeilen beantwortungsmodus- \_ Drop**
</dt> <dd> <dl> <dt>



Der derzeit aktive-Rückruf wird automatisch gelöscht.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**lineantwortmodus \_ halten**
</dt> <dd> <dl> <dt>



Der derzeit aktive Anruf wird automatisch angehalten.


</dt> </dl> </dd> <dt>

<span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**lineantwortmodus " \_ None"**
</dt> <dd> <dl> <dt>



Das beantworten eines weiteren Aufrufes in derselben Zeile hat keine Auswirkung auf den vorhandenen aktiven-Befehl in der Zeile.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Wenn ein Aufruf erfolgt (wird angeboten), wenn ein anderer Aufruf bereits aktiv ist, wird der neue Aufruf durch Aufrufen von [**lineanswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)mit verbunden. Welche Auswirkung dies auf den vorhandenen aktiven-Rückruf hat, hängt von den Gerätefunktionen der Zeile ab. Der erste Anruf ist möglicherweise nicht betroffen, er wird möglicherweise automatisch gelöscht, oder er wird automatisch angehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




