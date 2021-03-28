---
title: ID3DX11Effect isoptimierte-Methode (D3dx11effect. h)
description: Testen eines Effekts, um zu ermitteln, ob die reflektionsintemetadaten aus dem Arbeitsspeicher entfernt wurden.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Isoptimierte Methode Direct3D 11
- Isoptimierte Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, isoptimierte Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355537"
---
# <a name="id3dx11effectisoptimized-method"></a>ID3DX11Effect:: isoptimierte-Methode

Testen eines Effekts, um zu ermitteln, ob die reflektionsintemetadaten aus dem Arbeitsspeicher entfernt wurden.

## <a name="syntax"></a>Syntax


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** , wenn der Effekt optimiert ist. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Ein Effekt verwendet zwei verschiedene Möglichkeiten, um die für die Laufzeit erforderlichen Informationen zum Ausführen eines Effekts zu speichern und die Metadaten zu speichern, die für die Wiedergabe von Informationen an eine Anwendung mithilfe der API erforderlich sind. Sie können den von einem Effekt benötigten Arbeitsspeicher verringern, indem Sie [**ID3DX11Effect:: optimiert**](id3dx11effect-optimize.md) aufrufen, wodurch die reflektionsmetadaten aus dem Arbeitsspeicher entfernt werden. Natürlich funktionieren API-Methoden zum Lesen von Variablen nicht mehr, sobald die reflektionsliste entfernt wurde.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

