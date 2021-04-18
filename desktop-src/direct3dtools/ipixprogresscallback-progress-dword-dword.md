---
description: Ein Rückruf, der den Host über den Fortschritt einer zugeordneten Anforderung benachrichtigt.
MS-HAID: vspixengine.IPixProgressCallback\_Progress\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ipixprogresscallback::P rogress-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BE74599B-C98F-4BDB-ACDF-641F77A35EEB
api_name:
- IPixProgressCallback.Progress
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0379ad6fcb5f97825469c97af38453e55585d005
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392661"
---
# <a name="span-idvspixengineipixprogresscallback_progress_dword_dwordspanipixprogresscallbackprogress-method"></a><span id="vspixengine.ipixprogresscallback_progress_dword_dword"></span>Ipixprogresscallback::P rogress-Methode

Ein Rückruf, der den Host über den Fortschritt einer zugeordneten Anforderung benachrichtigt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Progress(
   DWORD current,
   DWORD maxSize
);
```

## <a name="parameters"></a>Parameter

*Strömung*   
Der Teil einer Anforderung wurde abgeschlossen, als Anzahl der abgeschlossenen Schritte.

*MaxSize*   
Die Gesamtanzahl der Schritte zum Durchführen der Anforderung.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipixprogresscallback**](/windows/desktop/direct3dtools/ipixprogresscallback)

 

 
