---
description: Die idxtkey-Schnittstelle legt Eigenschaften für den Schlüssel Übergang fest. Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten verwendet, wenn der Schlüssel Übergang gerendert wird.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Idxtkey-Schnittstelle (qedit. h)
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
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364732"
---
# <a name="idxtkey-interface"></a>Idxtkey-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IDxtKey` Schnittstelle legt Eigenschaften für den [Schlüssel](key-transition.md) Übergang fest.

Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten verwendet, wenn der Schlüssel Übergang gerendert wird. Die-Anwendungen müssen diese Schnittstelle nicht verwenden. Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.

## <a name="members"></a>Member

Die **idxtkey** -Schnittstelle erbt von **idxeffect**. **Idxtkey** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idxtkey** -Schnittstelle verfügt über diese Methoden.



| Methode                                            | BESCHREIBUNG                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**\_Farbton erhalten**](idxtkey-get-hue.md)               | Ruft den Hue-Wert ab, für den der Schlüssel abgerufen werden soll.<br/>                                    |
| [**\_Invertieren**](idxtkey-get-invert.md)         | Ruft einen booleschen Wert ab, der angibt, ob der Schlüssel Vorgang invertiert wird.<br/> |
| [**\_KeyType erhalten**](idxtkey-get-keytype.md)       | Ruft den Typ des Schlüssels ab.<br/>                                                  |
| [**\_Beleuchtung erhalten**](idxtkey-get-luminance.md)   | Ruft den Wert der Leuchtkraft ab, für den der Schlüssel abgerufen werden soll.<br/>                              |
| [**\_RGB erhalten**](idxtkey-get-rgb.md)               | Ruft die RGB-Farbe ab, für die der Schlüssel abgerufen werden soll.<br/>                                    |
| [**\_Ähnlichkeit erhalten**](idxtkey-get-similarity.md) | Ruft den Bereich der Farbdaten ab, der transparent wird.<br/>                 |
| [**\_Farbton ablegen**](idxtkey-put-hue.md)               | Gibt den Farbton Wert an, auf den der Schlüssel festgelegt wird.<br/>                                    |
| [**\_Invert einfügen**](idxtkey-put-invert.md)         | Gibt an, ob der Schlüssel Vorgang invertiert wird.<br/>                            |
| [**\_KeyType platzieren**](idxtkey-put-keytype.md)       | Gibt den Typ des Schlüssels an.<br/>                                                  |
| [**\_Leuchtkraft einfügen**](idxtkey-put-luminance.md)   | Gibt den Wert der Leuchtkraft an, auf den der Schlüssel festgelegt wird<br/>                              |
| [**\_RGB einfügen**](idxtkey-put-rgb.md)               | Gibt die RGB-Farbe für den Schlüssel an.<br/>                                    |
| [**\_Ähnlichkeit**](idxtkey-put-similarity.md) | Gibt den Bereich der Farbdaten an, der transparent wird.<br/>                 |



 

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



 

 




