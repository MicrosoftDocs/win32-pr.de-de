---
description: Legt einen Zeiger auf den DXGI-Device Manager für die Aufzeichnungs-Engine fest.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: MF_CAPTURE_ENGINE_D3D_MANAGER-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129800"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>MF- \_ Erfassungs Modul \_ \_ D3D \_ Manager-Attribut

Legt einen Zeiger auf den DXGI-Device Manager für die Aufzeichnungs-Engine fest.

## <a name="data-type"></a>Datentyp

**IUnknown \** _

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfdxgidebug Manager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle. Mit diesem Attribut kann die Aufzeichnungs-Engine Video Frames mithilfe von DXGI-Oberflächen zuordnen und Hardwarebeschleunigung für Decodierung und Videoverarbeitung verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>"MF"-Engine. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Aufzeichnungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**IMF captureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




