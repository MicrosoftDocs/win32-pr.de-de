---
description: Ruft einen booleschen Wert ab, der angibt, ob die Kontingent Datei für das Volume gerade neu erstellt wird.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Diskquotacontrol. quotafilerebuilding (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977504"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>Diskquotacontrol. quotafilerebuilding (Eigenschaft)

Ruft einen booleschen Wert ab, der angibt, ob die Kontingent Datei für das Volume gerade neu erstellt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird auf **true** festgelegt, wenn die Kontingent Datei neu erstellt wird, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Die Kontingent Datei wird automatisch neu erstellt, wenn Kontingente auf dem System aktiviert sind oder wenn mindestens ein Benutzereintrag zum Löschen markiert ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




