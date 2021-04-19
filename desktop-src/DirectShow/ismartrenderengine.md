---
description: Die ismartrenderengine-Schnittstelle stellt Methoden bereit, die eine intelligente Neukomprimierung in DirectShow-Bearbeitungs Diensten unterstützen. Diese Schnittstelle wird von der intelligenten Rendering-Engine
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Ismartrenderengine-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370058"
---
# <a name="ismartrenderengine-interface"></a>Ismartrenderengine-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `ISmartRenderEngine` Schnittstelle stellt Methoden bereit, die eine intelligente Neukomprimierung in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) unterstützen. Diese Schnittstelle wird von der intelligenten Rendering-Engine

## <a name="members"></a>Member

Die **ismartrenderengine** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ismartrenderengine** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ismartrenderengine** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Getgroupcompressor**](ismartrenderengine-getgroupcompressor.md)   | Ruft den Komprimierungs Filter für die angegebene Gruppe ab.<br/>                 |
| [**Setfindcompressorcb**](ismartrenderengine-setfindcompressorcb.md) | Nicht implementiert.<br/>                                                          |
| [**Setgroupcompressor**](ismartrenderengine-setgroupcompressor.md)   | Gibt einen Komprimierungs Filter an, der beim Rendern der angegebenen Gruppe verwendet werden soll.<br/> |



 

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

[Rendern eines Projekts](rendering-a-project.md)
</dt> </dl>

 

 
