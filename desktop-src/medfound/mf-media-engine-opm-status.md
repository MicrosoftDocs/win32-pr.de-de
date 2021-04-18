---
description: Definiert den Status des Output Protection Managers (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: MF_MEDIA_ENGINE_OPM_STATUS-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361119"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>\_ \_ \_ OPM- \_ Status Enumeration für MF-Medien-Engine

Definiert den Status des [Output Protection Managers](output-protection-manager.md) (OPM).

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**Das MF \_ Media \_ Engine \_ OPM wurde \_ nicht \_ angefordert.**
</dt> <dd>

Standardstatus. Wird verwendet, um den korrekten Status zurückzugeben, wenn der Inhalt nicht geschützt ist.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**OPM der MF- \_ Medien- \_ Engine \_ \_ eingerichtet**
</dt> <dd>

OPM wurde erfolgreich eingerichtet.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**Fehler beim virtuellen Computer der MF- \_ Medien- \_ Engine \_ OPM \_ \_**
</dt> <dd>

OPM ist fehlgeschlagen, weil die Ausführung in einer virtuellen Maschine (VM) ausgeführt wurde.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**Fehler \_ beim \_ \_ BM der \_ MF-Medien-Engine-Fehler \_**
</dt> <dd>

OPM ist fehlgeschlagen, da es keinen Grafiktreiber gibt und das System den Basic Display Adapter (BDA) verwendet.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF-Medien-Engine-Fehler bei \_ \_ \_ \_ \_ nicht signiertem \_ Treiber**
</dt> <dd>

OPM ist fehlgeschlagen, da der Grafiktreiber nicht mit PE signiert ist und auf den Warp zurückfällt.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**Fehler \_ beim \_ \_ OPM der MF-Medien-Engine \_**
</dt> <dd>

OPM konnte aus anderen Gründen nicht ausgeführt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




