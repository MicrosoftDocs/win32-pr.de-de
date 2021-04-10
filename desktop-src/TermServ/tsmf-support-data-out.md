---
title: TSMF_SUPPORT_DATA_OUT Struktur
description: Enthält Informationen zu Medienformaten. | TSMF_SUPPORT_DATA_OUT Struktur
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT Struktur Remotedesktopdienste
- PTSMF_SUPPORT_DATA_OUT Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961322"
---
# <a name="tsmf_support_data_out-structure"></a>Tsmf- \_ Unterstützung der \_ Daten \_ out-Struktur

Enthält Informationen zu Medienformaten. Diese Struktur wird von der [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) -Methode während der **\_ \_ \_ \_ Unterstützung** von Abfragen im wrds-Abfrage-MF-Format verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a>Member

<dl> <dt>

**guidmf Session**
</dt> <dd>

Dies muss mit der **guidmf Session** -Eigenschaft in den entsprechenden [**tsmf- \_ Unterstützungs \_ Daten \_ in**](tsmf-support-data-in.md) Structure übereinstimmen.

</dd> <dt>

**numentries**
</dt> <dd>

Die Anzahl der Strukturen in den Daten variabler Länge.

</dd> <dt>

**...**
</dt> <dd>

Eine Variable Anzahl von Strukturen, die Daten im Medienformat enthalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**tsmf \_ unterstützt \_ nodedata \_**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





