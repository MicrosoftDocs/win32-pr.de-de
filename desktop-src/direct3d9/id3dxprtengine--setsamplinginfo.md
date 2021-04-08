---
description: Legt Sampling-Eigenschaften fest, die vom PRT-Simulator (preberechnetes Radiance Transfer) verwendet werden.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine:: setsamplinginfo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762126"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>ID3DXPRTEngine:: setsamplinginfo-Methode

Legt Sampling-Eigenschaften fest, die vom PRT-Simulator (preberechnetes Radiance Transfer) verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Numrays* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Lichtstrahlen, die an jedem Beispiel weitergeleitet werden sollen. Muss größer sein als Null.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

**True** gibt an, dass die Stichproben über eine vollständige Kugel berechnet werden. Der Wert **false** gibt an, dass die Stichproben über eine Hemisphäre berechnet werden.

</dd> <dt>

*Usekosinus* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Wenn **true**, verwenden Sie eine Kosinus-Gewichtung von Beispielen. Wenn sowohl usecosinus als auch usesphere den Wert **true** aufweisen, schlägt die Methode fehl, und es wird ein Fehler zurückgegeben.

</dd> <dt>

*Adaptive* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Muss den Wert **false** aufweisen. Adaptive Stichprobenentnahme ist zurzeit nicht implementiert.

</dd> <dt>

*Adaptivethresh* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, e \_ notimpl, e \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
