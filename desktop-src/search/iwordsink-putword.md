---
description: Legt ein Wort und seine Position im IWordSink-Objekt ab.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: IWordSink::P utWord-Methode (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e860aafbef633e226933281aaaa0be5c6429387542e7c3ae2d65d3026fd7fe37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597600"
---
# <a name="iwordsinkputword-method"></a>IWordSink::P utWord-Methode

Legt ein Wort und seine Position im [**IWordSink-Objekt**](iwordsink.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cwc* \[ In\]
</dt> <dd>

Die Anzahl der Zeichen in *pwcInBuf.*

</dd> <dt>

*pwcInBuf* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine alternative Form eines Worts aus dem Quelltext enthält. Dieser Parameter wird von **PutWord nicht geändert.** Sie können den *pTextSource-Parameter* [**von IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) entsprechend übergeben.

</dd> <dt>

*cwcSrcLen* \[ In\]
</dt> <dd>

Die Anzahl der Zeichen im Quelltextpuffer (angegeben durch den *pTextSource-Parameter* für [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)), die dem in *pwcInBuf* enthaltenen Wort entsprechen.

</dd> <dt>

*cwcSrcPos* \[ In\]
</dt> <dd>

Die Anfangsposition des Worts in *pwcInBuf* im Quelltextpuffer (angegeben durch den *pTextSource-Parameter* für [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Der Vorgang wurde erfolgreich abgeschlossen. Gibt außerdem an, dass kein text mehr zum Auffüllen des Puffers verfügbar ist.<br/>                                  |
| <dl> <dt>**SPRACHE \_ S \_ LARGE \_ WORD**</dt> </dl> | Der Wert *von cwc* ist größer als der Wert für *ulMaxTokenSize,* der in [**IWordBreaker::Init angegeben ist.**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init) <br/> |



 

## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass **die IWordSink::P utWord-Methode** immer das ursprüngliche Wort wie in *pTextSource enthält.* Alternative Formen des Worts werden mithilfe von [**IWordSink::P utAltWord an WordSink übergeben.**](iwordsink-putaltword.md) Außerdem wird empfohlen, dass die Wörter in *pwcInBuf* so genau wie möglich mit dem Quelltext übereinstimmen. Behalten Sie z. B. nach Möglichkeit Groß- und Akzente bei.

Dieser Aufruf muss für jedes Von *pTextSource* abgerufene Wort vorgenommen werden, mit Ausnahme der Wörter, für die der [**IWordSink::P utAltWord-Aufruf**](iwordsink-putaltword.md) erfolgt ist. Das Wort wird mit einem EOW-Zeichen beendet, wenn es im WordSink gespeichert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Search.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
