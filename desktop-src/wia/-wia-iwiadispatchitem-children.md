---
description: Die Children-Eigenschaft des Item-Objekts ruft eine Auflistung von Item-Objekten ab. Die Elemente in dieser Auflistung stellen Elemente dar, die direkte untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind. Schreibgeschützt.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item.Children-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 72ce5119a10adc6a902d5a675d3ec116a3db1852a88e47ed852284cf44edf2f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440729"
---
# <a name="itemchildren-property"></a>Item.Children-Eigenschaft

Die **Children-Eigenschaft** des [**Item-Objekts**](-wia-item.md) ruft eine Auflistung von **Item-Objekten** ab. Die Elemente in dieser Auflistung stellen Elemente dar, die direkte untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind. Schreibgeschützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Eigenschaftswert

Variable, die die -Objekte empfängt.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaft, um in der hierarchischen Struktur von [**Item-Objekten**](-wia-item.md) zu navigieren, die ein Gerät darstellen, den Ordnern und den Dateien, die sich auf dem Gerät befinden.

Die **Children-Eigenschaft** ist eine Auflistung von [**Item-Objekten**](-wia-item.md) nur von der Ebene direkt unter diesem **Item-Objekt** in der Struktur. Um durch weitere Ebenen in der Struktur zu navigieren, verwenden Sie diese Eigenschaft rekursiv.

Wenn das Element keine untergeordneten Elemente enthalten kann oder nicht enthält, gibt diese Eigenschaft eine leere Auflistung zurück.

> [!Note]  
> Diese Auflistung ist 0-basiert.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Children-Eigenschaft** zum Abrufen und Aufzählen einer Auflistung der untergeordneten Elemente eines Geräts veranschaulicht. Wenn es sich bei dem Gerät um eine Digitalkamera handelt, enthält die Sammlung in der Regel Ordner- und Bildelemente. Wenn es sich bei dem Gerät um einen Scanner handelt, enthält die Sammlung in der Regel Elemente, die scannt.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




