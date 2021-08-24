---
description: Die Transfer-Methode des Item-Objekts überträgt Daten von einem Gerät in eine Datei. Diese Methode gilt nur für Gerätetypelemente.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item.Transfer-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: efef054a324244553748b75659820f582100a01ed6f56f9a2f80b0ef0c08f105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706320"
---
# <a name="itemtransfer-method"></a>Item.Transfer-Methode

Die **Transfer-Methode** des [**Item-Objekts**](-wia-item.md) überträgt Daten von einem Gerät in eine Datei. Diese Methode gilt nur für Gerätetypelemente.

## <a name="syntax"></a>Syntax


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Datei an, in die die Daten übertragen werden.

</dd> <dt>

*AsyncTransfer* \[ In\]
</dt> <dd>

Typ: **VARIANT \_ BOOL**

Ein boolescher Wert, der angibt, ob die Übertragung als asynchroner Aufruf ausgeführt werden soll.

<dt>



 (VARIANT \_ BOOL)


</dt> <dd>

Standard. Legen Sie diesen Wert auf **TRUE** fest, wenn der Aufruf asynchron sein soll (siehe **Hinweise**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode gilt nur für Dateitypelemente. Die -Methode überprüft, ob das Element diese Methode unterstützt, bevor versucht wird, die Datenübertragung abzuschließen.

Verwenden Sie die Zwischenablage als *Filename-Parameter,* um ein Element in die Zwischenablage zu übertragen.

Legen Sie den *AsyncTransfer-Wert* für Übertragungen innerhalb einer Anwendung oder eines Skripts, die in einer Umgebung ausgeführt werden, die einen Prozess am Ende eines Skripts beendet, wie z. B. Windows Script Host (WSH), auf **FALSE** fest. Andernfalls kann das Skript beendet und der Prozess beendet werden, bevor die Übertragung abgeschlossen wird.

Die **Transfer-Methode** hat keinen Rückgabewert. Nach Abschluss einer Übertragung sendet diese Methode ein [**OnTransferComplete-Ereignis**](-wia--iwiaevents-ontransfercomplete.md) an das Skript oder die Anwendung.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Transfer-Methode** zum Übertragen von Daten von einem Gerät veranschaulicht.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
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



 

 




