---
title: TSMF_SUPPORT_DATA_OUT-Struktur
description: Enthält Informationen zu Medienformaten. | TSMF_SUPPORT_DATA_OUT-Struktur
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT struktur Remotedesktopdienste
- PTSMF_SUPPORT_DATA_OUT Strukturzeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8577266c2e259e7a7e4bb70310837eee1d743905e0e0d166e5797bc51a1f1b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869020"
---
# <a name="tsmf_support_data_out-structure"></a>TSMF \_ SUPPORT \_ DATA \_ OUT-Struktur

Enthält Informationen zu Medienformaten. Diese Struktur wird von der [**QueryProperty-Methode**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) während **WRDS \_ QUERY MF FORMAT \_ \_ \_ SUPPORT-Abfragen** verwendet.

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

**guidMfSession**
</dt> <dd>

Dies muss mit der **guidMfSession-Eigenschaft** in der entsprechenden [**TSMF \_ SUPPORT DATA \_ \_ IN-Struktur**](tsmf-support-data-in.md) übereinstimmen.

</dd> <dt>

**num-Einträge**
</dt> <dd>

Die Anzahl der Strukturen in den Daten variabler Länge.

</dd> <dt>

**...**
</dt> <dd>

Eine variable Anzahl von Strukturen, die Medienformatdaten enthalten.

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

[**TSMF \_ SUPPORT \_ NODEDATA \_ OUT**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





