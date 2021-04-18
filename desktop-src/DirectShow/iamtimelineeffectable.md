---
description: Die iamtimelineeffectable-Schnittstelle stellt Methoden zum Hinzufügen von Effekten zu einem Timeline-Objekt in DirectShow-Bearbeitungs Diensten (de) und zum Bearbeiten der Auswirkungen auf ein Objekt bereit.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Iamtimelineeffectable-Schnittstelle (qedit. h)
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
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368537"
---
# <a name="iamtimelineeffectable-interface"></a>Iamtimelineeffectable-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `IAMTimelineEffectable` -Schnittstelle stellt Methoden zum Hinzufügen von Effekten zu einem Timeline-Objekt in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (de) und zum Bearbeiten der Auswirkungen auf ein Objekt bereit. Diese Schnittstelle wird von allen Objekten implementiert, auf die Effekte angewendet werden können. Dies schließt Quellen, Spuren und Kompositionen ein.

Ein Objekt, das diese Schnittstelle implementiert, kann eine beliebige Anzahl von Auswirkungen haben. Die Rendering-Engine wendet die Auswirkungen für jedes Objekt in der Reihenfolge ihrer Priorität an, beginnend mit der Prioritätsstufe 0.

## <a name="members"></a>Member

Die **iamtimelineeffectable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelineeffectable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelineeffectable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                     | BESCHREIBUNG                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Effectgetcount**](iamtimelineeffectable-effectgetcount.md)             | Ruft die Anzahl der Effekte für dieses-Objekt ab.<br/>                    |
| [**Effectinsbefore**](iamtimelineeffectable-effectinsbefore.md)           | Fügt einen Effekt auf der angegebenen Prioritäts Ebene in das-Objekt ein.<br/> |
| [**Effecungwapprioritäten**](iamtimelineeffectable-effectswappriorities.md) | Schaltet die Prioritäts Ebenen von zwei Effekten um.<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | Ruft den Effekt auf der angegebenen Prioritäts Ebene ab.<br/>              |



 

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



 

 
