---
description: Übertragen Sie alle an einem Gitternetz vorgenommenen Änderungen an das Gerät, damit die Änderungen gerendert werden können. Diese sollte aufgerufen werden, nachdem die Daten eines Gitters geändert und bevor sie gerendert werden. Ein Gitternetz kann nur gerendert werden, wenn es an das Gerät übertragen wird. Siehe Bemerkungen.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: ID3DX10Mesh::CommitToDevice-Methode (D3DX10.h)
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
ms.openlocfilehash: 50dde79e57ca7edf838f05b1fa1b4d10f5da5cc936b3cbf563c7838703650806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567030"
---
# <a name="id3dx10meshcommittodevice-method"></a>ID3DX10Mesh::CommitToDevice-Methode

Übertragen Sie alle an einem Gitternetz vorgenommenen Änderungen an das Gerät, damit die Änderungen gerendert werden können. Diese sollte aufgerufen werden, nachdem die Daten eines Gitters geändert und bevor sie gerendert werden. Ein Gitternetz kann nur gerendert werden, wenn es an das Gerät übertragen wird. Siehe Bemerkungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Wenn ein Gitternetz geladen wird, werden die Daten in Stagingressourcen geladen, was bedeutet, dass die Daten geändert, aber nicht gerendert werden können. Wenn CommitToDevice aufgerufen wird, werden die Daten aus den Stagingressourcen in Geräteressourcen kopiert, damit sie gerendert werden können. Obwohl die Daten an das Gerät übertragen werden, bleiben die Stagingressourcen erhalten und können geändert werden. Wenn Änderungen an den Stagingressourcen vorgenommen werden, müssen die Stagingressourcen erneut auf das Gerät übertragen werden, damit diese Änderungen auf dem Bildschirm gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




