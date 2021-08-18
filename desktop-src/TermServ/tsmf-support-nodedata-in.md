---
title: TSMF_SUPPORT_NODEDATA_IN-Struktur
description: Wird in der TSMF \_ SUPPORT \_ DATA \_ IN-Struktur verwendet, um Informationen zu unterstützten Medienformaten zu enthalten.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN strukturieren Remotedesktopdienste
- PTSMF_SUPPORT_NODEDATA_IN Strukturzeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e1920ca627a7da8aef2d49a6930b03f0906cfd912e2a2a584b20d8e8382b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755722"
---
# <a name="tsmf_support_nodedata_in-structure"></a>TSMF \_ SUPPORT \_ NODEDATA IN \_ structure

Wird in der [**TSMF \_ SUPPORT \_ DATA \_ IN-Struktur verwendet,**](tsmf-support-data-in.md) um Informationen zu unterstützten Medienformaten zu enthalten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a>Member

<dl> <dt>

**Bytecount**
</dt> <dd>

Die Größe der Struktur in Bytes.

</dd> <dt>

**nodeId**
</dt> <dd>

Der Knoten.

</dd> <dt>

**numMediaTypes**
</dt> <dd>

Die Anzahl der Medienformatstrukturen.

</dd> <dt>

**...**
</dt> <dd>

Eine variable Anzahl von Strukturen, die Audio- oder Videomedienformate definieren. **FormatType ist** entweder **FORMAT \_ WaveFormatEx für** Audio oder FORMAT **\_ MFVideoFormat** für Video.

Weitere Informationen zu dieser Struktur finden Sie unter [TS AM MEDIA TYPE \_ \_ \_ Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

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

[**\_TSMF-UNTERSTÜTZUNGSDATEN \_ \_ IN**](tsmf-support-data-in.md)
</dt> </dl>

 

