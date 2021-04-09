---
description: Commit für alle an einem Mesh vorgenommenen Änderungen auf dem Gerät durchgeführt, sodass die Änderungen gerendert werden können. Dies sollte aufgerufen werden, nachdem die Daten eines Netzes geändert wurden und bevor es gerendert wird. Ein Mesh kann nur dann gerendert werden, wenn es auf dem Gerät ausgeführt wird. Siehe Bemerkungen.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh:: commitondevice-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050864"
---
# <a name="id3dx10meshcommittodevice-method"></a>ID3DX10Mesh:: committo Device-Methode

Commit für alle an einem Mesh vorgenommenen Änderungen auf dem Gerät durchgeführt, sodass die Änderungen gerendert werden können. Dies sollte aufgerufen werden, nachdem die Daten eines Netzes geändert wurden und bevor es gerendert wird. Ein Mesh kann nur dann gerendert werden, wenn es auf dem Gerät ausgeführt wird. Siehe Bemerkungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Wenn ein Mesh geladen wird, werden die Daten in stagingressourcen geladen, was bedeutet, dass die Daten geändert, aber nicht gerendert werden können. Wenn committo Device aufgerufen wird, werden die Daten aus den stagingressourcen in Geräte Ressourcen kopiert, sodass Sie gerendert werden können. Obwohl die Daten auf dem Gerät committet werden, verbleiben die stagingressourcen und können geändert werden. Wenn Änderungen an den stagingressourcen vorgenommen werden, müssen die stagingressourcen erneut an das Gerät übertragen werden, damit diese Änderungen auf dem Bildschirm gerendert werden.

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

 

 




