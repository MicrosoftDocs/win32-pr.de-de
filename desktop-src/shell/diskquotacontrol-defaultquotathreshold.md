---
description: Legt den Standardkontingentschwellenwert fest oder ruft sie ab.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: DiskQuotaControl.DefaultQuotaThreshold-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 46d44f2e2df24c5ee1cbf646643810e09d007eb15ba6c9a352eb492dfb104752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943110"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>DiskQuotaControl.DefaultQuotaThreshold-Eigenschaft

Legt den Standardkontingentschwellenwert fest oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Eigenschaftswert

Ein **ganzzahliger** Wert, der für neue Benutzer auf den Standardmäßigen Warnungsschwellenwert in Bytes festgelegt ist.

## <a name="remarks"></a>Hinweise

Der Standardkontingentschwellenwert wird automatisch auf neue Benutzer des Volumes angewendet. Wenn die Datenträgerverwendung eines Benutzers diesen Wert überschreitet und die [**LogQuotaThreshold-Eigenschaft**](diskquotacontrol-logquotathreshold.md) auf **TRUE** festgelegt ist, generiert das System einen Ereignisprotokolleintrag. Wenn der Standardschwellenwert beispielsweise 10,0 MB beträgt, ist der Wert der Eigenschaft "10,0 MB". Wenn das Volume über keinen Standardschwellenwert verfügt, wird die -Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




