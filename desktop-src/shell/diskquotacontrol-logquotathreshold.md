---
description: Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingentschwellenwert überschreitet.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: DiskQuotaControl.LogQuotaThreshold-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bb2a2073a791fcbb8e5bb6db83480f0fcea52b35e0380c20be730265d5bb34ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090640"
---
# <a name="diskquotacontrollogquotathreshold-property"></a>DiskQuotaControl.LogQuotaThreshold-Eigenschaft

Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingentschwellenwert überschreitet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird auf **TRUE** festgelegt, wenn ein Systemereignisprotokolleintrag erfolgt, wenn der Benutzer seinen Kontingentwarnungsschwellenwert überschreitet, oder andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




