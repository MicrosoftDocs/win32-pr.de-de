---
description: Die IDxtAlphaSetter-Schnittstelle legt Eigenschaften für den Alpha-Setter-Effekt fest. Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der Alpha-Setter-Effekt gerendert wird.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: IDxtAlphaSetter-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f1cc4056733dbd0e46639a921da65e5cb2a81f3601fa1ae00624be7d92ddc0e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051930"
---
# <a name="idxtalphasetter-interface"></a>IDxtAlphaSetter-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `IDxtAlphaSetter` -Schnittstelle legt Eigenschaften für den [Alpha-Setter-Effekt](alpha-setter-effect.md) fest.

Diese Schnittstelle wird intern von DirectShow Editing Services (DES) verwendet, wenn der Alpha-Setter-Effekt gerendert wird. DES-Anwendungen müssen diese Schnittstelle nicht verwenden. Verwenden Sie zum Festlegen der Eigenschaften für einen Übergang in DES die [**IPropertySetter-Schnittstelle.**](ipropertysetter.md)

## <a name="members"></a>Member

Die **IDxtAlphaSetter-Schnittstelle** erbt von **IDXEffect**. **IDxtAlphaSetter** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDxtAlphaSetter-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**Alpha \_ erhalten**](idxtalphasetter-get-alpha.md)         | Ruft den Alphawert für das gesamte Bild ab.<br/> |
| [**\_AlphaRamp erhalten**](idxtalphasetter-get-alpharamp.md) | Ruft die Alpha-Rampeneigenschaft ab.<br/>              |
| [**put \_ Alpha**](idxtalphasetter-put-alpha.md)         | Gibt den Alphawert für das gesamte Bild an.<br/> |
| [**put \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Gibt die Alpha-Rampeneigenschaft an.<br/>              |



 

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



 

 




