---
description: Stellt eine Anforderung für ein Beispiel aus einem MediaStreamSource-Element dar.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Imfmediastreamsourcesamplerequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351509"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>Imfmediastreamsourcesamplerequest-Schnittstelle

Stellt eine Anforderung für ein Beispiel aus einem MediaStreamSource-Element dar.

## <a name="members"></a>Member

Die **imfmediastreamsourcesamplerequest** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imfmediastreamsourcesamplerequest** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imfmediastreamsourcesamplerequest** -Schnittstelle verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | Legt das Beispiel für die Medienstrom Quelle fest.<br/> |



 

## <a name="remarks"></a>Bemerkungen

**Mfmediastreamsourcesamplerequest** wird von der [**Windows. Media. Core. mediastreamsourcesamplerequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) -Lauf Zeit Klasse implementiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                       |
| IDL<br/>                      | <dl> <dt>MFI. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Schnittstellen](media-foundation-interfaces.md)
</dt> </dl>

 

 
