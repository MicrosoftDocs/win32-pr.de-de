---
description: Legt den Standard Kontingent Schwellenwert fest oder ruft ihn ab.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Diskquotacontrol. defaultquotathreshold (Eigenschaft)
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
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977193"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>Diskquotacontrol. defaultquotathreshold (Eigenschaft)

Legt den Standard Kontingent Schwellenwert fest oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Eigenschaftswert

Ein **ganzzahliger** Wert, der auf den Standard Warnungs Schwellenwert für neue Benutzer in Bytes festgelegt wird.

## <a name="remarks"></a>Bemerkungen

Der Standard Schwellenwert für Kontingente wird automatisch auf neue Benutzer des Volumes angewendet. Wenn die Datenträger Nutzung eines Benutzers diesen Wert überschreitet und die [**logquotathreshold**](diskquotacontrol-logquotathreshold.md) -Eigenschaft auf **true** festgelegt ist, generiert das System einen Ereignisprotokoll Eintrag. Wenn der Standard Schwellenwert z. b. 10,0 MB beträgt, lautet der Wert der Eigenschaft "10,0 MB". Wenn für das Volume kein Standard Schwellenwert festgelegt ist, wird die-Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol**](diskquotacontrol-object.md)
</dt> </dl>

 

 




