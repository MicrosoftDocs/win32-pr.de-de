---
description: Ruft den Standardkontingentschwellenwert als Textzeichenfolge ab.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: DiskQuotaControl.DefaultQuotaThresholdText-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8f16c32b46544d3966ae5e3a097576074d28bcfa40ce568cd591d37f9d3d0552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459903"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>DiskQuotaControl.DefaultQuotaThresholdText-Eigenschaft

Ruft den Standardkontingentschwellenwert als Textzeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeichenfolgenwert, der den Standardkontingentschwellenwert für das Volume enthält.

## <a name="remarks"></a>Hinweise

Der Standardkontingentschwellenwert wird automatisch auf neue Benutzer des Volumes angewendet. Wenn die Datenträgerverwendung eines Benutzers diesen Wert überschreitet und die [**LogQuotaThreshold-Eigenschaft**](diskquotacontrol-logquotathreshold.md) auf **TRUE** festgelegt ist, generiert das System einen Ereignisprotokolleintrag. Wenn der Standardschwellenwert beispielsweise 10,0 MB beträgt, ist der Wert der Eigenschaft "10,0 MB". Wenn das Volume über keinen Standardschwellenwert verfügt, wird die -Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




