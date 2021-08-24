---
description: Die IDxtKey-Schnittstelle legt Eigenschaften für den Schlüsselübergang fest. Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der Schlüsselübergang gerendert wird.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: IDxtKey-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d967d15dededf879ffd08671aac00e7892aa8ad2f2c1a39ce478f7f9f3e4db90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792360"
---
# <a name="idxtkey-interface"></a>IDxtKey-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IDxtKey` -Schnittstelle legt Eigenschaften für den [Schlüsselübergang](key-transition.md) fest.

Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der Schlüsselübergang gerendert wird. DES-Anwendungen müssen diese Schnittstelle nicht verwenden. Verwenden Sie die [**IPropertySetter-Schnittstelle,**](ipropertysetter.md) um die Eigenschaften für einen Übergang in DES festzulegen.

## <a name="members"></a>Member

Die **IDxtKey-Schnittstelle erbt** von **IDXEffect.** **IDxtKey** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDxtKey-Schnittstelle** verfügt über diese Methoden.



| Methode                                            | Beschreibung                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**\_Get Hue**](idxtkey-get-hue.md)               | Ruft den Farbtonwert ab, für den die Taste geschaltet werden soll.<br/>                                    |
| [**get \_ Invert**](idxtkey-get-invert.md)         | Ruft einen booleschen Wert ab, der angibt, ob der Schlüsselvorgang invertiert ist.<br/> |
| [**\_get KeyType**](idxtkey-get-keytype.md)       | Ruft den Typ des Schlüssels ab.<br/>                                                  |
| [**get \_ Luminance**](idxtkey-get-luminance.md)   | Ruft den Leuchtdichtewert ab, für den die Taste aktiviert werden soll.<br/>                              |
| [**get \_ RGB**](idxtkey-get-rgb.md)               | Ruft die RGB-Farbe ab, für die ein Schlüssel angezeigt werden soll.<br/>                                    |
| [**get \_ Similarity (Ähnlichkeit abrufen)**](idxtkey-get-similarity.md) | Ruft den Bereich der Farbdaten ab, der transparent wird.<br/>                 |
| [**put \_ Hue**](idxtkey-put-hue.md)               | Gibt den Farbtonwert an, für den die Taste festgelegt werden soll.<br/>                                    |
| [**put \_ Invert**](idxtkey-put-invert.md)         | Gibt an, ob der Schlüsselvorgang invertiert wird.<br/>                            |
| [**\_put KeyType**](idxtkey-put-keytype.md)       | Gibt den Typ des Schlüssels an.<br/>                                                  |
| [**put \_ Luminance**](idxtkey-put-luminance.md)   | Gibt den Leuchtdichtewert an, für den ein Schlüssel festgelegt werden soll.<br/>                              |
| [**put \_ RGB**](idxtkey-put-rgb.md)               | Gibt die RGB-Farbe an, für die die Taste festgelegt werden soll.<br/>                                    |
| [**put \_ Similarity**](idxtkey-put-similarity.md) | Gibt den Bereich von Farbdaten an, der transparent wird.<br/>                 |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




