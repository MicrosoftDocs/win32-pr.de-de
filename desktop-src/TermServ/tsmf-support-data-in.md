---
title: TSMF_SUPPORT_DATA_IN Struktur
description: Enthält Informationen zu Medienformaten. | TSMF_SUPPORT_DATA_IN Struktur
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN Struktur Remotedesktopdienste
- PTSMF_SUPPORT_DATA_IN Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371855"
---
# <a name="tsmf_support_data_in-structure"></a>Tsmf- \_ Unterstützungs \_ Daten \_ in der Struktur

Enthält Informationen zu Medienformaten. Diese Struktur wird von der [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) -Methode während der **\_ \_ \_ \_ Unterstützung** von Abfragen im wrds-Abfrage-MF-Format verwendet.

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

**guidmf Session**
</dt> <dd>

Die Sitzung.

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

[**tsmf \_ unterstützt \_ nodedata \_ in**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





