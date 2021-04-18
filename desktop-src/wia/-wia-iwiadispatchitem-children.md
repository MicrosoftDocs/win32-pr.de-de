---
description: Die Children-Eigenschaft des Item-Objekts Ruft eine Auflistung von Element Objekten ab. Die Elemente in dieser Auflistung stellen Elemente dar, die direkt untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind. Schreibgeschützt.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item. Children-Eigenschaft
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
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345159"
---
# <a name="itemchildren-property"></a>Item. Children-Eigenschaft

Die **Children** -Eigenschaft des [**Item**](-wia-item.md) -Objekts Ruft eine Auflistung von **Element** Objekten ab. Die Elemente in dieser Auflistung stellen Elemente dar, die direkt untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind. Schreibgeschützt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Item.Children
```



## <a name="property-value"></a>Eigenschaftswert

Variable, die die-Objekte empfängt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um in der hierarchischen Struktur von [**Element**](-wia-item.md) Objekten, die ein Gerät darstellen, die Ordner und Dateien, die sich auf dem Gerät befinden, zu navigieren.

Die **Children** -Eigenschaft ist eine Auflistung von [**Item**](-wia-item.md) -Objekten, die sich nur von der Ebene direkt unterhalb dieses **Element** Objekts in der Struktur befindet. Verwenden Sie diese Eigenschaft rekursiv, um weitere Ebenen in der Struktur zu navigieren.

Wenn das Element über keine untergeordneten Elemente verfügt oder keine untergeordneten Elemente enthält, gibt diese Eigenschaft eine leere Auflistung zurück.

> [!Note]  
> Diese Auflistung ist 0-basiert.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Children** -Eigenschaft zum Abrufen und Auflisten einer Auflistung der untergeordneten Elemente eines Geräts veranschaulicht. Wenn das Gerät eine digitale Kamera ist, enthält die Sammlung normalerweise Ordner-und Bildelemente. Wenn es sich bei dem Gerät um einen Scanner handelt, enthält die Sammlung in der Regel Elemente, die das Scannen von Betten


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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




