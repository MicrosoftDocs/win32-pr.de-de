---
description: Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn eine Texturlast abgeschlossen wurde.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks::LoadTextureFromFileComplete-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e9a9530fb9ada600d818494565765655c2c8cfb3bca938d8b9dff9d240aa6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985970"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks::LoadTextureFromFileComplete-Methode

Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn eine Texturlast abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a>Parameter

*textureId*   
Die ID der geladenen Textur.

*textureDesc*   
Der Texturdeskriptor der geladenen Textur.

*numSlices*   
Die Anzahl der Slices, über die die Textur verfügt.

*count2 \_ sliceIndicies*   
Sliceindicies, die der Textur zugeordnet sind.

*count2 \_ sliceDescriptors*   
Deskriptoren für jeden Slice.

*numFormatOverrides*   
Die Anzahl der Formatüberschreibungen.

*count5 \_ formatOverrides*   
Das Format überschreibt.

*Histogramm*   
Die Adresse der Histogrammdaten für die geladene Textur.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
