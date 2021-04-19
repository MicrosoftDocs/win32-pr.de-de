---
description: Enthält die CLSID eines topologieladers für die Medien Sitzung.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: MF_SESSION_TOPOLOADER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359528"
---
# <a name="mf_session_topoloader-attribute"></a>MF- \_ Sitzungs \_ topoloader-Attribut

Enthält die CLSID eines topologieladers für die Medien Sitzung.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut verwenden, um ein benutzerdefiniertes topologielader für die Medien Sitzung bereitzustellen.

Legen Sie dieses Attribut mithilfe des Parameters *pconfiguration* der Funktion [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) oder der Funktion [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) fest.

Wenn dieses Attribut festgelegt ist, ruft die Medien Sitzung **cokreateinstance** mit der angegebenen CLSID auf, wenn das topologielader erstellt wird. Das von dieser CLSID erstellte-Objekt muss die [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) -Schnittstelle verfügbar machen.

Wenn dieses Attribut nicht festgelegt ist, erstellt die Medien Sitzung das standardmäßige topologielader, das in Media Foundation bereitgestellt wird.

Ein topologielader muss Multithread-Apartments unterstützen. Registrieren Sie den topologielader als ThreadingModel = "both". Wenn Sie das topologielader innerhalb des geschützten Medien Pfads (PMP) verwenden, muss das topologieloader auch eine vertrauenswürdige Komponente sein. Weitere Informationen finden Sie unter [geschützter Medien Pfad](protected-media-path.md).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**Imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[Medien Sitzungs Attribute](media-session-attributes.md)
</dt> <dt>

[Benutzerdefinierte topologielader](custom-topology-loaders.md)
</dt> </dl>

 

 




