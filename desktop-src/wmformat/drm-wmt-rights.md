---
title: WMT_RIGHTS -Enumeration (Wmdrmsdk.h)
description: Definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS enumeration windows Media Format
- Enumerationsfenster-Medienformat
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
ms.openlocfilehash: 3a48c9ce3a276f060ac90dd15100ca8612e35116e124588e27f4ee36c1a0b8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930740"
---
# <a name="wmt_rights-enumeration"></a>WMT \_ RIGHTS-Enumeration

Der **WMT \_ RIGHTS-Enumerationstyp** definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.

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

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT \_ RIGHT \_ PLAYBACK**
</dt> <dd>

Gibt das Recht an, Inhalte ohne Einschränkung wiedergibt.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT \_ RIGHT \_ COPY \_ TO \_ NON \_ SDMI \_ DEVICE**
</dt> <dd>

Gibt das Recht an, Inhalte auf ein Gerät zu kopieren, das nicht mit der Secure Digital Musik Initiative (SDMI) kompatibel ist.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT \_ RIGHT \_ COPY \_ TO \_ CD**
</dt> <dd>

Gibt das Recht an, Inhalt auf eine CD zu kopieren.

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT \_ RIGHT \_ COPY \_ TO \_ SDMI \_ DEVICE**
</dt> <dd>

Gibt das Recht an, Inhalte auf ein Gerät zu kopieren, das mit dem SDMI kompatibel ist.

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ RIGHT \_ EINMAL \_**
</dt> <dd>

Gibt das Recht an, Inhalte nur einmal wiedergibt.

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ RIGHT \_ SAVE \_ STREAM \_ PROTECTED**
</dt> <dd>

Gibt das Recht an, Inhalte von einem Server zu speichern.

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT \_ RIGHT \_ COPY**
</dt> <dd>

Gibt das Recht zum Kopieren von Inhalt an. Windows Media DRM 10 reguliert die Geräte, auf die der Inhalt mithilfe von Ausgabeschutzebenen (Output Protection Levels, OPLs) kopiert werden kann.

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ RIGHT \_ COLLABORATIVE \_ PLAY**
</dt> <dd>

Gibt das Recht an, Inhalte als Teil eines Onlineszenarios wiedergibt, in dem mehrere Teilnehmer Titel aus ihrer Sammlung zu einer freigegebenen Wiedergabeliste beitragen können.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT \_ RIGHT \_ SDMI \_ TRIGGER**
</dt> <dd>

Für die zukünftige Verwendung reserviert. Darf nicht verwendet werden.

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ RIGHT \_ SDMI \_ NOMORECOPIES**
</dt> <dd>

Für die zukünftige Verwendung reserviert. Darf nicht verwendet werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Werte sind Bitflags, sodass mindestens ein Flag festgelegt werden kann, indem sie mit dem bitweise **OR-Operator kombiniert** werden.

Bei Verwendung Windows Media DRM 10 werden **WMT \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI \_ DEVICE**, **WMT RIGHT COPY TO \_ \_ \_ \_ SDMI \_ DEVICE** und **WMT RIGHT COPY TO \_ \_ \_ \_ CD** durch **WMT RIGHT \_ \_ COPY** ersetzt. Einschränkungen für die Geräte, auf die der Inhalt kopiert werden kann, werden mithilfe von Ausgabeschutzebenen (Output Protection Levels, OPLs) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





