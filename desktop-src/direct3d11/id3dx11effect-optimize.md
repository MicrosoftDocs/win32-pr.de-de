---
title: ID3DX11Effect-Optimierungsmethode (D3dx11effect. h)
description: Minimieren Sie den für einen Effekt benötigten Arbeitsspeicher.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Optimieren der Methode Direct3D 11
- Optimieren der Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, Methode optimieren
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996088"
---
# <a name="id3dx11effectoptimize-method"></a>ID3DX11Effect:: optimiert-Methode

Minimieren Sie den für einen Effekt benötigten Arbeitsspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Ein Effekt verwendet zwei verschiedene Möglichkeiten, um die für die Laufzeit erforderlichen Informationen zum Ausführen eines Effekts zu speichern und die Metadaten zu speichern, die für die Wiedergabe von Informationen an eine Anwendung mithilfe der API erforderlich sind. Sie können den von einem Effekt benötigten Arbeitsspeicher verringern, indem Sie **ID3DX11Effect:: optimiert** aufrufen, wodurch die reflektionsmetadaten aus dem Arbeitsspeicher entfernt werden. API-Methoden zum Lesen von Variablen funktionieren nicht mehr, sobald die reflektionsingendaten entfernt wurden.

Die folgenden Methoden schlagen fehl, nachdem die Optimierung für einen Effekt aufgerufen wurde.

-   [**ID3DX11Effect:: getconstantbufferbyindex**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect:: getconstantbufferbyname**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect:: getdebug**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect:: getdevice**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect:: gettechniquebyindex**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect:: gettechniquebyname**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect:: getvariablebyindex**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect:: getvariablebyname**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect:: getvariablebysemantic**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> Verweise, die mit diesen Methoden vor dem Aufruf von **ID3DX11Effect:: optimiert** abgerufen werden, sind nach wie vor für den Aufruf von **ID3DX11Effect::** Optimierungen gültig Dadurch kann die Anwendung alle Variablen, Techniken und Verläufen abrufen, die Sie verwenden werden, und dann optimieren und dann den Effekt verwenden.

 

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

 

 





