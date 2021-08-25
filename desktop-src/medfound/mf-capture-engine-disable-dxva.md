---
description: Gibt an, ob die Erfassungs-Engine DirectX Video Acceleration (DXVA) für die Videodecodierung verwendet.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA-Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c722b70e1707e6ad5d14b7afca0da2c8d1a63b3a132345e727de1f37023916a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941010"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>MF \_ CAPTURE ENGINE DISABLE \_ \_ \_ DXVA-Attribut

Gibt an, ob die Erfassungs-Engine DirectX Video Acceleration (DXVA) für die Videodecodierung verwendet.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt, wenn die folgenden Bedingungen zutreffen:

-   Die Erfassungs-Engine decodiert einen komprimierten Videodatenstrom vom Erfassungsgerät (z. B. wenn das Erfassungsgerät H.264-Video ausgibt).
-   Der Videodecoder unterstützt die hardwarebeschleunigte Decodierung mit DXVA.
-   Die Anwendung verwendet das [ATTRIBUT MF CAPTURE ENGINE \_ \_ \_ D3D \_ MANAGER,](mf-capture-engine-d3d-manager.md) um die DXGI-Geräte-Manager auf der Erfassungs-Engine festzulegen.

Andernfalls wird dieses Attribut ignoriert.

Mit diesem Attribut kann die Anwendung DXVA deaktivieren, während sie weiterhin in Direct3D-Oberflächen decodiert.

Der Standardwert dieses Attributs ist **FALSE.** Dies bedeutet, dass die DXVA-Decodierung aktiviert ist, wenn verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attribute der Erfassungs-Engine](capture-engine-attributes.md)
</dt> <dt>

[**ADRPaturEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




