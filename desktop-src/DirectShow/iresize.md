---
description: 'Die iresize-Schnittstelle muss von jedem benutzerdefinierten Filter zum Ändern der Größe von Videos für DirectShow-Bearbeitungs Dienste unterstützt werden. Um einen benutzerdefinierten Filter für die Größenänderung festzulegen, müssen Sie die IRenderEngine2:: setresizerguid-Methode für die Rendering-Engine aufzurufen.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Iresize-Schnittstelle (qedit. h)
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
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357553"
---
# <a name="iresize-interface"></a>Iresize-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `IResize` Schnittstelle muss von jedem benutzerdefinierten Filter zum Ändern der Größe von Videos für DirectShow-Bearbeitungs Dienste unterstützt werden. Um einen benutzerdefinierten Filter für die Größenänderung festzulegen, müssen Sie die [**IRenderEngine2:: setresizerguid**](irenderengine2-setresizerguid.md) -Methode für die Rendering-Engine aufzurufen.

## <a name="members"></a>Member

Die **iresize** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iresize** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iresize** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**\_inputsize erhalten**](iresize-get-inputsize.md) | Gibt die aktuelle Eingabe Größe des Filter der Größenänderung zurück.<br/>  |
| [**\_mediaType erhalten**](iresize-get-mediatype.md) | Gibt den Typ des Ausgabemediums für die Größe der Größe zurück.<br/>   |
| [**\_Größe erhalten**](iresize-get-size.md)           | Gibt die aktuelle Ausgabegröße und den streckungs Modus zurück.<br/> |
| [**\_mediaType platzieren**](iresize-put-mediatype.md) | Legt den Ausgabe Medientyp fest.<br/>                       |
| [**Put \_ size**](iresize-put-size.md)           | Legt die Ausgabegröße und den streckungs Modus fest.<br/>            |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Bereitstellen eines benutzerdefinierten Videos zum Ändern der Größe](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
