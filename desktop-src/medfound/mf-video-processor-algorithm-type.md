---
description: Definiert Algorithmen für den Videoprozessor, der vom \_ MF-VIDEOPROZESSORALGORITHMUS \_ verwendet \_ wird.
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 885c3e9c34fa787a6877fd37eef81f470be395225594b90b2f5516a8e773eb88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244138"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>TYPE-Enumeration des \_ MF-VIDEOPROZESSORALGORITHMUS \_ \_ \_

Definiert Algorithmen für den Videoprozessor, der vom [ \_ MF-VIDEOPROZESSORALGORITHMUS \_ \_ verwendet wird.](mf-video-processor-algorithm.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**STANDARDEINSTELLUNG FÜR \_ MF-VIDEOPROZESSORALGORITHMUS \_ \_ \_**
</dt> <dd>

Standardmodus bevorzugt ein ausgewogenes Verhältnis von Qualität und Geschwindigkeit

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_MF-VIDEOPROZESSORALGORITHMUS \_ \_ \_ MRF \_ CRF \_ 444**
</dt> <dd>

Der Videoprozessor wird immer intern in AYUV verarbeiten und hochwertige Filter verwenden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                              |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




