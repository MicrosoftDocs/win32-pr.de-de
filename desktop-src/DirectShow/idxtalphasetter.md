---
description: Die idxtalphasetter-Schnittstelle legt Eigenschaften für den Alpha Setter-Effekt fest. Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn Sie den Alpha Setter-Effekt rendert.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Idxtalphasetter-Schnittstelle (qedit. h)
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
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362006"
---
# <a name="idxtalphasetter-interface"></a>Idxtalphasetter-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IDxtAlphaSetter` Schnittstelle legt Eigenschaften für den [Alpha Setter](alpha-setter-effect.md) -Effekt fest.

Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn Sie den Alpha Setter-Effekt rendert. Die-Anwendungen müssen diese Schnittstelle nicht verwenden. Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.

## <a name="members"></a>Member

Die **idxtalphasetter** -Schnittstelle erbt von **idxeffect**. **Idxtalphasetter** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idxtalphasetter** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**\_Alpha**](idxtalphasetter-get-alpha.md)         | Ruft den Alpha-Wert für das gesamte Bild ab.<br/> |
| [**\_alpharamp erhalten**](idxtalphasetter-get-alpharamp.md) | Ruft die Eigenschaft für die Alpha-Eigenschaft ab.<br/>              |
| [**\_Alpha platzieren**](idxtalphasetter-put-alpha.md)         | Gibt den Alpha-Wert für das gesamte Bild an.<br/> |
| [**Put \_ alpharamp**](idxtalphasetter-put-alpharamp.md) | Gibt die Eigenschaft für die Alpha-Eigenschaft an.<br/>              |



 

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



 

 




