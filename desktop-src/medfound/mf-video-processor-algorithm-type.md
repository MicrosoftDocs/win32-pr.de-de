---
description: Definiert Algorithmen für den Videoprozessor, der von dem MF- \_ Video \_ Prozessor Algorithmus verwendet wird \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE-Enumeration
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
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345170"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>\_Typ- \_ \_ \_ Enumeration des MF-Video Prozessors

Definiert Algorithmen für den Videoprozessor, der von dem [MF- \_ Video \_ Prozessor \_ Algorithmus](mf-video-processor-algorithm.md)verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**Standard für den MF- \_ Video \_ Prozessor \_ Algorithmus \_**
</dt> <dd>

der Standardmodus begünstigt eine Ausgewogenheit der Qualität und Geschwindigkeit.

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF- \_ Video \_ Prozessor \_ Algorithmus \_ MRF \_ CRF \_ 444**
</dt> <dd>

Der Videoprozessor wird immer intern in ayuv verarbeitet und verwendet hochwertige Filter.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                              |
| IDL<br/>                      | <dl> <dt>MFI. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




