---
description: Die iamtimelineeffect-Schnittstelle stellt Methoden zum Bearbeiten von Audio-und Video Effekten in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Iamtimelineeffect-Schnittstelle (qedit. h)
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
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372003"
---
# <a name="iamtimelineeffect-interface"></a>Iamtimelineeffect-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `IAMTimelineEffect` -Schnittstelle stellt Methoden zum Bearbeiten von Audio-und Video Effekten in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit. Einem Zeitachsen Objekt, das die [**iamtimelineeffectable**](iamtimelineeffectable.md) -Schnittstelle verfügbar macht, kann ein Effekt hinzugefügt werden. Um Eigenschaften für einen Effekt festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.

Das des des-Effekts-Objekts ist tatsächlich ein Wrapper für eines von zwei anderen Objekten:

-   Für Audioeffekte ist jeder DirectShow-audiowirkungs Filter.
-   Für Video Effekte und 1-Input-DirectX-Transformations Objekt.

Microsoft unterstützt die Entwicklung von DirectX-Transformations Objekten von Drittanbietern nicht mehr.

Um das Filter-oder DirectX-Transformations Objekt für einen Effekt anzugeben, müssen Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode aufrufen.

Um ein Effect-Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert der Wert Zeitachse des \_ Haupt \_ Typs auf \_ . Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die- `IAMTimelineEffect` Schnittstelle Abfragen.

## <a name="members"></a>Member

Die **iamtimelineeffect** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelineeffect** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelineeffect** -Schnittstelle verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**Effectgetpriority**](iamtimelineeffect-effectgetpriority.md) | Ruft die Prioritäts Ebene des Effekts ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
