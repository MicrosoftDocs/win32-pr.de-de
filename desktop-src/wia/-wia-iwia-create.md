---
description: Die Create-Methode des WIA-Objekts stellt eine Verbindung mit dem angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein Element Objekt zurück, das das Gerät darstellt.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: WIA. Create-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529150"
---
# <a name="wiacreate-method"></a>WIA. Create-Methode

Die **Create** -Methode des [**WIA**](-wia-wia.md) -Objekts stellt eine Verbindung mit dem angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gerät* \[ in\]
</dt> <dd>

Typ: **Variant \** _

Gibt das WIA-Gerät an, mit dem eine Verbindung hergestellt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: _ *iwiadispatchitem**

Bei erfolgreicher Ausführung gibt diese Methode ein [**Element**](-wia-item.md) Objekt zurück, das ein WIA-Hardware Gerät (ein Stamm Element) darstellt.

## <a name="remarks"></a>Bemerkungen

Der *Geräte* Parameter gibt ein Objekt vom Typ " [**toviceinfo**](-wia-deviceinfo.md) " an, indem das Objekt selbst, dessen Index von einem Auflistungs Objekt oder der Wert der [**ID**](-wia-iwiadeviceinfo-id.md) -Eigenschaft übergeben wird. Übergeben Sie **nichts** , um ein Dialogfeld anzuzeigen, das einem Benutzer ermöglicht, ein Gerät auszuwählen.

## <a name="examples"></a>Beispiele

Die folgenden VBScript-Beispiele veranschaulichen die Verwendung der **Create** -Methode.

Im ersten Beispiel wird ein [**deviceInfo**](-wia-deviceinfo.md) -Objekt an die **Create** -Methode übergeben. Beachten Sie, dass das übergeben der [**ID**](-wia-iwiadeviceinfo-id.md) -Eigenschaft des Objekts genau dasselbe Verhalten bewirkt.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



Im nächsten Beispiel übergibt die aufrufenden Anwendung den Index des [**deviceInfo**](-wia-deviceinfo.md) -Objekts in der-Auflistung an die **Create** -Methode.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



Das nächste Beispiel übergibt **nichts** an die **Create** -Methode, um ein Dialogfeld anzuzeigen, in dem ein Benutzer ein Gerät auswählen kann.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




