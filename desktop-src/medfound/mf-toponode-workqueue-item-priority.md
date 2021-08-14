---
description: Gibt die Arbeitselementpriorität für einen Branch der Topologie an.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff67e48bda6ac00baeab9418b80d366c23808713b4689a013949b364f09b6e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739834"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ ITEM \_ PRIORITY-Attribut

Gibt die Arbeitselementpriorität für einen Branch der Topologie an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Quellknoten (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Das Attribut ist optional.

Für dieses Attribut ist das [MF \_ TOPONODE \_ WORKQUEUE \_ ID-Attribut](mf-toponode-workqueue-id-attribute.md) auf demselben Knoten erforderlich.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> <dt>

[Verbesserungen bei Arbeitswarteschlangen und Threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**TOPOLOGIENode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**REGISTRWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ \_ MF-TOPONODE-WORKQUEUE-ID \_**](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




