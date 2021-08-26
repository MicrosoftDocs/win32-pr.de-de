---
description: Enthält die CLSID eines Topologieladeers für die Mediensitzung.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: MF_SESSION_TOPOLOADER -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9568193bbdbd46485015b6e5975db26fca2b552b23b7c227576e4e6544d69af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955130"
---
# <a name="mf_session_topoloader-attribute"></a>MF \_ SESSION \_ TOPOLOADER-Attribut

Enthält die CLSID eines Topologieladeers für die Mediensitzung.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut verwenden, um ein benutzerdefiniertes Topologielader für die Mediensitzung zur Verfügung zu stellen.

Legen Sie dieses Attribut mithilfe *des pConfiguration-Parameters* der [**MFCreateMediaSession-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) oder der [**MFCreatePMPMediaSession-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) fest.

Wenn dieses Attribut festgelegt ist, ruft die Mediensitzung **CoCreateInstance** mit der angegebenen CLSID auf, wenn sie das Topologielader erstellt. Das von dieser CLSID erstellte -Objekt muss die [**-SCHNITTSTELLE DESTTOPOLoaders**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) verfügbar machen.

Wenn dieses Attribut nicht festgelegt ist, erstellt die Mediensitzung das Standardtopologielader, das in der Media Foundation.

Ein Topologielader muss Multithread-Apartment unterstützen. Sie sollten das Topologielader als ThreadingModel="Both" registrieren. Wenn Sie das Topologielader innerhalb des geschützten Medienpfads (PMP) verwenden, muss das Topologielader außerdem eine vertrauenswürdige Komponente sein. Weitere Informationen finden Sie unter [Protected Media Path](protected-media-path.md).

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**ATTRIBUTEs::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Media Session Attributes](media-session-attributes.md)
</dt> <dt>

[Benutzerdefinierte Topologielader](custom-topology-loaders.md)
</dt> </dl>

 

 




