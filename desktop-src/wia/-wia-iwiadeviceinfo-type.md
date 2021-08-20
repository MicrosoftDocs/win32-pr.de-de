---
description: Ruft den Typ des WIA-Hardwaregeräts (Windows Image Acquisition) ab.
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo.Type-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 841ba87b71f79d1f9dfbf85053d914315f89f592ec16a50bd9f6baf061b989a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118035501"
---
# <a name="deviceinfotype-property"></a>DeviceInfo.Type-Eigenschaft

Ruft den Typ des WIA-Hardwaregeräts (Windows Image Acquisition) ab. Mögliche Werte:

-   DigitalCamera
-   Scanner
-   StreamingVideo
-   Standard

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a>Eigenschaftswert

Zeichenfolge, die das Gerät empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




