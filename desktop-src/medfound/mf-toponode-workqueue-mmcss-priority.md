---
description: Gibt die relative Threadpriorität für einen Branch der Topologie an.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1b131e6c8b0f379e5e7951498c52f7c0d7a3eab83b75fed4ab9e8100721668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874793"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY-Attribut

Gibt die relative Threadpriorität für einen Branch der Topologie an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Das Attribut ist optional.

Dieses Attribut erfordert die ATTRIBUTE [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) und [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) auf demselben Knoten.

Der Wert des Attributs ist die relative Threadpriorität der Arbeitswarteschlange für diesen Branch der Topologie. Der [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) verwendet die relative Priorität, wenn er die Threadpriorität festlegt. Weitere Informationen finden Sie unter [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Verbesserungen an Arbeitswarteschlangen und Threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MENUWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ ID**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
