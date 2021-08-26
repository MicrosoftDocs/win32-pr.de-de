---
title: Windows Event Collector-Konstanten (Evcoll.h)
description: Das Windows Event Collector SDK enthält die folgenden Konstanten.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d168ecb16c293c524c4dffcb16aee7db2924e23219e42d402939ab26b4bbecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005980"
---
# <a name="windows-event-collector-constants"></a>Windows Event Collector-Konstanten

Das Windows Event Collector SDK enthält die folgenden Konstanten.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ VARIANT \_ TYPE \_ MASK**
</dt> <dd> <dl> <dt>

0x7f
</dt> <dt>



Wird verwendet, um das Arraybit aus der **Type-Eigenschaft** einer [**EC \_ VARIANT-Eigenschaft**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) zu maskieren, um den Typ des Variantwerts zu extrahieren.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC \_ VARIANT \_ TYPE \_ ARRAY**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Wenn dieses Bit in der **Type-Eigenschaft** einer [**EC \_ VARIANT-Eigenschaft**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)festgelegt ist, enthält die Variante einen Zeiger auf ein Array von Werten, anstatt auf den Wert selbst.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_ \_ EC-LESEZUGRIFF**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Lesezugriffssteuerungsberechtigung, mit der Informationen aus dem Ereignissammler gelesen werden können.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_ \_ EC-SCHREIBZUGRIFF**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Schreibzugriffssteuerungsberechtigung, mit der Informationen in den Ereignissammler geschrieben werden können.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ OPEN \_ ALWAYS**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Öffnet ein vorhandenes Abonnement oder erstellt das Abonnement, wenn es nicht vorhanden ist. Wird von der [**EcOpenSubscription-Methode**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) verwendet.


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ CREATE \_ NEW**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Ein Flag, das an die [**EcOpenSubscription-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) übergeben wird, um anzugeben, dass ein neues Abonnement erstellt werden soll.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ OPEN \_ EXISTING**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Ein Flag, das an die [**EcOpenSubscription-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) übergeben wird, um anzugeben, dass ein vorhandenes Abonnement geöffnet werden soll.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Evcoll.h</dt> </dl> |



 

 





