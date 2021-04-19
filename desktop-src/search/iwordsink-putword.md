---
description: Fügt ein Wort und seine Position in das iwordsink-Objekt ein.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: Iwordsink::P utword-Methode (Search. h)
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
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339755"
---
# <a name="iwordsinkputword-method"></a>Iwordsink::P utword-Methode

Fügt ein Wort und seine Position in das [**iwordsink**](iwordsink.md) -Objekt ein.

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

*CWC* \[ in\]
</dt> <dd>

Die Anzahl der Zeichen in *pwcinbuf*.

</dd> <dt>

*pwcinbuf* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine alternative Form eines Worts aus dem Quelltext enthält. Dieser Parameter wird nicht von **putword** geändert. Sie können den *ptextsource* -Parameter nach Bedarf von [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) übergeben.

</dd> <dt>

*cwcsrclen* \[ in\]
</dt> <dd>

Die Anzahl der Zeichen im Quell Text Puffer (angegeben durch den *ptextsource* -Parameter für [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)), die dem in *pwcinbuf* enthaltenen Wort entsprechen.

</dd> <dt>

*cwcsrcpos* \[ in\]
</dt> <dd>

Die Anfangsposition des Worts in *pwcinbuf* im Quell Text Puffer (angegeben durch den *ptextsource* -Parameter für [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Der Vorgang wurde erfolgreich abgeschlossen. Gibt auch an, dass kein Text mehr zum Auffüllen des Puffers verfügbar ist.<br/>                                  |
| <dl> <dt>**Sprache \_ \_großes \_ Wort**</dt> </dl> | Der Wert von *CWC* ist größer als der Wert für *ulmaxumkensize* , der in [**iwordbreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)angegeben wird. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass die **iwordsink::P utword** -Methode immer das ursprüngliche Wort enthält, wie es in *ptextsource* gefunden wurde. Alternative Formen des Worts werden mithilfe von [**iwordsink::P utaltword**](iwordsink-putaltword.md)an wordsink übermittelt. Außerdem wird empfohlen, dass die Wörter in *pwcinbuf* so genau wie möglich mit dem Quelltext übereinstimmen. Behalten Sie z. b. Groß-/Kleinschreibung und Akzente bei.

Dieser Rückruf muss für jedes aus *ptextsource* abgerufene Wort mit Ausnahme derjenigen erfolgen, für die der [**iwordsink::P utaltword**](iwordsink-putaltword.md) -Befehl durchgeführt wurde. Das Wort wird mit einem EOW-Zeichen beendet, wenn es in der wordsink gespeichert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwordsink**](iwordsink.md)
</dt> </dl>

 

 
