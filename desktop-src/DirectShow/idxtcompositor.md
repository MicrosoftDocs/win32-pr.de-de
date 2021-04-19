---
description: Die idxtcompositor-Schnittstelle legt Eigenschaften für den compositorübergang fest. Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn der compositorübergang gerendert wird.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Idxtcompositor-Schnittstelle (qedit. h)
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
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356032"
---
# <a name="idxtcompositor-interface"></a>Idxtcompositor-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IDxtCompositor` Schnittstelle legt Eigenschaften für den [compositorübergang](compositor-transition.md) fest.

Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn der compositorübergang gerendert wird. Die-Anwendungen müssen diese Schnittstelle nicht verwenden. Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.

Der Compositor-Übergang setzt ein Vordergrundbild auf ein Hintergrundbild zusammen. Das *Quell Rechteck* definiert den Abschnitt des Vordergrund Bilds, das zusammengesetzt ist. Das *Ziel Rechteck* definiert den Abschnitt des Hintergrund Bilds, das das Vordergrundbild empfängt. Das folgende Diagramm veranschaulicht diese Rechtecke.

![Eigenschaften des compositorübergangs](images/compmeasure.png)

## <a name="members"></a>Member

Die **idxtcompositor** -Schnittstelle erbt von **idxeffect**. **Idxtcompositor** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idxtcompositor** -Schnittstelle verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**\_Höhe erhalten**](idxtcompositor-get-height.md)         | Ruft die Höhe des Ziel Rechtecks ab.<br/>            |
| [**\_OffsetX erhalten**](idxtcompositor-get-offsetx.md)       | Ruft den horizontalen Offset des Ziel Rechtecks ab.<br/> |
| [**\_offität abrufen**](idxtcompositor-get-offsety.md)       | Ruft den vertikalen Offset des Ziel Rechtecks ab.<br/>   |
| [**\_srcHeight erhalten**](idxtcompositor-get-srcheight.md)   | Ruft die Höhe des Quell Rechtecks ab.<br/>            |
| [**\_srcoffsetx erhalten**](idxtcompositor-get-srcoffsetx.md) | Ruft den horizontalen Offset des Quell Rechtecks ab.<br/> |
| [**\_srcoff-Ty abrufen**](idxtcompositor-get-srcoffsety.md) | Ruft den vertikalen Offset des Quell Rechtecks ab.<br/>   |
| [**\_srcWidth erhalten**](idxtcompositor-get-srcwidth.md)     | Ruft die Breite des Quell Rechtecks ab.<br/>             |
| [**\_Breite erhalten**](idxtcompositor-get-width.md)           | Ruft die Breite des Ziel Rechtecks ab.<br/>             |
| [**\_Höhe ablegen**](idxtcompositor-put-height.md)         | Gibt die Höhe des Ziel Rechtecks an.<br/>            |
| [**\_OffsetX ablegen**](idxtcompositor-put-offsetx.md)       | Gibt den horizontalen Offset des Ziel Rechtecks an.<br/> |
| [**Put \_ offty**](idxtcompositor-put-offsety.md)       | Gibt den vertikalen Offset des Ziel Rechtecks an.<br/>   |
| [**\_srcHeight platzieren**](idxtcompositor-put-srcheight.md)   | Gibt die Höhe des Quell Rechtecks an.<br/>            |
| [**\_srcoffsetx platzieren**](idxtcompositor-put-srcoffsetx.md) | Gibt den horizontalen Offset des Quell Rechtecks an.<br/> |
| [**\_srcoff-Ty platzieren**](idxtcompositor-put-srcoffsety.md) | Gibt den vertikalen Offset des Quell Rechtecks an.<br/>   |
| [**\_srcWidth platzieren**](idxtcompositor-put-srcwidth.md)     | Gibt die Breite des Quell Rechtecks an.<br/>             |
| [**\_Breite platzieren**](idxtcompositor-put-width.md)           | Gibt die Breite des Ziel Rechtecks an.<br/>             |



 

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



 

 




