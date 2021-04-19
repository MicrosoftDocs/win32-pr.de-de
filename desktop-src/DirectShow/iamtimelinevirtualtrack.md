---
description: Die iamtimelinevirtualtrack-Schnittstelle stellt Methoden für das Arbeiten mit virtuellen Spuren in DirectShow-Bearbeitungs Diensten (de) bereit. Komposition und Spuren unterstützen diese Schnittstelle.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Iamtimelinevirtualtrack-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370662"
---
# <a name="iamtimelinevirtualtrack-interface"></a>Iamtimelinevirtualtrack-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMTimelineVirtualTrack` Schnittstelle stellt Methoden zum Arbeiten mit virtuellen Spuren in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit. Komposition und Spuren unterstützen diese Schnittstelle.

## <a name="members"></a>Member

Die **iamtimelinevirtualtrack** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinevirtualtrack** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinevirtualtrack** -Schnittstelle verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [**Settrackdirty**](iamtimelinevirtualtrack-settrackdirty.md)       | Wird nicht unterstützt.<br/>                         |
| [**Trackgetpriority**](iamtimelinevirtualtrack-trackgetpriority.md) | Ruft die Prioritäts Ebene des-Objekts ab.<br/> |



 

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



 

 
