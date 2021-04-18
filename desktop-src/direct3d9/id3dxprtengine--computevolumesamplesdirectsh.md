---
description: Berechnet eine Projektion entfernter Beleuchtung in eine kugelförmige (SH) Basis Vektoren, die die Ereignis Strahlen an angegebenen Orten darstellen.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine:: computevolumesamplesdirectsh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351984"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>ID3DXPRTEngine:: computevolumesamplesdirectsh-Methode

Berechnet eine Projektion entfernter Beleuchtung in eine kugelförmige (SH) Basis Vektoren, die die Ereignis Strahlen an angegebenen Orten darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OrderIn* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Darstellung der entfernten Beleuchtung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Der Bewertungs Grad ist OrderIn-1.

</dd> <dt>

*Order out* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Darstellung der lokalen Beleuchtung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Der Bewertungs Grad ist orderout-1.

</dd> <dt>

*NumVolSamples.xml* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Beispiel Speicherorte.

</dd> <dt>

*psamplelocs* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Die Position für jede Stichprobe.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das die entfernte Beleuchtung in SH-Basis Vektoren projiziert. Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden. Diese Methode generiert \* Orser ² orderout "² Skars pro Kanal an jedem Beispiel Speicherort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird berechnet, wie Light aus einer entfernten Quelle an jedem von psamplelocs angegebenen Raum erreicht wird. Die SH-Koeffizienten stellen die Zuordnung der Quell Strahlung an jedem psamplelocs-Punkt zur Übertragung von Ereignis Strahlen dar.

Um diese Methode erfolgreich zu verwenden, müssen Sie die Stichprobenentnahme für eine Kugel mit usesphere = **true** und usecosinus = **false** in [**ID3DXPRTEngine:: setsamplinginfo**](id3dxprtengine--setsamplinginfo.md); festlegen. Andernfalls gibt diese Methode einen Fehler mit D3DERR \_ invalidcallzurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computevolumesamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
