---
title: ID3DX11Effect IsOptimized-Methode (D3dx11effect.h)
description: Testen Sie einen Effekt, um zu prüfen, ob die Reflektionsmetadaten aus dem Arbeitsspeicher entfernt wurden.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- IsOptimized-Methode Direct3D 11
- IsOptimized-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11 , IsOptimized-Methode
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
ms.openlocfilehash: 5bd04bf43869f23bfec38db34be1b83b2c4f3953c7017120ebe2f0c985504b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124505"
---
# <a name="id3dx11effectisoptimized-method"></a>ID3DX11Effect::IsOptimized-Methode

Testen Sie einen Effekt, um zu prüfen, ob die Reflektionsmetadaten aus dem Arbeitsspeicher entfernt wurden.

## <a name="syntax"></a>Syntax


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE,** wenn der Effekt optimiert ist; **andernfalls FALSE**.

## <a name="remarks"></a>Hinweise

Für einen Effekt werden zwei verschiedene Möglichkeiten verwendet: zum Speichern der Informationen, die von der Laufzeit zum Ausführen eines Effekts benötigt werden, und zum Speichern der Metadaten, die erforderlich sind, um Informationen mithilfe der API an eine Anwendung zurückzureflektorieren. Sie können die für einen Effekt erforderliche Arbeitsspeichermenge minimieren, indem Sie [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) aufrufen, wodurch die Reflektionsmetadaten aus dem Arbeitsspeicher entfernt werden. Natürlich funktionieren API-Methoden zum Lesen von Variablen nicht mehr, nachdem Reflektionsdaten entfernt wurden.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

