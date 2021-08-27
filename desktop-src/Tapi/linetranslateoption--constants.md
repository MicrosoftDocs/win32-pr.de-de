---
description: Die \_ LINETRANSLATEOPTION-Bitflagkonst constant beschreibt eine Option, die von der Adressübersetzung verwendet wird.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: LINETRANSLATEOPTION_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d1cc9f3d7798dda9dd5bb69817ccfac64ae88fbc45fccccd59563cc24614d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073020"
---
# <a name="linetranslateoption_-constants"></a>LINETRANSLATEOPTION-Konstanten \_

Die **\_ LINETRANSLATEOPTION-Bitflagkonst** constant beschreibt eine Option, die von der Adressübersetzung verwendet wird.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**
</dt> <dd> <dl> <dt>



Wenn für den Speicherort eine Zeichenfolge zum Abbrechen des Anrufs definiert ist, wird diese Zeichenfolge am Anfang der Wählbaren Zeichenfolge eingefügt, wenn dieses Bit festgelegt wird. Dies wird häufig von Datenmodem- und Faxanwendungen verwendet, um unterbrechungsfreie Anrufe durch Anrufwarterufe zu verhindern. Wenn für den Speicherort keine Zeichenfolge vom Typ Cancel Call Waiting definiert ist, hat dieses Bit keine Auswirkungen. Beachten Sie, dass Anwendungen, die dieses Bit verwenden, auch das LINECALLPARAMFLAGS \_ SECURE-Bit im **dwCallParamFlags-Member** der [**LINECALLPARAMS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) festlegen sollten, das über den *lpCallParams-Parameter* an [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) übergeben wird. Wenn das Liniengerät einen anderen Mechanismus als dialable digits verwendet, um Aufrufunterbrechungen zu unterdrücken, wird dieser Mechanismus aufgerufen.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**
</dt> <dd> <dl> <dt>



Die Standard-Anrufkarte muss mit einer angegebenen überschrieben werden.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**
</dt> <dd> <dl> <dt>



Diese Option erzwingt, dass die Adresse (Zahl) als Entfernungsabstand übersetzt wird.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**
</dt> <dd> <dl> <dt>



Diese Option erzwingt, dass die Zahl (Adresse) als lokal übersetzt wird.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**LINETRANSLATEOUTPUT**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




