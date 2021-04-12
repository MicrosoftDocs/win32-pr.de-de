---
description: Gibt an, ob die Aufzeichnungs-Engine die DirectX-Videobeschleunigung (DXVA) zum Decodieren von Videos verwendet.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343938"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>\_ \_ \_ \_ DXVA-Attribut für MF-Erfassungs Modul deaktivieren

Gibt an, ob die Aufzeichnungs-Engine die DirectX-Videobeschleunigung (DXVA) zum Decodieren von Videos verwendet.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt, wenn die folgenden Bedingungen zutreffen:

-   Die Aufzeichnungs-Engine decodiert einen komprimierten Videostream aus dem Erfassungsgerät (z. b. wenn das Erfassungsgerät H. 264-Video ausgibt).
-   Der Video Decoder unterstützt die hardwarebeschleunigte Decodierung mithilfe von DXVA.
-   Die Anwendung verwendet das [ \_ \_ \_ D3D \_ Manager](mf-capture-engine-d3d-manager.md) -Attribut der MF-Erfassungs-Engine zum Festlegen der DXGI-Device Manager für die Aufzeichnungs-Engine.

Andernfalls wird dieses Attribut ignoriert.

Dieses Attribut ermöglicht es der Anwendung, DXVA zu deaktivieren, während die Decodierung an Direct3D-Oberflächen noch nicht

Der Standardwert dieses Attributs ist **false**. Dies bedeutet, dass die DXVA-Decodierung aktiviert ist, wenn verfügbar.

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

 

 




