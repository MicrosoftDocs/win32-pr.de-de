---
description: Ruft einen booleschen Wert ab, der angibt, ob die Kontingentdatei für das Volume gerade neu erstellt wird.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: DiskQuotaControl.QuotaFileRebuilding (Eigenschaft)
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
ms.openlocfilehash: 8e90d5d920392b9b518fed619aeb4f8c7b99d830fad9f6f901c59fe6128ca94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710520"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>DiskQuotaControl.QuotaFileRebuilding (Eigenschaft)

Ruft einen booleschen Wert ab, der angibt, ob die Kontingentdatei für das Volume gerade neu erstellt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft wird auf **TRUE festgelegt,** wenn die Kontingentdatei neu erstellt wird, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Die Kontingentdatei wird automatisch neu erstellt, wenn Kontingente auf dem System aktiviert sind oder wenn mindestens ein Benutzereintrag zum Löschen markiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




