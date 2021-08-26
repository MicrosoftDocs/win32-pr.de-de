---
description: Die IAMTimelineSplittable-Schnittstelle teilt ein Zeitachsenobjekt in DirectShow Editing Services (DES) auf. Quellen, Effekte, Übergänge und Spuren implementieren diese Schnittstelle.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: IAMTimelineSplittable-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd9f3ca6b1bdea5f80c117b869163d9a2375d5b434765b5962c6216795dd9e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078970"
---
# <a name="iamtimelinesplittable-interface"></a>IAMTimelineSplittable-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IAMTimelineSplittable` Schnittstelle teilt ein Zeitachsenobjekt in [DirectShow Editing Services](directshow-editing-services.md) (DES) auf. Quellen, Effekte, Übergänge und Spuren implementieren diese Schnittstelle.

## <a name="members"></a>Member

Die **IAMTimelineSplittable-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineSplittable** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineSplittable-Schnittstelle** verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Teilt das -Objekt zum angegebenen Zeitpunkt auf.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Teilt das -Objekt zum angegebenen Zeitpunkt, angegeben als [**REFTIME-Wert.**](reftime.md)<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
