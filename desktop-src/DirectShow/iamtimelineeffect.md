---
description: Die IAMTimelineEffect-Schnittstelle stellt Methoden zum Bearbeiten von Audio- und Videoeffekten in DirectShow Editing Services (DES) bereit.
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: IAMTimelineEffect-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f710693c967e1f0ac73c69534e8ac90a65d6603e749cd2aeae6a355ed8517415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052760"
---
# <a name="iamtimelineeffect-interface"></a>IAMTimelineEffect-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IAMTimelineEffect` -Schnittstelle stellt Methoden zum Bearbeiten von Audio- und Videoeffekten in [DirectShow Editing Services](directshow-editing-services.md) (DES) bereit. Ein Effekt kann jedem Zeitachsenobjekt hinzugefügt werden, das die [**IAMTimelineEffectable-Schnittstelle**](iamtimelineeffectable.md) verfügbar macht. Verwenden Sie die [**IPropertySetter-Schnittstelle,**](ipropertysetter.md) um Eigenschaften für einen Effekt festzulegen.

Das DES-Effektobjekt ist eigentlich ein Wrapper für eines von zwei anderen -Objekten:

-   Für Audioeffekte jeden DirectShow-Audioeffektfilter.
-   Für Videoeffekte und ein DirectX-Transformationsobjekt mit 1 Eingabe.

Microsoft unterstützt nicht mehr die Entwicklung von DirectX Transform-Objekten von Drittanbietern.

Um den Filter oder das DirectX-Transformationsobjekt für einen Effekt anzugeben, rufen Sie die [**IAMTimelineObj::SetSubObjectGUID-Methode**](iamtimelineobj-setsubobjectguid.md) auf.

Um ein Effektobjekt zu erstellen, rufen [**Sie IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) mit dem Wert TIMELINE \_ MAJOR TYPE EFFECT \_ \_ auf. Sie können den zurückgegebenen [**IAMTimelineObj-Zeiger**](iamtimelineobj.md) für die `IAMTimelineEffect` Schnittstelle abfragen.

## <a name="members"></a>Member

Die **IAMTimelineEffect-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineEffect** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineEffect-Schnittstelle** verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | Ruft die Prioritätsebene des Effekts ab.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
