---
title: TSMF_SUPPORT_NODEDATA_OUT-Struktur
description: Wird in der TSMF \_ SUPPORT \_ DATA \_ OUT-Struktur verwendet, um Informationen zu unterstützten Medienformaten zu enthalten.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT struktur Remotedesktopdienste
- PTSMF_SUPPORT_NODEDATA_OUT strukturzeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3eb4c515963e13d2a7919c58a6d55ca4b2a7600c429a33516093215b5ac0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869010"
---
# <a name="tsmf_support_nodedata_out-structure"></a>TSMF \_ SUPPORT \_ NODEDATA \_ OUT-Struktur

Wird in der [**TSMF \_ SUPPORT \_ DATA \_ OUT-Struktur**](tsmf-support-data-out.md) verwendet, um Informationen zu unterstützten Medienformaten zu enthalten.

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

**nodeId**
</dt> <dd>

Der Knoten.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Gibt an, ob die vom *clsidNewSink-Parameter* identifizierte Senke unterstützt wird.

Die möglichen Werte sind.

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

**clsidNewSink**
</dt> <dd>

Die Senke, die dem Medientyp zugeordnet ist.

</dd> <dt>

**supportedMediaTypeIndex**
</dt> <dd>

Der nullbasierte Index des Medientyps, der von der Senke unterstützt wird.

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

[**TSMF \_ SUPPORT \_ DATA \_ OUT**](tsmf-support-data-out.md)
</dt> </dl>

 

 





