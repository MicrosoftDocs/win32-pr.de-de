---
description: Die idxtjpeg-Schnittstelle legt Eigenschaften für den SMPTE-zurücksetzen-Übergang fest. Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten (de) verwendet, wenn Sie den Übergang der SMPTE-Löschung rendert.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Idxtjpeg-Schnittstelle (qedit. h)
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
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351278"
---
# <a name="idxtjpeg-interface"></a>Idxtjpeg-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IDxtJpeg` Schnittstelle legt Eigenschaften für den [SMPTE](smpte-wipe-transition.md) -zurücksetzen-Übergang fest.

Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten (de) verwendet, wenn Sie den Übergang der SMPTE-Löschung rendert. Die-Anwendungen müssen diese Schnittstelle nicht verwenden. Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.

## <a name="members"></a>Member

Die **idxtjpeg** -Schnittstelle erbt von **idxeffect**. **Idxtjpeg** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idxtjpeg** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ApplyChanges**](idxtjpeg-applychanges.md)              | Wendet alle geänderten Eigenschaften an.<br/>                                      |
| [**\_BorderColor erhalten**](idxtjpeg-get-bordercolor.md)       | Ruft die Farbe des Rahmens um die Ränder des Entwurfsmusters ab.<br/>        |
| [**\_borderweichheit erhalten**](idxtjpeg-get-bordersoftness.md) | Ruft die Breite des unscharf-Bereichs um die Ränder des-tokenmusters ab.<br/> |
| [**\_BorderWidth erhalten**](idxtjpeg-get-borderwidth.md)       | Ruft die Breite des vollständigen Rahmens entlang der Kanten des Abbild Musters ab.<br/>   |
| [**\_maskname erhalten**](idxtjpeg-get-maskname.md)             | Ruft den Namen einer JPEG-Datei ab, die als abzurufende Maske verwendet werden soll.<br/>                 |
| [**\_masknum-**](idxtjpeg-get-masknum.md)               | Ruft den SMPTE-Code zum Löschen der Löschung ab.<br/>                                     |
| [**\_OffsetX erhalten**](idxtjpeg-get-offsetx.md)               | Ruft den horizontalen Offset des Ursprungs zum Löschen ab.<br/>                            |
| [**\_offität abrufen**](idxtjpeg-get-offsety.md)               | Ruft den vertikalen Offset des Ursprungs zum Löschen ab.<br/>                              |
| [**\_Repli-Ex repliholen**](idxtjpeg-get-replicatex.md)         | Ruft ab, wie oft das Abbild der Löschung horizontal repliziert wird.<br/>     |
| [**\_replierhalten**](idxtjpeg-get-replicatey.md)         | Ruft die Häufigkeit ab, mit der das Muster für das Löschen vertikal repliziert wird.<br/>       |
| [**\_ScaleX erhalten**](idxtjpeg-get-scalex.md)                 | Ruft den Betrag ab, um den das Löschen horizontal gestreckt wird.<br/>              |
| [**get \_ ScaleY**](idxtjpeg-get-scaley.md)                 | Ruft den Betrag ab, um den das Löschen vertikal gestreckt wird.<br/>                |
| [**Loaddefsettings**](idxtjpeg-loaddefsettings.md)        | Stellt die Standardeinstellungen des Übergangs Übergangs wieder her.<br/>                          |
| [**\_BorderColor platzieren**](idxtjpeg-put-bordercolor.md)       | Gibt die Farbe des Rahmens um die Ränder des-Token für das Löschen an.<br/>        |
| [**\_borderweichheit platzieren**](idxtjpeg-put-bordersoftness.md) | Gibt die Breite des unscharf-Bereichs um die Ränder des Abbild Musters an.<br/> |
| [**\_BorderWidth platzieren**](idxtjpeg-put-borderwidth.md)       | Gibt die Breite des vollständigen Rahmens entlang der Kanten des Abbild Musters an.<br/>   |
| [**Put \_ maskname**](idxtjpeg-put-maskname.md)             | Gibt den Namen einer JPEG-Datei an, die als abzurufende Maske verwendet werden soll.<br/>                     |
| [**\_masknum platzieren**](idxtjpeg-put-masknum.md)               | Gibt den SMPTE-Code zum Löschen der Löschung an.<br/>                                     |
| [**\_OffsetX ablegen**](idxtjpeg-put-offsetx.md)               | Gibt den horizontalen Offset des Ursprungs für das Löschen an.<br/>                            |
| [**Put \_ offty**](idxtjpeg-put-offsety.md)               | Gibt den vertikalen Offset des Ursprungs für das Löschen an.<br/>                              |
| [**\_Repli-Ex platzieren**](idxtjpeg-put-replicatex.md)         | Gibt an, wie oft das Muster für die Löschung horizontal repliziert wird.<br/>     |
| [**versetzen von \_ Repli|**](idxtjpeg-put-replicatey.md)         | Gibt an, wie oft das Muster für die Löschung vertikal repliziert wird.<br/>       |
| [**\_ScaleX platzieren**](idxtjpeg-put-scalex.md)                 | Gibt den Betrag an, um den das Löschen horizontal gestreckt wird.<br/>              |
| [**\_skaley platzieren**](idxtjpeg-put-scaley.md)                 | Gibt den Betrag an, um den das Löschen vertikal gestreckt wird.<br/>                |



 

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



 

 




