---
description: Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Licht Sprung in eine kugelförmige (SH) Basis Vektoren, die den Vorfall Glanz an angegebenen Orten darstellen.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'ID3DXPRTEngine:: computevolumesamples-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361238"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>ID3DXPRTEngine:: computevolumesamples-Methode

Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Licht Sprung in eine kugelförmige (SH) Basis Vektoren, die den Vorfall Glanz an angegebenen Orten darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psurfdatain* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt.

</dd> <dt>

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*NumVolSamples.xml* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Beispiel Speicherorte.

</dd> <dt>

*psamplelocs* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Die Position für jede Stichprobe. Wenn psamplelocs den Wert **null** hat, berechnet computevolumesamples Übertragungs Matrizen an jedem Mesh-Scheitelpunkt. Wenn psamplelocs jedoch nicht **null** ist, müssen Sie eine Stichprobe über eine Kugel ausführen (Set usesphere = **true** und usecosinus = **false** in [**ID3DXPRTEngine:: setsamplinginfo**](id3dxprtengine--setsamplinginfo.md)); Andernfalls gibt computevolumesamples D3DERR \_ invalidcallzurück.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das die direkte Beleuchtung aus dem vorherigen Licht Sprung in SH-Basis Vektoren projiziert. Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode berechnet, wie das Licht aus der Quell Funktions Funktion von der Oberfläche reflektiert wird, die die Szene darstellt (psurfdatain) und an jedem von psamplelocs angegebenen Punkt des Raums ankommt. Die SH-Koeffizienten stellen die Zuordnung der Quell Strahlung an jedem psamplelocs-Punkt zur Übertragung von Ereignis Strahlen dar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computevolumesamplesdirectsh**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
