---
description: Rendert eine Textur in eine Datei und gibt das Ergebnis asynchron an den Host zurück.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5:: rendertextureasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd16214887514fa348a672c45d5eb85c2df6bca5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521523"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5:: rendertextureasync-Methode

Rendert eine Textur in eine Datei und gibt das Ergebnis asynchron an den Host zurück.

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

*textureid*   
Die ID der zu Rendering enden Textur.

*slicabdex*   
Der Index des Slice innerhalb der zu Rendering enden Textur.

*formatoverride*   
Das Farb Format Überschreibung.

*günstigere*   

*weite*   

*shaderdateiname*   
Eine com-Zeichenfolge, die den Pfadnamen der Shader-Datei enthält.

*numfloatshadervars*   
Die Anzahl von Gleit Komma-Shader-Variablen.

*count6 \_ shaderfloatvarname*   
COM-Zeichen folgen, die die Namen der Gleit Komma-Shader-Variablen zusammenhängender.

*count6 \_ shaderfloatvarvalue*   
Die Gleit Komma-Shader-Variablen.

*numboolshadervars*   
Die Anzahl der booleschen Shader-Variablen.

*count9 \_ shaderboolvarname*   
COM-Zeichen folgen, die die Namen der booleschen shadervariablen zusammen hänchern.

*count9 \_ shaderboolvarvalue*   
Die booleschen Shader-Variablen.

*rendercontentfilename*   
Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die die gerenderte Textur geschrieben wurde.

*Rückrufe*   
Die Adresse eines Objekts, das die IPixEngine5 Rückrufe-Schnittstelle bereitstellt.

*requestcookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.

*progressintervalmsekunden*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
