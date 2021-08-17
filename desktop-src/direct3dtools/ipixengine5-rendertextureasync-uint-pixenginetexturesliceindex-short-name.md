---
description: Rendert eine Textur in einer Datei und gibt das Ergebnis asynchron an den Host zurück.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5::RenderTextureAsync-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41189637fd741d22fc566f913b25ddba1109854ed12a0336ffac899c10fd3147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405680"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync-Methode

Rendert eine Textur in einer Datei und gibt das Ergebnis asynchron an den Host zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*textureId*   
Die ID der zu rendernden Textur.

*sliceIndex*   
Der Index des Zu rendernden Slices innerhalb der Textur.

*formatOverride*   
Die Überschreibung des Farbformats.

*Niedriger*   

*Oberen*   

*shaderFileName*   
Eine COM-Zeichenfolge, die den Pfadnamen der Shaderdatei enthält.

*numFloatShaderVars*   
Die Anzahl der Gleitkomma-Shadervariablen

*count6 \_ shaderFloatVarName*   
COM-Zeichenfolgen, die die Namen der Gleitkomma-Shadervariablen aufeinander folgen.

*count6 \_ shaderFloatVarValue*   
Die Gleitkomma-Shadervariablen.

*numBoolShaderVars*   
Die Anzahl der booleschen Shadervariablen.

*count9 \_ shaderBoolVarName*   
COM-Zeichenfolgen, die die Namen der booleschen Shadervariablen aufeinander folgen.

*count9 \_ shaderBoolVarValue*   
Die booleschen Shadervariablen.

*renderContentFileName*   
Eine COM-Zeichenfolge, die den Pfadnamen der Datei enthält, in die die gerenderte Textur geschrieben wurde.

*Rückrufe*   
Die Adresse eines Objekts, das die IPixEngine5-Rückrufschnittstelle anordnt.

*requestCookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*progressIntervalMsecs*   
Wird nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
