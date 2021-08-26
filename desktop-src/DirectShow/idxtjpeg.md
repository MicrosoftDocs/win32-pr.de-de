---
description: Die IDxtJpeg-Schnittstelle legt Eigenschaften für den SMPTE-Zurücksetzungsübergang fest. Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der SMPTE-Zurücksetzungsübergang gerendert wird.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: IDxtJpeg-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b1f48ff04c087c0c0c391eaf1a64ae8e7768505a5ba8d108ab49c54ffc7b17f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997500"
---
# <a name="idxtjpeg-interface"></a>IDxtJpeg-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IDxtJpeg` -Schnittstelle legt Eigenschaften für den [SMPTE-Zurücksetzungsübergang](smpte-wipe-transition.md) fest.

Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der SMPTE-Zurücksetzungsübergang gerendert wird. DES-Anwendungen müssen diese Schnittstelle nicht verwenden. Verwenden Sie zum Festlegen der Eigenschaften für einen Übergang in DES die [**IPropertySetter-Schnittstelle.**](ipropertysetter.md)

## <a name="members"></a>Member

Die **IDxtJpeg-Schnittstelle** erbt von **IDXEffect**. **IDxtJpeg** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDxtJpeg-Schnittstelle** verfügt über diese Methoden.



| Methode                                                     | Beschreibung                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Applychanges**](idxtjpeg-applychanges.md)              | Wendet alle Eigenschaften an, die geändert wurden.<br/>                                      |
| [**Get \_ BorderColor**](idxtjpeg-get-bordercolor.md)       | Ruft die Farbe des Rahmens um die Ränder des Zurücksetzungsmusters ab.<br/>        |
| [**Get \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Ruft die Breite des unscharfen Bereich um die Ränder des Zurücksetzungsmusters ab.<br/> |
| [**Get \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Ruft die Breite des Vollbildrands entlang der Ränder des Zurücksetzungsmusters ab.<br/>   |
| [**get \_ MaskName**](idxtjpeg-get-maskname.md)             | Ruft den Namen einer JPEG-Datei ab, die als Zurücksetzungsmaske verwendet werden soll.<br/>                 |
| [**get \_ MaskNum**](idxtjpeg-get-masknum.md)               | Ruft den SMPTE-Zurücksetzungscode der Zurücksetzung ab.<br/>                                     |
| [**get \_ OffsetX**](idxtjpeg-get-offsetx.md)               | Ruft den horizontalen Offset des Zurücksetzungsabdrucks ab.<br/>                            |
| [**get \_ OffsetY**](idxtjpeg-get-offsety.md)               | Ruft den vertikalen Offset des Zurücksetzungsstarts ab.<br/>                              |
| [**Get \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Ruft ab, wie oft das Zurücksetzungsmuster horizontal repliziert wird.<br/>     |
| [**Get \_ Replicatey**](idxtjpeg-get-replicatey.md)         | Ruft ab, wie oft das Zurücksetzungsmuster vertikal repliziert wird.<br/>       |
| [**Get \_ ScaleX**](idxtjpeg-get-scalex.md)                 | Ruft den Betrag ab, um den die Zurücksetzung horizontal gestreckt wird.<br/>              |
| [**Get \_ ScaleY**](idxtjpeg-get-scaley.md)                 | Ruft den Betrag ab, um den die Zurücksetzung vertikal gestreckt wird.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Stellt die Standardeinstellungen des Zurücksetzen-Übergangs wieder auf.<br/>                          |
| [**Put \_ BorderColor**](idxtjpeg-put-bordercolor.md)       | Gibt die Farbe des Rahmens um die Ränder des Zurücksetzungsmusters an.<br/>        |
| [**Put \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Gibt die Breite des unscharfen Bereich um die Ränder des Zurücksetzungsmusters an.<br/> |
| [**Put \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Gibt die Breite des Vollbildrands entlang der Ränder des Zurücksetzungsmusters an.<br/>   |
| [**put \_ MaskName**](idxtjpeg-put-maskname.md)             | Gibt den Namen einer JPEG-Datei an, die als Zurücksetzungsmaske verwendet werden soll.<br/>                     |
| [**put \_ MaskNum**](idxtjpeg-put-masknum.md)               | Gibt den SMPTE-Zurücksetzungscode des Zurücksetzungscodes an.<br/>                                     |
| [**put \_ OffsetX**](idxtjpeg-put-offsetx.md)               | Gibt den horizontalen Offset des Zurücksetzungsabdrucks an.<br/>                            |
| [**put \_ OffsetY**](idxtjpeg-put-offsety.md)               | Gibt den vertikalen Offset des Zurücksetzungsstarts an.<br/>                              |
| [**Put \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Gibt an, wie oft das Zurücksetzungsmuster horizontal repliziert wird.<br/>     |
| [**Put \_ ReplicateY**](idxtjpeg-put-replicatey.md)         | Gibt an, wie oft das Zurücksetzungsmuster vertikal repliziert wird.<br/>       |
| [**Put \_ ScaleX**](idxtjpeg-put-scalex.md)                 | Gibt den Betrag an, um den die Zurücksetzung horizontal gestreckt wird.<br/>              |
| [**Put \_ ScaleY**](idxtjpeg-put-scaley.md)                 | Gibt den Betrag an, um den die Zurücksetzung vertikal gestreckt wird.<br/>                |



 

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



 

 




