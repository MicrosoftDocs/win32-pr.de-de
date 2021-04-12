---
description: Definiert die Medien Schlüssel-Fehlercodes für die Medien-Engine.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: MF_MEDIA_ENGINE_KEYERR-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351348"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>MF- \_ Medien- \_ Engine \_ keyerr-Enumeration

Definiert die Medien Schlüssel-Fehlercodes für die Medien-Engine.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ mediaengine \_ keyerr \_ unbekannt**
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF \_ mediaengine \_ keyerr- \_ Client**
</dt> <dd>

Fehler beim Client.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF \_ mediaengine \_ keyerr- \_ Dienst**
</dt> <dd>

Fehler beim Dienst.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF \_ mediaengine \_ keyerr- \_ Ausgabe**
</dt> <dd>

Es ist ein Fehler mit der Ausgabe aufgetreten.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ mediaengine \_ keyerr \_ hardwarechange** 
</dt> <dd>

Fehler im Zusammenhang mit einer Hardware Änderung.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF \_ mediaengine \_ keyerr- \_ Domäne**
</dt> <dd>

Fehler bei der Domäne.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**MF \_ Die Medien- \_ Engine \_ keyerr** wird mit dem *Code* -Parameter von [**IMF mediakeysessionnotify:: keyerror**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) und dem von [**IMF mediakeysession:: getError**](imfmediakeysession-geterror.md)zurückgegebenen *Codewert* verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Enumerationen](media-foundation-enumerations.md)
</dt> </dl>

 

 




