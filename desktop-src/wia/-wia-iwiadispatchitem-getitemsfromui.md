---
description: Die GetItemsFromUI-Methode des Item-Objekts zeigt ein Dialogfeld an, in dem benutzer Bilder und Audiodaten auswählen können, die von einem Gerät übertragen werden sollen.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item.GetItemsFromUI-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a954dbefec9728d2d6f595144ba3991ab4f7b3a1ded77fdf7e3ca5407be70d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669712"
---
# <a name="itemgetitemsfromui-method"></a>Item.GetItemsFromUI-Methode

Die **GetItemsFromUI-Methode** des [**Item-Objekts**](-wia-item.md) zeigt ein Dialogfeld an, in dem benutzer Bilder und Audiodaten auswählen können, die von einem Gerät übertragen werden sollen.

## <a name="syntax"></a>Syntax


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **WiaFlag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

Standard. \[in \] Gibt das Verhalten des Dialogfelds an. Die gültigen Werte für diesen Parameter sind die gleichen wie für den *lFlags-Parameter* der [**DeviceDlg-Methode.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)

</dd> </dl> </dd> <dt>

*Absicht* \[ In\]
</dt> <dd>

Typ: **WiaIntent**

<dt>



  (0)


</dt> <dd>

Standard. \[in \] Gibt an, welche Art von Daten das Bild darstellen soll. Eine Liste der Bildabsichtswerte finden Sie unter [**Image Intent Constants**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **ICollection**

Diese Methode gibt eine Auflistung von [**Item-Objekten**](-wia-item.md) zurück, die die vom Benutzer ausgewählten Elemente darstellen. Wenn keine Elemente ausgewählt sind, ist die Auflistung leer.

## <a name="remarks"></a>Hinweise

Fügen Sie Visual Basic Microsoft-Anwendungen einen Verweis auf "Windows Image Acquisition 1.01 Type Library" hinzu.

Diese Methode gilt nur für Geräte (Stammelemente). Die -Methode gibt eine Auflistung von [**Item-Objekten**](-wia-item.md) zurück, die die vom Benutzer ausgewählten Bilder oder Audioclips darstellen.

Wenn vom Benutzer keine Elemente ausgewählt werden, gibt die Methode eine leere Auflistung zurück.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **GetItemsFromUI-Methode** veranschaulicht, mit der ein Benutzer Bilder aus einem Dialogfeld auswählen kann.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




