---
title: WM_BACKUP_RESTORE_STATUS Struktur (wmdrmsdk. h)
description: Die Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_ enthält Informationen zu einem ausstehenden Lizenz Sicherungs-oder Wiederherstellungs Vorgang.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- WM_BACKUP_RESTORE_STATUS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365730"
---
# <a name="wm_backup_restore_status-structure"></a>Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_

Die **Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_** enthält Informationen zu einem ausstehenden Lizenz Sicherungs-oder Wiederherstellungs Vorgang.

## <a name="syntax"></a>Syntax


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**estatus**
</dt> <dd>

Member der [**msdrm- \_ statusenumeration**](msdrm-status.md) , die den Status angibt.

</dd> <dt>

**bstrauerror**
</dt> <dd>

Zeichenfolge, die den Fehler enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird empfangen, wenn Sie die [**iwmdrmlicencbackuprestorestatus:: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) -Methode aufrufen. Sie enthält den Status des ausstehenden Sicherungs-oder Wiederherstellungs Vorgangs zum Zeitpunkt des Aufrufens.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





