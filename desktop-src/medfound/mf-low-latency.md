---
description: Ermöglicht die Verarbeitung mit geringer Latenz in der Microsoft Media Foundation Pipeline.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51421b68e23ab3f29c15b0b360a7d189befb45cd9046176e6dcb99f1b0748f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956450"
---
# <a name="mf_low_latency-attribute"></a>MF \_ LOW \_ LATENCY-Attribut

Ermöglicht die Verarbeitung mit geringer Latenz in der Microsoft Media Foundation Pipeline.

## <a name="data-type"></a>Datentyp

**BOOL** als **UINT32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="remarks"></a>Hinweise

Niedrige Latenz wird als die kleinstmögliche Verzögerung zwischen dem Generieren (oder Empfangen) der Mediendaten und dem Rendern definiert. Niedrige Latenz ist für Echtzeitkommunikationsszenarien wünschenswert. Für andere Szenarien, z. B. lokale Wiedergabe oder Transcodierung, sollten Sie in der Regel den Modus mit niedriger Latenz nicht aktivieren, da dies die Qualität beeinträchtigen kann.

> [!Note]  
> Der GUID-Wert dieses Attributs ist identisch mit der [CODECAPI \_ AVLowLatencyMode-Eigenschaft,](codecapi-avlowlatencymode.md) die für die [**ICodecAPI-Schnittstelle**](/windows/win32/api/strmif/nn-strmif-icodecapi) definiert ist.

 

Legen Sie dieses Attribut für Pipelinekomponenten wie folgt fest:

-   Medienquelle: Verwenden Sie die [**METHODE VONMEDIASOURCEEx::GetSourceAttributes.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes)
-   Media Foundation-Transformation (MFT): Verwenden Sie die [**METHODE VONTRANSFORM::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Bei Encodern unterstützt der Encoder möglicherweise eine geringe Latenz über die [**ICodecAPI-Schnittstelle.**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   Mediensenke: Fragen Sie die Mediensenke für die [**SCHNITTSTELLE VON ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ab.

Anwendungen legen dieses Attribut in der Regel nicht direkt auf den Pipelinekomponenten fest, sondern legen es für eines der folgenden Objekte fest:

-   [Mediensitzung:](media-session.md)Verwenden Sie den *pConfiguation-Parameter* der [**MFCreateMediaSession-**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) oder [**MFCreatePMPMediaSession-Funktion,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) oder legen Sie andernfalls das -Attribut für die Topologie fest.
-   [Quellleser:](source-reader.md)Legen Sie das Attribut mit den Konfigurationseigenschaften fest, wenn Sie den Quellleser erstellen. Weitere Informationen finden Sie unter [Quellleseattribute.](source-reader-attributes.md)
-   [Sink Writer:](sink-writer.md)Legen Sie das Attribut mit den Konfigurationseigenschaften fest, wenn Sie den Sink Writer erstellen. Weitere Informationen finden Sie unter [Sink Writer Attributes](sink-writer-attributes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sink Writer-Attribute](sink-writer-attributes.md)
</dt> <dt>

[Quellleseattribute](source-reader-attributes.md)
</dt> <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 
