---
description: Definiert den Status des Ausgabeschutz-Managers (Output Protection Manager, OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: MF_MEDIA_ENGINE_OPM_STATUS Enumeration
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
ms.openlocfilehash: 98efb0054402f8bf019e91d639f16322a1378a23dfeee76cd31daea9d12bf6fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013040"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>MF \_ MEDIA \_ ENGINE \_ OPM \_ STATUS-Enumeration

Definiert den Status des [Ausgabeschutz-Managers](output-protection-manager.md) (Output Protection Manager, OPM).

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

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF \_ MEDIA \_ ENGINE \_ OPM NICHT \_ \_ ANGEFORDERT**
</dt> <dd>

Standardstatus. Wird verwendet, um den richtigen Status zurück zu geben, wenn der Inhalt nicht geschützt ist.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ EINGERICHTET**
</dt> <dd>

OPM erfolgreich eingerichtet.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**FEHLERHAFTER VIRTUELLER COMPUTER \_ DER MF-MEDIEN-ENGINE \_ \_ \_ \_**
</dt> <dd>

OpM failed because running in a virtual machined (VM) (OPM failed because running in a virtual machined (VM)) (OPM-Fehler aufgrund der Ausführung auf einem virtuellen Computer

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**Fehler beim BDA der \_ MF-MEDIEN-ENGINE-OPM \_ \_ \_ \_**
</dt> <dd>

Fehler bei OPM, weil kein Grafiktreiber vorgeist und das System den Standardanzeigeadapter (Basic Display Adapter, BDA) verwendet.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF \_ MEDIA \_ ENGINE \_ OPM \_ FAILED \_ UNSIGNED \_ DRIVER**
</dt> <dd>

OpM failed because the graphics driver is not PE signed, fall back to WARP. (OPM ist fehlgeschlagen, weil der Grafiktreiber nicht PE-signiert ist und auf WARP zurückfällt.)

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**Fehler bei \_ \_ MF-MEDIEN-ENGINE-OPM \_ \_**
</dt> <dd>

OpM ist aus anderen Gründen fehlgeschlagen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




