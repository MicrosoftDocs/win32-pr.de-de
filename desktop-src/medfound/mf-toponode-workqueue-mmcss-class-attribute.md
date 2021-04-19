---
description: Gibt eine MMCSS-Aufgabe (Multimedia Class Scheduler Service) für eine topologieverzweigung an.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: MF_TOPONODE_WORKQUEUE_MMCSS_CLASS-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353144"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a>\_ \_ \_ MMCSS- \_ Klassen Attribut für MF toponode workqueue

Gibt eine MMCSS-Aufgabe ( [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) ) für eine topologieverzweigung an.

## <a name="data-type"></a>Datentyp

Breitzeichenfolge

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Quellknoten (**MF- \_ Topologie \_ sourcestream- \_ Knoten**). Dieses Attribut ist optional.

Dieses Attribut erfordert das [MF- \_ toponode- \_ workqueue- \_ ID](mf-toponode-workqueue-id-attribute.md) -Attribut. Wenn Sie dieses Attribut festlegen, legen Sie außerdem fest, dass das **MF- \_ toponode- \_ workqueue- \_ ID** -Attribut auf dem gleichen Knoten festgelegt ist.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMF workqueueservices:: beginregistertopologyworkqueueswithmmcss**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF- \_ toponode- \_ workwarteschlangen- \_ ID**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Arbeits Warteschlangen](work-queues.md)
</dt> </dl>

 

 
