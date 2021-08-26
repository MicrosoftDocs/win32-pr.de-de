---
description: Die IAMTimelineEffectable-Schnittstelle stellt Methoden zum Hinzufügen von Effekten zu einem Zeitachsenobjekt in DirectShow Editing Services (DES) und zum Bearbeiten der Auswirkungen auf ein Objekt bereit.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: IAMTimelineEffectable-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ad6b373f4b30209566709117b3b15ecf1a65d093ddb2dd27e9e0273b11ad0b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905030"
---
# <a name="iamtimelineeffectable-interface"></a>IAMTimelineEffectable-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Schnittstelle stellt Methoden zum Hinzufügen von Effekten zu einem Zeitachsenobjekt `IAMTimelineEffectable` in [DirectShow Editing Services](directshow-editing-services.md) (DES) und zum Bearbeiten der Auswirkungen auf ein Objekt bereit. Alle Objekte, auf die Effekte angewendet werden können, implementieren diese Schnittstelle. dazu gehören Quellen, Spuren und Kompositionen.

Ein Objekt, das diese Schnittstelle implementiert, kann eine beliebige Anzahl von Effekten haben. Für jedes Objekt wendet die Render-Engine ihre Effekte in der Reihenfolge ihrer Priorität an, beginnend mit prioritätsebene 0.

## <a name="members"></a>Member

Die **IAMTimelineEffectable-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineEffectable** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineEffectable-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EffectGetCount**](iamtimelineeffectable-effectgetcount.md)             | Ruft die Anzahl der Auswirkungen auf dieses Objekt ab.<br/>                    |
| [**EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)           | Fügt einen Effekt auf der angegebenen Prioritätsebene in das -Objekt ein.<br/> |
| [**EffectSwapPriorities**](iamtimelineeffectable-effectswappriorities.md) | Wechselt die Prioritätsebenen von zwei Effekten.<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | Ruft den Effekt auf der angegebenen Prioritätsebene ab.<br/>              |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
