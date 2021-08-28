---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Informationen zu Ereignissen in der Ereignisliste zu benachrichtigen.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsCallback::ResultCallback-Methode
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
ms.openlocfilehash: 1b6cf33869fce9dc51df8dcd58f98b0cc17a5f44
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623966"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über Informationen zu Ereignissen in der Ereignisliste zu benachrichtigen.

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

*frameNumber*   
Die den Ereignissen zugeordnete Framenummer.

*numElements*   
Die Gesamtanzahl der Felder in allen Spalten aller Ereignisse.

*numRows*   
Die Anzahl der Ereignisse im Ergebnis.

*numColumns*   
Die Anzahl der Spalten (Felder) in jeder Zeile.

*count1 \_ pRowData*   
Informationen zu den Ereignissen; ein Element für jedes Feld jedes Ereignisses.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IFrameEventsCallback**](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
