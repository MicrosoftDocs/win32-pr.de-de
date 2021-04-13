---
description: Ruft Informationen darüber ab, welche Spalten (Objektdaten Typen) von der Objekttabelle unterstützt werden.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iobjecttablecallback:: getsupportedcolumns-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ed077e0921043245e4ff3dda4b1c33dd4e3f20d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481275"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>Iobjecttablecallback:: getsupportedcolumns-Methode

Ruft Informationen darüber ab, welche Spalten (Objektdaten Typen) von der Objekttabelle unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a>Parameter

*NumColumns*   
Die Anzahl der Spalten, die von der Objekttabelle unterstützt werden.

*count0_pIDs*   
Die IDs der einzelnen Spalten, die von der Objekttabelle unterstützt werden.

*count0_pBstrNames*   
Die Namen der einzelnen Spalten (als com-Zeichenfolge), die von der Objekttabelle unterstützt werden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iobjecttablecallback**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
