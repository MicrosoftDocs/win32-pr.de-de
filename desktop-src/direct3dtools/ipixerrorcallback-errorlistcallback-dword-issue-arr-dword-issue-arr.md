---
description: Ein Rückruf, der den Host von Fehlern benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IPixErrorCallback\_ErrorListCallback\_DWORD\_Issue\_arr\_DWORD\_Issue\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixerrorcallback:: errorlistcallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B345846D-4853-4F6B-AB79-42265720451D
api_name:
- IPixErrorCallback.ErrorListCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 91754cd7db13165efcb66e9bc87b8e4661842fce
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344928"
---
# <a name="span-idvspixengineipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arrspanipixerrorcallbackerrorlistcallback-method"></a><span id="vspixengine.ipixerrorcallback_errorlistcallback_dword_issue_arr_dword_issue_arr"></span>Ipixerrorcallback:: errorlistcallback-Methode

Ein Rückruf, der den Host von Fehlern benachrichtigt, die von der zugeordneten Anforderung zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ErrorListCallback(
   DWORD    count,
   Issue [] count0_errorList,
   DWORD    count,
   Issue [] count0_warningList
);
```

## <a name="parameters"></a>Parameter

*Countdown*   
Die Anzahl der Fehler.

*count0 \_ errorlist*   
Die Fehler.

*Countdown*   
Die Anzahl der warningns.

*count0 \_ warninglist*   
Die Warnungen.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipixerrorcallback**](/windows/desktop/direct3dtools/ipixerrorcallback)

 

 
