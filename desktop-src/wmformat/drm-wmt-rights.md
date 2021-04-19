---
title: WMT_RIGHTS-Enumeration (wmdrmsdk. h)
description: Definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369356"
---
# <a name="wmt_rights-enumeration"></a>WMT- \_ Rechte Enumeration

Der Enumerationstyp **WMT- \_ Rechte** definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.

## <a name="syntax"></a>Syntax


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT \_ right- \_ Wiedergabe**
</dt> <dd>

Gibt die Berechtigung an, Inhalte ohne Einschränkung wiederzugeben.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT- \_ Rechte \_ Kopie \_ auf nicht- \_ \_ SDMI- \_ Gerät**
</dt> <dd>

Gibt die Berechtigung an, Inhalte auf ein Gerät zu kopieren, das mit der Secure Digital Music Initiative (SDMI) nicht kompatibel ist.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT- \_ Rechte \_ Kopie \_ auf \_ CD**
</dt> <dd>

Gibt die Berechtigung an, Inhalte auf eine CD zu kopieren.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT- \_ Rechte \_ Kopie \_ auf \_ SDMI- \_ Gerät kopieren**
</dt> <dd>

Gibt die Berechtigung an, Inhalte auf ein Gerät zu kopieren, das mit dem SDMI kompatibel ist.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ right \_ einmalig \_**
</dt> <dd>

Gibt die Berechtigung an, den Inhalt nur einmal wiederzugeben.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ right \_ Save \_ Stream \_ Protected**
</dt> <dd>

Gibt die Berechtigung an, Inhalte von einem Server zu speichern.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT- \_ Rechte \_ Kopie**
</dt> <dd>

Gibt die Berechtigung an, Inhalte zu kopieren. Windows Media DRM 10 regelt die Geräte, auf die der Inhalt kopiert werden kann, mithilfe von "Output Protection Levels (opls)".

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ right \_ COLLABORATIVE \_ Play**
</dt> <dd>

Gibt die Berechtigung an, Inhalte als Teil eines Online Szenarios wiederzugeben, in dem mehrere Teilnehmer in einer freigegebenen Wiedergabeliste auf Titel aus Ihrer Sammlung mitwirken können.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT \_ right- \_ SDMI-Auslösung \_**
</dt> <dd>

Für die zukünftige Verwendung reserviert. Darf nicht verwendet werden.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ right \_ SDMI \_ nomorecopies**
</dt> <dd>

Für die zukünftige Verwendung reserviert. Darf nicht verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Werte sind Bitflags, sodass eine oder mehrere festgelegt werden können, indem Sie mit dem bitweisen **or** -Operator kombiniert werden.

Bei der Verwendung von Windows Media DRM 10 werden **WMT- \_ Rechte \_ auf ein nicht- \_ \_ \_ SDMI- \_ Gerät kopiert**, die **WMT-Rechte Kopie auf das \_ \_ \_ \_ SDMI- \_ Gerät** und die **WMT-Rechte Kopie \_ \_ \_ auf \_ CD** ersetzt durch die **WMT- \_ Rechte \_ Kopie**. Einschränkungen auf den Geräten, auf die der Inhalt kopiert werden kann, werden mithilfe von "Output Protection Levels (opls)" angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





