---
description: Eine Rückruffunktion, die verwendet wird, um den Host von Objekt Tabellen Informationen zu benachrichtigen.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iobjecttablecallback:: resultCallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747393"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>Iobjecttablecallback:: resultCallback-Methode

Eine Rückruffunktion, die verwendet wird, um den Host von Objekt Tabellen Informationen zu benachrichtigen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a>Parameter

*numElements*   
Die Gesamtanzahl der Felder in allen Spalten aller-Objekte.

*numRows*   
Die Anzahl der Objekte, die übertragen werden.

*NumColumns*   
Die Anzahl der Spalten (Felder) der Informationen, die für jedes Objekt übertragen werden.

*count0 \_ prowdata*   
Informationen zu den Objekten ein-Element für jedes Feld der einzelnen-Objekte.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iobjecttablecallback**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
