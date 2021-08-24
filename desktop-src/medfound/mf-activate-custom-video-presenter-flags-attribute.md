---
description: Gibt an, wie eine benutzerdefinierte Präsentation für den erweiterten Videorenderer (EVR) erstellt wird.
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb223224b7dc01dbfcbfe43962201e4c40871d2d7d1a2be0e5cf78ebcac21430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723667"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a>MF \_ ACTIVATE CUSTOM VIDEO \_ \_ \_ PRESENTER \_ FLAGS-Attribut

Gibt an, wie eine benutzerdefinierte Präsentation für den erweiterten Videorenderer (EVR) erstellt wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut für den [**POINTERActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festlegen, der von der [**MFCreateVideoRendererActivate-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) abgerufen wurde. Der Wert dieses Attributs ist ein bitweises **OR** der folgenden Werte.



| Wert                                          | Beschreibung                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ ACTIVATE \_ CUSTOM \_ PRESENTER \_ ALLOWFAIL** | Wenn die [**ACTIVATEActivate::ActivateObject-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) die benutzerdefinierte Präsentation der Anwendung nicht erstellen kann, wird stattdessen die EVR-Standardvorgabe verwendet. Standardmäßig schlägt die **ActivateObject-Methode** fehl, wenn beim Erstellen des benutzerdefinierten Presenters ein Fehler beim [**OBJECTActivate-Objekt**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) auftritt. |



 

Anwendungen können das [**MF ACTIVATE CUSTOM VIDEO \_ \_ \_ \_ PRESENTER \_ CLSID-Attribut**](mf-activate-custom-video-presenter-clsid-attribute.md) verwenden, um eine benutzerdefinierte Präsentation für die EVR anzugeben.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Erweiterte Videorendererattribute](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Aktivierungsobjekte](activation-objects.md)
</dt> <dt>

[Schreiben eines EVR-Presenters](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




