---
description: Der Typ dieses Elements. Schreibgeschützt.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Item.ItemType-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3cbf60c935a88a62786c7c516ec0e768d65019c02d4419c44d928cee704a67b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450780"
---
# <a name="itemitemtype-property"></a>Item.ItemType-Eigenschaft

Der Typ dieses Elements. Schreibgeschützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a>Eigenschaftswert

Folgende Werte sind möglich:



| Wert  | BESCHREIBUNG                                     |
|--------|-------------------------------------------------|
| device | Das Element ist ein WIA-Hardwaregerät.              |
| folder | Das Element ist ein Ordner, der andere Elemente enthält. |
| file   | Das Element ist eine Bild- oder Audiodatei.             |
| Audio  | Das Element ist ein Audioclip.                      |
| image  | Das Element ist ein Bild.                           |



 

## <a name="remarks"></a>Hinweise

Ein Element kann mehrere Typen haben. Beispielsweise ist jedes Bild sowohl vom Typ "image" als auch vom Typ "file". **ItemType** gibt eine Zeichenfolge zurück, die alle gültigen Typen für das Element enthält, getrennt durch Semikolons. Beispiel: "image;file". In dieser Zeichenfolge sind keine Leerzeichen und am Ende kein Semikolon enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




