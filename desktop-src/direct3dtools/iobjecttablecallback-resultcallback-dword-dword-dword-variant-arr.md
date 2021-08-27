---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Objekttabelleninformationen zu benachrichtigen.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableCallback::ResultCallback-Methode
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
ms.openlocfilehash: e82381211f580412414c646af58360a55f8309bd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627946"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über Objekttabelleninformationen zu benachrichtigen.

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
Die Gesamtanzahl von Feldern in allen Spalten aller Objekte.

*numRows*   
Die Anzahl der objekte, die übertragen werden.

*numColumns*   
Die Anzahl der Spalten (Felder) von Informationen, die für jedes Objekt übertragen werden.

*count0 \_ pRowData*   
Informationen zu den Objekten; ein Element für jedes Feld jedes Objekts.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IObjectTableCallback**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
