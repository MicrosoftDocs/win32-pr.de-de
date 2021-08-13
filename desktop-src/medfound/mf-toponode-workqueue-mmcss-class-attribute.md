---
description: Gibt einen MMCSS-Task (Multimedia Class Scheduler Service) für eine Topologieverzweigung an.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: MF_TOPONODE_WORKQUEUE_MMCSS_CLASS-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6630cf22d3afe270b2a032304fd9de3118e73e75e28da4116418894271237a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739844"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS-Attribut

Gibt einen [MMCSS-Task (Multimedia Class Scheduler Service)](../procthread/multimedia-class-scheduler-service.md) für eine Topologieverzweigung an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Dieses Attribut ist optional.

Dieses Attribut erfordert das [MF \_ TOPONODE \_ WORKQUEUE \_ ID-Attribut.](mf-toponode-workqueue-id-attribute.md) Wenn Sie dieses Attribut festlegen, legen Sie auch fest, dass das **MF \_ TOPONODE \_ WORKQUEUE \_ ID-Attribut** auf demselben Knoten festgelegt ist.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**MENUWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ ID**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Arbeitswarteschlangen](work-queues.md)
</dt> </dl>

 

 
