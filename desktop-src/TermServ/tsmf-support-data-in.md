---
title: TSMF_SUPPORT_DATA_IN-Struktur
description: Enthält Informationen zu Medienformaten. | TSMF_SUPPORT_DATA_IN-Struktur
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN struktur Remotedesktopdienste
- PTSMF_SUPPORT_DATA_IN Strukturzeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ae90099b69494425344ff65b73090cce574b843cd1589572203a4786b38ff6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755776"
---
# <a name="tsmf_support_data_in-structure"></a>TSMF \_ SUPPORT DATA IN \_ \_ structure

Enthält Informationen zu Medienformaten. Diese Struktur wird von der [**QueryProperty-Methode**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) während **WRDS \_ QUERY MF FORMAT \_ \_ \_ SUPPORT-Abfragen** verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>Member

<dl> <dt>

**guidMfSession**
</dt> <dd>

Die Sitzung.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**\_TSMF-UNTERSTÜTZUNG \_ FÜR NODEDATA \_ IN**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





