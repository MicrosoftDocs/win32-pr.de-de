---
description: Legt das ursprüngliche Word-Formular in das iwordformsink-Objekt ein.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: Iwordformsink::P utword-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340161"
---
# <a name="iwordformsinkputword-method"></a>Iwordformsink::P utword-Methode

Legt das ursprüngliche Word-Formular in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwcinbuf* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die endgültige alternative Form eines Worts enthält, bei der es sich immer um das ursprüngliche Wort handelt.

</dd> <dt>

*CWC* \[ in\]
</dt> <dd>

Die Anzahl der Zeichen in *pwcinbuf*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Der Vorgang wurde erfolgreich abgeschlossen. <br/> |



 

## <a name="remarks"></a>Bemerkungen

**Putword** wird von der [**generatewordforms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) -Methode der [**istemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) -Implementierung aufgerufen. Diese Methode verarbeitet die ursprüngliche Form eines Worts und wird zuletzt aufgerufen. Alle vorherigen Alternativen Formulare für ein Wort werden durch Aufrufen von [**iwordformsink::P utaltword**](iwordformsink-putphrase.md)in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt eingefügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
