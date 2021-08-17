---
description: Die GetPropById-Methode des DeviceInfo-Objekts verwendet die ID einer Geräteeigenschaft, um ihren Wert zurück zu geben.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo.GetPropById-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: c996989661703c4a9c7416cd63904c376fdb7fcca3071d4558551bdd78470d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208786"
---
# <a name="deviceinfogetpropbyid-method"></a>DeviceInfo.GetPropById-Methode

Die **GetPropById-Methode** des [**DeviceInfo-Objekts**](-wia-deviceinfo.md) verwendet die ID einer Geräteeigenschaft, um ihren Wert zurück zu geben.

## <a name="syntax"></a>Syntax


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Typ: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**

Gibt die ID der Eigenschaft an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **VARIANT**

Diese Methode gibt den Wert der durch id angegebenen *Eigenschaft zurück.*

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um den Wert einer Geräteeigenschaft aus ihrer ID zu suchen. Eine Liste der Eigenschaften-IDs finden Sie unter [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md). Informationen zu den wia Windows(Wia)-Eigenschaften finden Sie unter [WIA-Eigenschaftenkonst constants (WIA-Eigenschaftenkonst constants).](-wia-wia-property-constants.md)

Fügen Sie Visual Basic Microsoft-Anwendungen einen Verweis auf "Windows Image Acquisition 1.01 Type Library" hinzu. Die folgenden konstanten, in dieser Datei definierten Konstanten sind für diese Methode gültig:

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **GetPropById-Methode** zum Abrufen eines Eigenschaftswerts veranschaulicht.


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




