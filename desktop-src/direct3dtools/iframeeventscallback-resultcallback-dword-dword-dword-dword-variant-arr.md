---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Ereignisse in der Ereignisliste zu benachrichtigen.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframeeventscallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213919"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>Iframeeventscallback:: resultCallback-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über Informationen über Ereignisse in der Ereignisliste zu benachrichtigen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a>Parameter

*Framezahl*   
Die dem Ereignis zugeordnete Frame Nummer.

*numElements*   
Die Gesamtanzahl der Felder in allen Spalten aller Ereignisse.

*numRows*   
Die Anzahl der Ereignisse im Ergebnis.

*NumColumns*   
Die Anzahl der Spalten (Felder) in jeder Zeile.

*count1 \_ prowdata*   
Informationen zu den Ereignissen ein Element für jedes Feld jedes Ereignisses.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iframeeventscallback**](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
