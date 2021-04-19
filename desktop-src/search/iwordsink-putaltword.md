---
description: Fügt ein alternatives Wort und seine Position in das iwordsink-Objekt ein.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: Iwordsink::P utaltword-Methode (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344262"
---
# <a name="iwordsinkputaltword-method"></a>Iwordsink::P utaltword-Methode

Fügt ein alternatives Wort und seine Position in das [**iwordsink**](iwordsink.md) -Objekt ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT PutAltWord(
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

Ein Zeiger auf einen Puffer, der eine alternative Form eines Worts aus dem Quelltext enthält. Dieser Parameter wird nicht von **putaltword** geändert. Sie können den *ptextsource* -Parameter nach Bedarf von [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) übergeben.

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
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Der Vorgang wurde erfolgreich abgeschlossen. Gibt auch an, dass noch kein Text mehr verarbeitet werden muss.<br/>                                            |
| <dl> <dt>**Sprache \_ \_großes \_ Wort**</dt> </dl> | Der Wert von *CWC* ist größer als der Wert für *ulmaxumkensize* , der in [**iwordbreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)angegeben wird. <br/> |



 

## <a name="remarks"></a>Bemerkungen

**Putaltword** stellt eine alternative Form eines Worts in [**iwordsink**](iwordsink.md)dar. Das Wort wird an derselben Position wie das ursprüngliche Wort in der Text Quelle abgelegt (*ptextsource* in [**iwordbreaker:: breaktext**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)). Standardmäßig beendet **putaltword** Wörter mit einem **wordrep- \_ \_** Break-Break-Typ aus dem Enumerationstyp " [**wordrep \_ break \_ Type**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ".

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

 

 
