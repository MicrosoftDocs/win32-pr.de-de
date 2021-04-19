---
description: Die \_ Bit-Flag-Konstanten von lineforwardmode beschreiben die Bedingungen, unter denen Aufrufe an eine Adresse weitergeleitet werden können.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: LINEFORWARDMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370853"
---
# <a name="lineforwardmode_-constants"></a>Lineforwardmode- \_ Konstanten

Die Bit-Flag-Konstanten von **lineforwardmode \_** beschreiben die Bedingungen, unter denen Aufrufe an eine Adresse weitergeleitet werden können.

<dl> <dt>

<span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**lineforwardmode \_ ausgelastet**
</dt> <dd> <dl> <dt>



Alle Aufrufe an "ausgelastet" weiterleiten, unabhängig von deren Ursprung. Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**lineforwardmode \_ busyextern**
</dt> <dd> <dl> <dt>



Alle externen Aufrufe an ausgelasteter weiterleiten. Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**lineforwardmode \_ busyinternal**
</dt> <dd> <dl> <dt>



Alle internen Aufrufe von ausgelastet weiterleiten. Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**lineforwardmode- \_ busyna**
</dt> <dd> <dl> <dt>



Alle Aufrufe an "ausgelastet"/"keine Antwort" weiterleiten, unabhängig von deren Ursprung. Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe von ausgelastet ist und keine Antwort separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**lineforwardmode \_ busynaextern**
</dt> <dd> <dl> <dt>



Leiten Sie alle externen Aufrufe für ausgelastet/keine Antwort weiter. Verwenden Sie diesen Wert, wenn die Aufruf Weiterleitung bei "ausgelastet" und "keine Antwort" bei internen Aufrufen nicht separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**lineforwardmode \_ busynainternal**
</dt> <dd> <dl> <dt>



Alle internen Aufrufe an "ausgelastet"/"keine Antwort" weiterleiten. Verwenden Sie diesen Wert, wenn die Aufruf Weiterleitung bei "ausgelastet" und "keine Antwort" bei internen Aufrufen nicht separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**lineforwardmode- \_ busynaspecific**
</dt> <dd> <dl> <dt>



Forward on ausgelastet/keine Antwort alle Aufrufe, die von einer bestimmten Adresse stammen (selektive Aufruf Weiterleitung).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**lineforwardmode- \_ busyspecific**
</dt> <dd> <dl> <dt>



Forward an ausgelasteten aufrufen, die bei einer bestimmten Adresse (selektive Aufruf Weiterleitung) entstanden sind.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**lineforwardmode \_ noansw**
</dt> <dd> <dl> <dt>



Alle Aufrufe ohne Antwort weiterleiten, unabhängig von deren Ursprung. Verwenden Sie diesen Wert, wenn die Aufruf Weiterleitung für interne und externe Aufrufe ohne Antwort nicht separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**lineforwardmode \_ noanswexternal**
</dt> <dd> <dl> <dt>



Alle externen Aufrufe ohne Antwort weiterleiten. Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe ohne Antwort separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**lineforwardmode \_ noanswinternal**
</dt> <dd> <dl> <dt>



Alle internen Aufrufe ohne Antwort weiterleiten. Verwenden Sie diesen Wert, wenn die Weiterleitung für interne und externe Aufrufe ohne Antwort separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**lineforwardmode \_ noanswspecific**
</dt> <dd> <dl> <dt>



Forward auf keine Antwort alle Aufrufe, die von einer angegebenen Adresse stammen (selektive Aufruf Weiterleitung).


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**"lineforwardmode" ist \_ nicht erreichbar.**
</dt> <dd> <dl> <dt>



Aufrufe werden weitergeleitet, aber die Bedingungen, unter denen die Weiterleitung erfolgt, sind nicht bekannt, und der Dienstanbieter wird nie bekannt sein. (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**lineforwardmode \_ untd**
</dt> <dd> <dl> <dt>



Alle Aufrufe unabhängig von ihrem Ursprung bedingungslos weiterleiten. Verwenden Sie diesen Wert, wenn die bedingungslose Weiterleitung für interne und externe Aufrufe nicht separat gesteuert werden kann. Bei der bedingungslosen Weiterleitung wird die Weiterleitung von ausgelasteten und/oder keine Antwort Bedingungen


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**lineforwardmode \_ unkonform**
</dt> <dd> <dl> <dt>



Leiten Sie alle externen Aufrufe bedingungslos weiter. Verwenden Sie diesen Wert, wenn die Bedingungs bedingte Weiterleitung für interne und externe Aufrufe separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**lineforwardmode \_ unintern**
</dt> <dd> <dl> <dt>



Alle internen Aufrufe bedingungslos weiterleiten. Verwenden Sie diesen Wert, wenn die Bedingungs bedingte Weiterleitung für interne und externe Aufrufe separat gesteuert werden kann.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**lineforwardmode \_ nicht-spezifisch**
</dt> <dd> <dl> <dt>



Alle Aufrufe, die von einer angegebenen Adresse stammen (selektive Aufruf Weiterleitung), bedingungslos weiterleiten.


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**"lineforwardmode" \_ unbekannt**
</dt> <dd> <dl> <dt>



Aufrufe werden weitergeleitet, aber die Bedingungen, unter denen die Weiterleitung erfolgt, sind zurzeit nicht bekannt. Es ist möglich, dass die Bedingungen zu einem späteren Zeitpunkt bekannt werden. (TAPI-Versionen 1,4 und höher)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Die von lineforwardmode definierten Bitflags \_ sind nicht orthogonal. Bei der bedingungslosen Weiterleitung werden alle spezifischen Bedingungen, z. b. ausgelastet oder keine Antwort Wenn die bedingungslose Weiterleitung nicht wirksam ist, kann die Weiterleitung an ausgelastet und ohne Antwort separat oder nicht separat gesteuert werden. Bei separater Steuerung \_ können die noansw-Flags "lineforwardmode ausgelastet" und "lineforwardmode" \_ separat verwendet werden. Wenn diese nicht separat gesteuert wird, muss das Flag lineforwardmode \_ busyna verwendet werden. Wenn die Weiterleitung interner und externer Aufrufe separat gesteuert werden kann, können auch die externen lineforwardmode \_ -und lineforwardmode- \_ Flags separat verwendet werden. andernfalls wird die Kombination verwendet.

Adress Funktionen geben an, welche Weiterleitungs Modi für jede Adresse verfügbar sind, die einer Zeile zugewiesen ist. Eine Anwendung kann [**lineforward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) verwenden, um Weiterleitungs Bedingungen auf dem Switch festzulegen.

Aus Gründen der Abwärtskompatibilität liegt es in der Verantwortung des Dienstanbieters, die ausgehandelte API-Version in der Zeile zu untersuchen und diese lineforwardmode-Werte nicht zu verwenden, \_ Wenn Sie von der ausgehandelten Version nicht unterstützt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




