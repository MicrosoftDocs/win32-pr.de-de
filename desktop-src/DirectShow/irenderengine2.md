---
description: Die IRenderEngine2-Schnittstelle ermöglicht es der Anwendung, den von DirectShow Editing Services (DES) verwendeten Standardfilter für die Größenänderung von Videos zu ersetzen. Die Basic Render Engine und die Smart Render Engine unterstützen beide diese Schnittstelle.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: IRenderEngine2-Schnittstelle (Qedit.h)
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
ms.openlocfilehash: 39f1bc68fc6cd76e87d1998047cb211b3a8aa8e263c90e0494c7eaf15d52f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818508"
---
# <a name="irenderengine2-interface"></a>IRenderEngine2-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Mit `IRenderEngine2` der -Schnittstelle kann die Anwendung den Standardfilter für die Größenänderung von Videos ersetzen, der von DirectShow Editing Services (DES) verwendet wird. Die [Basic Render Engine](basic-render-engine.md) und die Smart Render [Engine](smart-render-engine.md) unterstützen beide diese Schnittstelle.

## <a name="members"></a>Member

Die **IRenderEngine2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IRenderEngine2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IRenderEngine2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Gibt die CLSID eines benutzerdefinierten Größenänderungsfilters an, der von der Anwendung bereitgestellt wird.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9.0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Bereitstellen eines benutzerdefinierten Video-Resizers](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
