---
title: TSMF_SUPPORT_NODEDATA_IN Struktur
description: Wird innerhalb der tsmf- \_ Unterstützungs \_ Daten in der Struktur verwendet \_ , um Informationen zu den unterstützten Medienformaten zu enthalten.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN Struktur Remotedesktopdienste
- PTSMF_SUPPORT_NODEDATA_IN Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338554"
---
# <a name="tsmf_support_nodedata_in-structure"></a>Tsmf \_ unterstützt \_ nodedata \_ in der Struktur

Wird innerhalb der [**tsmf- \_ Unterstützungs \_ Daten \_ in**](tsmf-support-data-in.md) der Struktur verwendet, um Informationen zu den unterstützten Medienformaten zu enthalten.

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

**byteCount**
</dt> <dd>

Die Größe der Struktur in Bytes.

</dd> <dt>

**NodeId**
</dt> <dd>

Der Knoten.

</dd> <dt>

**nummediatypes**
</dt> <dd>

Die Anzahl der Medienformat Strukturen.

</dd> <dt>

**...**
</dt> <dd>

Eine Variable Anzahl von Strukturen, die Audioformate oder Video Medienformate definieren. Der **formatType** ist entweder **Format \_ WaveFormatEx** for Audiodatei oder **Format \_ MF Videoformat** for Video.

Details zu dieser Struktur finden Sie unter [TS \_ am \_ \_ Medientyp Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

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

[**tsmf- \_ Unterstützungs \_ Daten \_ in**](tsmf-support-data-in.md)
</dt> </dl>

 

