---
description: Fügt eine alternative Form eines Worts in das iwordformsink-Objekt ein.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: Iwordformsink::P utaltword-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750360"
---
# <a name="iwordformsinkputaltword-method"></a>Iwordformsink::P utaltword-Methode

Fügt eine alternative Form eines Worts in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwcinbuf* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine alternative Form eines Worts enthält.

</dd> <dt>

*CWC* \[ in\]
</dt> <dd>

Die Anzahl der Zeichen in *pwcinbuf*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Der Vorgang wurde erfolgreich abgeschlossen. <br/>                                                                                             |
| <dl> <dt>**Sprache \_ \_großes \_ Wort**</dt> </dl> | Der Wert von *CWC* ist größer als der Wert für *ulmaxumkensize* , der in [**istemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init)angegeben wird. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von der [**generatewordforms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) -Methode der [**istemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) -Implementierung aufgerufen. Alle alternativen Formulare für ein Wort, mit Ausnahme des letzten, werden durch Aufrufen von **iwordformsink::P utaltword** in das [**iwordformsink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) -Objekt eingefügt. Die endgültige alternative Form eines Worts, bei der es sich immer um die ursprüngliche Form des Worts handelt, wird durch Aufrufen von [**iwordformsink::P utword**](iwordformsink-putword.md)behandelt.

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

 

 
