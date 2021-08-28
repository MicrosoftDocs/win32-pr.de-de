---
description: Rendert eine Textur in einer Datei und gibt das Ergebnis asynchron an den Host zurück.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5::RenderTextureAsync-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400ade8aa962a73234efbfb710d9ab6b178dfd4e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626566"
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
Die ID der zu rendernde Textur.

*sliceIndex*   
Der Index des Slices innerhalb der textur, die gerendert werden soll.

*formatOverride*   
Die Farbformatüberschreibung.

*Niedriger*   

*Oberen*   

*shaderFileName*   
Eine COM-Zeichenfolge, die den Pfadnamen der Shaderdatei enthält.

*numFloatShaderVars*   
Die Anzahl der Gleitkomma-Shadervariablen

*count6 \_ shaderFloatVarName*   
COM-Zeichenfolgen, die die Namen der Gleitkomma-Shadervariablen zuordnen.

*count6 \_ shaderFloatVarValue*   
Die Gleitkomma-Shadervariablen.

*numBoolShaderVars*   
Die Anzahl der booleschen Shadervariablen.

*count9 \_ shaderBoolVarName*   
COM-Zeichenfolgen, die die Namen der booleschen Shadervariablen enthalten.

*count9 \_ shaderBoolVarValue*   
Die booleschen Shadervariablen.

*renderContentFileName*   
Eine COM-Zeichenfolge, die den Pfadnamen der Datei enthält, in die die gerenderte Textur geschrieben wurde.

*Rückrufe*   
Die Adresse eines Objekts, das die IPixEngine5-Rückrufschnittstelle bereitstellt.

*requestCookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*progressIntervalMsecs*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
