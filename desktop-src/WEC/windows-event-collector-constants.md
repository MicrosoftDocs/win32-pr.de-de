---
title: Windows-Ereignis Sammler Konstanten (evcoll. h)
description: Das Windows-Ereignis Sammler-SDK enthält die folgenden Konstanten.
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
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739744"
---
# <a name="windows-event-collector-constants"></a>Windows-Ereignis Sammler Konstanten

Das Windows-Ereignis Sammler-SDK enthält die folgenden Konstanten.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ Variant \_ Type \_ Mask**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Wird verwendet, um das arraybit aus der **Type** -Eigenschaft einer [**EC- \_ Variante**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) zu maskieren, um den Typ des Variant-Werts zu extrahieren.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**Type-Array der EC- \_ Variante \_ \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Wenn dieses Bit in der **Type** -Eigenschaft einer EC- [**\_ Variante**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)festgelegt wird, enthält die Variante einen Zeiger auf ein Array von Werten anstatt auf den Wert selbst.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC- \_ Lese \_ Zugriff**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Lese Zugriffs Steuerungs Berechtigung, die das Lesen von Informationen aus dem Ereignis Sammler ermöglicht.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC- \_ Schreib \_ Zugriff**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Berechtigung zum Schreiben der Zugriffs Steuerung, die das Schreiben von Informationen in den Ereignis Sammler ermöglicht.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ \_ immer öffnen**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Öffnet ein vorhandenes Abonnement oder erstellt das Abonnement, wenn es nicht vorhanden ist. Wird von der [**ecopenabonnementmethode**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) verwendet.


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ Create \_ New**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Ein Flag, das an die Funktion [**ecopenabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) übermittelt wird und angibt, dass ein neues Abonnement erstellt werden soll.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ Open \_ vorhanden**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Ein Flag, das an die Funktion [**ecopenabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) übermittelt wird und angibt, dass ein vorhandenes Abonnement geöffnet werden soll.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





