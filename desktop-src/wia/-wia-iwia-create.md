---
description: Die Create-Methode des Wia-Objekts stellt eine Verbindung mit dem angegebenen WIA-Gerät (Windows Image Acquisition) und gibt ein Item-Objekt zurück, das das Gerät darstellt.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Wia.Create-Methode
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
ms.openlocfilehash: a4056354992010d3d213ed619b7460e12c800630ca38fb17acb6d7677fe842a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814050"
---
# <a name="wiacreate-method"></a>Wia.Create-Methode

Die **Create-Methode** des [**Wia-Objekts**](-wia-wia.md) stellt eine Verbindung mit dem angegebenen WIA-Gerät (Windows Image Acquisition) und gibt ein [**Item-Objekt**](-wia-item.md) zurück, das das Gerät darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gerät* \[ In\]
</dt> <dd>

Typ: **\* VARIANT**

Gibt das WIA-Gerät an, mit dem eine Verbindung hergestellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **IWiaDispatchItem**

Bei Erfolg gibt diese Methode ein [**Item-Objekt**](-wia-item.md) zurück, das ein WIA-Hardwaregerät (ein Stammelement) darstellt.

## <a name="remarks"></a>Hinweise

Der *Device-Parameter* gibt ein [**DeviceInfo-Objekt**](-wia-deviceinfo.md) an, indem er das Objekt selbst, seinen Index aus einem Sammlungsobjekt oder den Wert seiner [**ID-Eigenschaft**](-wia-iwiadeviceinfo-id.md) übergibt. Keine **übergeben,** um ein Dialogfeld anzuzeigen, in dem ein Benutzer ein Gerät auswählen kann.

## <a name="examples"></a>Beispiele

Die folgenden VBScript-Beispiele veranschaulichen die Verwendung der **Create-Methode.**

Im ersten Beispiel wird ein [**DeviceInfo-Objekt**](-wia-deviceinfo.md) an die **Create-Methode** übergibt. Beachten Sie, dass die Übergabe der [**ID-Eigenschaft des**](-wia-iwiadeviceinfo-id.md) Objekts genau das gleiche Verhalten verursacht.


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



Im nächsten Beispiel übergibt die aufrufende Anwendung den Index des [**DeviceInfo-Objekts**](-wia-deviceinfo.md) in der Auflistung an die **Create-Methode.**


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



Im nächsten Beispiel wird **Nothing an die** **Create-Methode übergibt,** um ein Dialogfeld anzuzeigen, in dem ein Benutzer ein Gerät auswählen kann.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




