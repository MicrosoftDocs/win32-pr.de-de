---
description: Die IDxtCompositor-Schnittstelle legt Eigenschaften für den Compositor-Übergang fest. Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der Compositor-Übergang gerendert wird.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: IDxtCompositor-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd59f62a4382ae6023a18792ce3547f67b49c9e8ae49e9de7c9c8409bccd788d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997694"
---
# <a name="idxtcompositor-interface"></a>IDxtCompositor-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IDxtCompositor` -Schnittstelle legt Eigenschaften für den [Compositor-Übergang](compositor-transition.md) fest.

Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der Compositor-Übergang gerendert wird. DES-Anwendungen müssen diese Schnittstelle nicht verwenden. Verwenden Sie zum Festlegen der Eigenschaften für einen Übergang in DES die [**IPropertySetter-Schnittstelle.**](ipropertysetter.md)

Der Compositorübergang zusammengesetzt ein Vordergrundbild zu einem Hintergrundbild. Das *Quellrechteck* definiert den Abschnitt des Vordergrundbilds, das zusammengesetzt ist. Das *Zielrechteck* definiert den Abschnitt des Hintergrundbilds, das das Vordergrundbild empfängt. Das folgende Diagramm veranschaulicht diese Rechtecke.

![Eigenschaften des Compositorübergangs](images/compmeasure.png)

## <a name="members"></a>Member

Die **IDxtCompositor-Schnittstelle** erbt von **IDXEffect.** **IDxtCompositor** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDxtCompositor-Schnittstelle** verfügt über diese Methoden.



| Methode                                                   | Beschreibung                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**Get \_ Height**](idxtcompositor-get-height.md)         | Ruft die Höhe des Zielrechtecks ab.<br/>            |
| [**get \_ OffsetX**](idxtcompositor-get-offsetx.md)       | Ruft den horizontalen Offset des Zielrechtecks ab.<br/> |
| [**get \_ OffsetY**](idxtcompositor-get-offsety.md)       | Ruft den vertikalen Offset des Zielrechtecks ab.<br/>   |
| [**get \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Ruft die Höhe des Quellrechtecks ab.<br/>            |
| [**Get \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Ruft den horizontalen Offset des Quellrechtecks ab.<br/> |
| [**get \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Ruft den vertikalen Offset des Quellrechtecks ab.<br/>   |
| [**get \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Ruft die Breite des Quellrechtecks ab.<br/>             |
| [**get \_ Width**](idxtcompositor-get-width.md)           | Ruft die Breite des Zielrechtecks ab.<br/>             |
| [**Put \_ Height**](idxtcompositor-put-height.md)         | Gibt die Höhe des Zielrechtecks an.<br/>            |
| [**put \_ OffsetX**](idxtcompositor-put-offsetx.md)       | Gibt den horizontalen Offset des Zielrechtecks an.<br/> |
| [**put \_ OffsetY**](idxtcompositor-put-offsety.md)       | Gibt den vertikalen Offset des Zielrechtecks an.<br/>   |
| [**put \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Gibt die Höhe des Quellrechtecks an.<br/>            |
| [**put \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Gibt den horizontalen Offset des Quellrechtecks an.<br/> |
| [**put \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Gibt den vertikalen Offset des Quellrechtecks an.<br/>   |
| [**put \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Gibt die Breite des Quellrechtecks an.<br/>             |
| [**Put \_ Width**](idxtcompositor-put-width.md)           | Gibt die Breite des Zielrechtecks an.<br/>             |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




