---
description: Ermöglicht der Medien-Engine, geschützte Inhalte wiederzugeben.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361120"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>MF \_ Media \_ Engine \_ Content \_ Protection \_ Manager-Attribut

Ermöglicht der Medien-Engine, geschützte Inhalte wiederzugeben.

## <a name="data-type"></a>Datentyp

**IUnknown\***

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [**imfcontentschutzmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle. Der Aufrufer muss die-Schnittstelle implementieren.

Dieses Attribut kann eines der Attribute sein, die an [**imfmediaengineclassfactory:: kreateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)übergeben werden. Dies ist erforderlich, wenn geschützter Inhalt wiedergegeben werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>MF mediaengine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMF mediaengineclassfactory:: "forateinstance"**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




