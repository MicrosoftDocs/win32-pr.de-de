---
description: Wird mit IOCTL \_ SCSI \_ Miniport ioctl und dem ctlcode \_ iscsitgt \_ SPT \_ Session \_ End (0x101)-Steuerungs Code verwendet, um eine Sitzung zu beenden.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: ISCSITGT_SPT_SESSION_STOP Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103869672"
---
# <a name="iscsitgt_spt_session_stop-structure"></a>Struktur der iscsitgt \_ SPT- \_ Sitzungs \_ Beendigung

\[Die folgende Struktur ist für die Verwendung in Windows Server 2012 R2 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Wird mit [**IOCTL \_ SCSI \_ Miniport**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) ioctl und dem ctlcode \_ iscsitgt \_ SPT \_ Session \_ End (0x101)-Steuerungs Code verwendet, um eine Sitzung zu beenden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a>Member

<dl> <dt>

**Header**
</dt> <dd>

Obligatorischer Header.

</dd> <dt>

**Itnexushandle**
</dt> <dd>

Ein undurchsichtiges handle, das eine Sitzung darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                               |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[iSCSI-Ziel-Pass-Through](/powershell/module/iscsi)
</dt> <dt>

[**SRB \_ IO- \_ Steuerelement**](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
