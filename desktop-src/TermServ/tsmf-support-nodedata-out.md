---
title: TSMF_SUPPORT_NODEDATA_OUT Struktur
description: Wird innerhalb der tsmf- \_ Unterstützung der \_ Datenausgabe Struktur verwendet \_ , um Informationen zu unterstützten Medienformaten zu enthalten.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT Struktur Remotedesktopdienste
- PTSMF_SUPPORT_NODEDATA_OUT Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859028"
---
# <a name="tsmf_support_nodedata_out-structure"></a>Tsmf \_ unterstützt \_ nodedata- \_ out-Struktur

Wird innerhalb der [**tsmf- \_ Unterstützung der \_ Daten \_**](tsmf-support-data-out.md) Ausgabestruktur verwendet, um Informationen zu unterstützten Medienformaten zu enthalten.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a>Member

<dl> <dt>

**NodeId**
</dt> <dd>

Der Knoten.

</dd> <dt>

**hrsupportstatus**
</dt> <dd>

Gibt an, ob die durch den *clsidnewsink* -Parameter identifizierte Senke unterstützt wird.

Mögliche Werte sind.

<dt>

0
</dt> <dd>

Nicht unterstützt

</dd> <dt>

1
</dt> <dd>

Unterstützt

</dd> </dl>

Andere Werte sind nicht definiert.

</dd> <dt>

**clsidnewsink**
</dt> <dd>

Die Senke, die dem Medientyp zugeordnet ist.

</dd> <dt>

**supportedmediatypeingedex**
</dt> <dd>

Der null basierte Index des Medientyps, der von der Senke unterstützt wird.

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

[**tsmf- \_ Unterstützung \_ \_ von Daten**](tsmf-support-data-out.md)
</dt> </dl>

 

 





