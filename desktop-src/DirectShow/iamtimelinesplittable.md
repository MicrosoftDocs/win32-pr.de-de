---
description: Die iamtimelinesplicustom-Schnittstelle teilt ein Zeitachsen Objekt in DirectShow-Bearbeitungs Diensten (de). Quellen, Effekte, Übergänge und Spuren implementieren diese Schnittstelle.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Iamtimelinesplicustom-Schnittstelle (qedit. h)
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
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361281"
---
# <a name="iamtimelinesplittable-interface"></a>Iamtimelinesplicustom-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMTimelineSplittable` Schnittstelle teilt ein Zeitachsen Objekt in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (des). Quellen, Effekte, Übergänge und Spuren implementieren diese Schnittstelle.

## <a name="members"></a>Member

Die **iamtimelinesplicustom** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinesplicustom** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinesplicustom** -Schnittstelle verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Splitat**](iamtimelinesplittable-splitat.md)   | Teilt das Objekt zum angegebenen Zeitpunkt.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Teilt das Objekt zum angegebenen Zeitpunkt, angegeben als [**ref-Zeit**](reftime.md) -Wert.<br/> |



 

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



 

 
