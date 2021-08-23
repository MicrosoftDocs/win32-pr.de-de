---
description: Legt den Warnungsschwellenwert des Benutzers in Bytes fest oder ruft den Warnungsschwellenwert ab.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: DIDiskQuotaUser.QuotaThreshold-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 38caa5ef5ded6ed40708314c6063fba13a74cbbe506465aed55e8504898a9307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032788"
---
# <a name="didiskquotauserquotathreshold-property"></a>DIDiskQuotaUser.QuotaThreshold-Eigenschaft

Legt den Warnungsschwellenwert des Benutzers in Bytes fest oder ruft den Warnungsschwellenwert ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a>Eigenschaftswert

Ein **Ganzzahlwert,** der den Warnungsschwellenwert des Benutzers angibt oder empfängt. Wenn die Datenträgerverwendung eines Benutzers diesen Wert überschreitet und die [**LogQuotaThreshold-Eigenschaft**](diskquotacontrol-logquotathreshold.md) auf **TRUE** festgelegt ist, generiert das System einen Ereignisprotokolleintrag.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




