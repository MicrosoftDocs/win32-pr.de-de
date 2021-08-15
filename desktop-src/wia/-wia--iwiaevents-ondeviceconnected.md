---
description: Das Ereignis tritt auf, wenn ein Windows WIA-Hardwaregerät (Image Acquisition) verbunden ist.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Wia.OnDeviceConnected-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d878cc663cc9f7ea1422e2dc2cad10e652296a48ef597cf699fe5eb3af99e49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209547"
---
# <a name="wiaondeviceconnected-event"></a>Wia.OnDeviceConnected-Ereignis

Das Ereignis tritt auf, wenn ein Windows WIA-Hardwaregerät (Image Acquisition) verbunden ist.

## <a name="syntax"></a>Syntax


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Eine Zeichenfolge, die die ID des verbundenen Geräts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

WIA benachrichtigt das Skript oder die Anwendung, wenn ein neues Hardwaregerät mit dem Computer verbunden ist. Implementieren Sie **die Unterroutine objWia** \_ **OnDeviceConnected(),** damit das Skript oder die Anwendung auf die Geräteverbindung reagieren kann.

Sie möchten beispielsweise, dass ein Skript die [**Gerätesammlung**](-wia-iwia-devices.md) aktualisiert, wenn ein neues Gerät installiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




