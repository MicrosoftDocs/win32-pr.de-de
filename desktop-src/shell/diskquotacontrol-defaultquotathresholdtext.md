---
description: Ruft den Standard Kontingent Schwellenwert als Text Zeichenfolge ab.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Diskquotacontrol. defaultquotader OLDTEXT-Eigenschaft
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
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128440"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>Diskquotacontrol. defaultquotader OLDTEXT-Eigenschaft

Ruft den Standard Kontingent Schwellenwert als Text Zeichenfolge ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeichen folgen Wert, der den Standard Kontingent Schwellenwert für das Volume enthält.

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

 

 




