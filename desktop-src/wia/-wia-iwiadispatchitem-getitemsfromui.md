---
description: Die getitemsfromui-Methode des Item-Objekts zeigt ein Dialogfeld an, in dem ein Benutzer Bilder und Audiodaten auswählen kann, die von einem Gerät übertragen werden sollen.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. getitemsfromui-Methode
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
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130020"
---
# <a name="itemgetitemsfromui-method"></a>Item. getitemsfromui-Methode

Die **getitemsfromui** -Methode des [**Item**](-wia-item.md) -Objekts zeigt ein Dialogfeld an, in dem ein Benutzer Bilder und Audiodaten auswählen kann, die von einem Gerät übertragen werden sollen.

## <a name="syntax"></a>Syntax


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **wiaflag**](-wia-wiaflag.md)**

<dt>



  (0)


</dt> <dd>

Standard. \[in \] gibt das Dialogfeld Verhalten an. Die gültigen Werte für diesen Parameter sind identisch mit denen für den *lFlags* -Parameter der [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) -Methode.

</dd> </dl> </dd> <dt>

*Absicht* \[ in\]
</dt> <dd>

Typ: **wiaintent**

<dt>



  (0)


</dt> <dd>

Standard. \[in \] gibt an, welche Art von Daten das Image darstellen soll. Eine Liste der Abbild Intent-Werte finden Sie unter [**Bild beabsichtigte Konstanten**](-wia-imageintentconstants.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **ICollection**

Diese Methode gibt eine Auflistung von [**Element**](-wia-item.md) Objekten zurück, die die vom Benutzer ausgewählten Elemente darstellen. Wenn keine Elemente ausgewählt sind, ist die Auflistung leer.

## <a name="remarks"></a>Bemerkungen

Fügen Sie für Microsoft Visual Basic-Anwendungen einen Verweis auf die Typbibliothek "Windows-Abbild Erfassung 1,01" hinzu.

Diese Methode gilt nur für Geräte (Stamm Elemente). Die-Methode gibt eine Auflistung von [**Element**](-wia-item.md) Objekten zurück, die die vom Benutzer ausgewählten Bilder oder Audioclips darstellen.

Wenn vom Benutzer keine Elemente ausgewählt werden, gibt die Methode eine leere Auflistung zurück.

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht die Verwendung der **getitemsfromui** -Methode, um Benutzern das Auswählen von Bildern aus einem Dialogfeld zu ermöglichen.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




