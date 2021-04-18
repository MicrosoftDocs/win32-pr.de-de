---
description: Die \_ Bit-Flag-Konstante linetranslateoption beschreibt eine Option, die von der Adressübersetzung verwendet wird.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: LINETRANSLATEOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372353"
---
# <a name="linetranslateoption_-constants"></a>Linetranslateoption- \_ Konstanten

Die Bit-Flag-Konstante **linetranslateoption \_** beschreibt eine Option, die von der Adressübersetzung verwendet wird.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**linetranslateoption \_ cancelcallwaiting**
</dt> <dd> <dl> <dt>



Wenn eine aufrufende Zeichenfolge für den Abbruch Aufruf für den Speicherort definiert ist, bewirkt das Festlegen dieses Bits, dass diese Zeichenfolge am Anfang der ausführbaren Zeichenfolge eingefügt wird. Dies wird häufig von Datenmodem-und Faxanwendungen verwendet, um die Unterbrechung von Aufrufen durch Aufrufe, die darauf warten, zu verhindern. Wenn keine aufrufende Zeichenfolge für den Abbruch Vorgang für den Speicherort definiert ist, hat dieses Bit keine Auswirkung. Beachten Sie, dass für Anwendungen, die dieses Bit verwenden, empfohlen wird, auch das Secure-Bit linecallparamflags \_ im **dwcallparamflags** -Member der [**linecallpara**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) -Struktur festzulegen, die über den *lpcallparser* -Parameter an [**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) übergeben wird, sodass der Mechanismus aufgerufen wird, wenn das liniengerät einen anderen Mechanismus als dable-Ziffern verwendet.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**linetranslateoption \_ cardoverride**
</dt> <dd> <dl> <dt>



Die Standard Aufruf Karte muss mit einem angegebenen überschrieben werden.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**linetranslateoption ( \_ forceld)**
</dt> <dd> <dl> <dt>



Diese Option erzwingt, dass die Adresse (Zahl) als lange Distanz übersetzt wird.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**linetranslateoption ( \_ forcelocal)**
</dt> <dd> <dl> <dt>



Diese Option erzwingt, dass die Zahl (Address) als Local übersetzt wird.


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

[**Linecallparametriams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**Linetranslateoutput**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




