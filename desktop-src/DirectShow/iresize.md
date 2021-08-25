---
description: Die IResize-Schnittstelle muss von jedem benutzerdefinierten Videoänderungsfilter für DirectShow Editing Services (DES) unterstützt werden. Um einen benutzerdefinierten Resizerfilter festzulegen, rufen Sie die IRenderEngine2::SetResizerGUID-Methode für die Render-Engine auf.
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: IResize-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 19aabd7c04cb5350ef3da87e1a20db6b75f6546f0fbcf5af3422c152bcafcf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818069"
---
# <a name="iresize-interface"></a>IResize-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IResize` Schnittstelle muss von jedem benutzerdefinierten Videoänderungsfilter für DirectShow Editing Services (DES) unterstützt werden. Um einen benutzerdefinierten Resizerfilter festzulegen, rufen Sie die [**IRenderEngine2::SetResizerGUID-Methode**](irenderengine2-setresizerguid.md) für die Render-Engine auf.

## <a name="members"></a>Member

Die **IResize-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IResize** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IResize-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | Beschreibung                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**get \_ InputSize**](iresize-get-inputsize.md) | Gibt die aktuelle Eingabegröße des Resizerfilters zurück.<br/>  |
| [**\_Get MediaType**](iresize-get-mediatype.md) | Gibt den Ausgabemedientyp des Resizerfilters zurück.<br/>   |
| [**get \_ Size**](iresize-get-size.md)           | Gibt die aktuelle Ausgabegröße und den Stretchingmodus zurück.<br/> |
| [**\_Put MediaType**](iresize-put-mediatype.md) | Legt den Ausgabemedientyp fest.<br/>                       |
| [**put \_ Size**](iresize-put-size.md)           | Legt die Ausgabegröße und den Stretchmodus fest.<br/>            |



 

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

 

 
