---
description: Die Übertragungsmethode des Item-Objekts überträgt Daten von einem Gerät in eine Datei. Diese Methode gilt nur für Gerätetyp Elemente.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Transfer-Methode
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
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347233"
---
# <a name="itemtransfer-method"></a>Item. Transfer-Methode

Die **Übertragungs** Methode des [**Item**](-wia-item.md) -Objekts überträgt Daten von einem Gerät in eine Datei. Diese Methode gilt nur für Gerätetyp Elemente.

## <a name="syntax"></a>Syntax


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Datei an, in die die Daten übertragen werden.

</dd> <dt>

*Asynctransfer* \[ in\]
</dt> <dd>

Typ: **Variant \_ bool**

Ein boolescher Wert, der angibt, ob die Übertragung als asynchroner-Befehl ausgeführt werden soll.

<dt>



 (Variant \_ BOOL


</dt> <dd>

Standard. Legen Sie diesen Wert auf **true** fest, wenn der-Befehl asynchron sein soll (siehe **Hinweise**).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode gilt nur für Dateityp Elemente. Die-Methode überprüft, ob das Element diese Methode unterstützt, bevor versucht wird, die Datenübertragung abzuschließen.

Verwenden Sie "Clipboard" als *filename* -Parameter, um ein Element in die Zwischenablage zu übertragen.

Legen Sie den *asynctransfer* -Wert für Übertragungen innerhalb einer Anwendung oder eines Skripts, die in einer Umgebung ausgeführt wird, die einen Prozess am Ende eines Skripts beendet, z. b. Windows Script Host (WSH), auf **false** fest. Andernfalls kann das Skript beendet werden, und der Prozess wird beendet, bevor die Übertragung abgeschlossen ist.

Die **Übertragungs** Methode weist keinen Rückgabewert auf. Nach Abschluss einer Übertragung sendet diese Methode ein [**ontransfercomplete**](-wia--iwiaevents-ontransfercomplete.md) -Ereignis an das Skript oder die Anwendung.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Übertragungs** Methode zum Übertragen von Daten von einem Gerät veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




