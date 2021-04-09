---
description: Gibt die relative Thread Priorität für eine Verzweigung der Topologie an.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130136"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>\_ \_ \_ MMCSS- \_ Prioritäts Attribut für MF toponode workqueue

Gibt die relative Thread Priorität für eine Verzweigung der Topologie an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**). Das-Attribut ist optional.

Dieses Attribut erfordert die [MF \_ toponode \_ workqueue- \_ ID](mf-toponode-workqueue-id-attribute.md) -und die [MF \_ toponode \_ workqueue- \_ MMCSS- \_ Klassen](mf-toponode-workqueue-mmcss-class-attribute.md) Attribute auf dem gleichen Knoten.

Der Wert des-Attributs ist die relative Thread Priorität der Arbeits Warteschlange für diesen Branch der Topologie. Der [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) verwendet beim Festlegen der Thread Priorität die relative Priorität. Weitere Informationen finden Sie unter [**avsetmmthreadpriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Arbeits Warteschlangen und Threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMF workqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF- \_ toponode- \_ workwarteschlangen- \_ ID**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
