---
description: Der Typ dieses Elements. Schreibgeschützt.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Item. ItemType (Eigenschaft)
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
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351694"
---
# <a name="itemitemtype-property"></a>Item. ItemType (Eigenschaft)

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
| device | Das Element ist ein WIA-Hardware Gerät.              |
| folder | Das Element ist ein Ordner, der andere Elemente enthält. |
| file   | Das Element ist ein Bild oder eine Audiodatei.             |
| Audio  | Das Element ist ein Audioclip.                      |
| image  | Das Element ist ein Bild.                           |



 

## <a name="remarks"></a>Bemerkungen

Ein Element kann über mehr als einen Typ verfügen. Beispielsweise ist jedes Image sowohl vom Typ "Image" als auch vom Typ "file". **ItemType** gibt eine Zeichenfolge zurück, die alle gültigen Typen für das Element enthält, getrennt durch Semikolons. Beispiel: "Image; File". Diese Zeichenfolge enthält keine Leerzeichen, und am Ende ist kein Semikolon vorhanden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




