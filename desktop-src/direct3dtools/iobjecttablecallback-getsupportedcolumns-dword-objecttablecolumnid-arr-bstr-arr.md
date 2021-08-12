---
description: Ruft Informationen darüber ab, welche Spalten (Objektdatentypen) von der Objekttabelle unterstützt werden.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IObjectTableCallback::GetSupportedColumns-Methode
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
ms.openlocfilehash: 6f785c8fafadf62a874d6be1d4c3ab2092f9cdaf8b49cc40f826b42fb69ce3b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283235"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>IObjectTableCallback::GetSupportedColumns-Methode

Ruft Informationen darüber ab, welche Spalten (Objektdatentypen) von der Objekttabelle unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a>Parameter

*numColumns*   
Die Anzahl von Spalten, die von der Objekttabelle unterstützt werden.

*count0_pIDs*   
Die IDs der einzelnen Spalten, die von der Objekttabelle unterstützt werden.

*count0_pBstrNames*   
Die Namen der einzelnen Spalten als COM-Zeichenfolge, die von der Objekttabelle unterstützt werden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IObjectTableCallback**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
