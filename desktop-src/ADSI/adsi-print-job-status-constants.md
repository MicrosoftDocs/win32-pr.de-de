---
title: ADSI Print Job-Status Konstanten (adssts. h)
description: Die folgenden Konstanten werden mit der iadsprintjoboperations. Status-Eigenschaft verwendet, um den Status eines Druckauftrags anzugeben.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956914"
---
# <a name="adsi-print-job-status-constants"></a>Status Konstanten für den ADSI-Druckauftrag

Die folgenden Konstanten werden mit der [**iadsprintjoboperations. Status**](iadsprintjoboperations-property-methods.md) -Eigenschaft verwendet, um den Status eines Druckauftrags anzugeben.

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**Werbe \_ Auftrag \_ angehalten**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Der Druckauftrag wurde angehalten.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS- \_ Auftrags \_ Fehler**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Ein Fehler ist aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**Löschen eines ADS \_ \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Der Druckauftrag wird gelöscht.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_ \_ Spoolvorgang für Werbeaufträge**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Der Druckauftrag wird gespoolte.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**Drucken von Werbe Aufträgen \_ \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Der Druckauftrag wird gedruckt.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS- \_ Auftrag \_ Offline**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Der Drucker ist offline.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_ \_ Taschenbuch der Werbe Einblendung**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Der Drucker ist nicht mehr im Papier.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**Werbe \_ Auftrag \_ gedruckt**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Der Druckauftrag wurde gedruckt.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**ADS- \_ Auftrag \_ gelöscht**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Der Druckauftrag wurde gelöscht.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Adssts. h</dt> </dl> |



 

 





