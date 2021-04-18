---
description: Ein Rückruf, der den Host von Meldungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPixErrorCallback\_MessagesCallback\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixerrorcallback:: messagescallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 55343F63-BB58-4F57-884D-CEFE8AB57A27
api_name:
- IPixErrorCallback.MessagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b95a95a6ef472f2603bfa6b21c85659634074a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343937"
---
# <a name="span-idvspixengineipixerrorcallback_messagescallback_dword_issue_arrspanipixerrorcallbackmessagescallback-method"></a><span id="vspixengine.ipixerrorcallback_messagescallback_dword_issue_arr"></span>Ipixerrorcallback:: messagescallback-Methode

Ein Rückruf, der den Host von Meldungen benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT MessagesCallback(
   DWORD    count,
   Issue [] count0_messages
);
```

## <a name="parameters"></a>Parameter

*Countdown*   
Die Anzahl der Meldungen.

*count0- \_ Nachrichten*   
Die Nachrichten.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipixerrorcallback**](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
