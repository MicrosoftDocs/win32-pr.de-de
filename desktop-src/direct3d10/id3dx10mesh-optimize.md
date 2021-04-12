---
description: Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'ID3DX10Mesh:: optimiert-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355276"
---
# <a name="id3dx10meshoptimize-method"></a>ID3DX10Mesh:: optimiert-Methode

Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Gibt den Typ der auszuführenden Optimierung an. Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus D3DXMESHOPT und D3DXMESH festgelegt werden (mit Ausnahme von D3DXMESH \_ 32 Bit, D3DXMESH \_ IB \_ Write only und D3DXMESH \_ Write).

</dd> <dt>

*pfakeremap* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Array von uint (eins pro Gesicht), das die ursprüngliche Gitterfläche angibt, die jedem Gesicht im optimierten Mesh entspricht. Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.

</dd> <dt>

*ppvertexremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***

Adresse eines Zeigers auf eine [**ID3D10Blob-Schnittstelle**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert ein neues Mesh. Bevor Sie optimieren ausführen, muss eine Anwendung durch Aufrufen von [**ID3DX10Mesh:: generateanpoinencyandpointreps**](id3dx10mesh-generateadjacencyandpointreps.md)einen Ereignis Puffer generieren. Der zutreffende Puffer enthält Informationen zu den Daten, z. b. eine Liste der Kanten und die Gesichter, die nebeneinander angeordnet sind.

Diese Methode ähnelt der [**ID3DX10Mesh:: clonemesh**](id3dx10mesh-clonemesh.md) -Methode, mit der Ausnahme, dass Sie beim Erzeugen des neuen Klon des Netzes eine Optimierung durchführen kann. Das Ausgabe Mesh erbt alle Erstellungs Parameter des eingabemesh.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
