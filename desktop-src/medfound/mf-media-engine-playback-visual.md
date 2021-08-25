---
description: Legt ein Microsoft DirectComposition-Visual als Wiedergabebereich für die Medien-Engine fest.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: MF_MEDIA_ENGINE_PLAYBACK_VISUAL Attribut (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e3c41d337fa198b2ab8b6f2e914d1dad53d180920f14860e5cc18faeb21117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113910"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>MF \_ MEDIA ENGINE PLAYBACK \_ \_ \_ VISUAL-Attribut

Legt ein Microsoft DirectComposition-Visual als Wiedergabebereich für die Medien-Engine fest.

## <a name="data-type"></a>Datentyp

**IDCompositionVisual \* *_ gespeichert als _* IUnknown\***

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)

Um dieses Attribut festzulegen, rufen Sie [**DIE ATTRIBUTEAttributes::SetUnknown auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)

## <a name="remarks"></a>Hinweise

Weitere Informationen zu DirectComposition finden Sie unter [DirectComposition](../directcomp/directcomposition-portal.md) und [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).

Dieses Attribut wird mit der [**METHODE VONMEDIAENGINEClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) verwendet, um die Medien-Engine zu initialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
