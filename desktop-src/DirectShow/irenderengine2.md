---
description: Die IRenderEngine2-Schnittstelle ermöglicht es der Anwendung, den von DirectShow-Bearbeitungs Diensten (des) verwendeten Standardfilter für die Videogröße zu ersetzen. Diese Schnittstelle wird von der grundlegenden Renderingengine und der intelligenten Rendering-Engine unterstützt
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: IRenderEngine2-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358753"
---
# <a name="irenderengine2-interface"></a>IRenderEngine2-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IRenderEngine2` Schnittstelle ermöglicht es der Anwendung, den von DirectShow-Bearbeitungs Diensten (des) verwendeten Standardfilter für die Videogröße zu ersetzen. Diese Schnittstelle wird von der [grundlegenden Renderingengine](basic-render-engine.md) und der [intelligenten Rendering-Engine](smart-render-engine.md) unterstützt

## <a name="members"></a>Member

Die **IRenderEngine2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IRenderEngine2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IRenderEngine2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Abbild-GUID**](irenderengine2-setresizerguid.md) | Gibt die CLSID eines benutzerdefinierten Größenänderung Filters an, der von der Anwendung bereitgestellt wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
