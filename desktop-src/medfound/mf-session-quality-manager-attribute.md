---
description: Enthält die CLSID eines Quality Managers für die Medien Sitzung.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: MF_SESSION_QUALITY_MANAGER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346658"
---
# <a name="mf_session_quality_manager-attribute"></a>\_ \_ Quality Manager- \_ Attribut der MF-Sitzung

Enthält die CLSID eines Quality Managers für die Medien Sitzung.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut verwenden, um einen benutzerdefinierten Quality Manager für die Medien Sitzung bereitzustellen.

Legen Sie dieses Attribut mithilfe des Parameters *pconfiguration* der Funktion [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) oder [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) fest.

Wenn dieses Attribut festgelegt ist, ruft die Medien Sitzung **cokreateinstance** mit der angegebenen CLSID auf, um den Qualitäts-Manager zu erstellen. Das von dieser CLSID erstellte-Objekt muss die [**imvqualitymanager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) -Schnittstelle verfügbar machen.

Wenn dieses Attribut nicht festgelegt ist, erstellt die Medien Sitzung den Standard-Quality Manager, der in Media Foundation bereitgestellt wird.

Wenn Sie die Medien Sitzung ohne Quality Manager ausführen möchten, legen Sie dieses Attribut auf **GUID \_ null** fest.

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
</dt> </dl>

 

 




