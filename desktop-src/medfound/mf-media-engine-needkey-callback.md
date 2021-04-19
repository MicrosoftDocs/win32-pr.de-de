---
description: Attribut, das bei der Erstellung in imfmediaengineneedkeynotify an die Medien-Engine weitergegeben wird.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363891"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a>MF-Medienmodul, \_ \_ \_ needkey- \_ Rückruf Attribut

Attribut, das bei der Erstellung in [**imfmediaengineneedkeynotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) an die Medien-Engine weitergegeben wird.

## <a name="data-type"></a>Datentyp

**IMF mediaengineneedkeynotify \* *_ gespeichert als _* IUnknown\***

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Zeiger auf die [**imfmediaengineneedkeynotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) -Schnittstelle, die von der Anwendung implementiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




