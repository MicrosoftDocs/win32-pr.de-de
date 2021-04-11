---
description: Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: MF_PD_PREFERRED_LANGUAGE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218242"
---
# <a name="mf_pd_preferred_language-attribute"></a>Bevorzugte Programmiersprache für MF \_ PD \_ \_

Enthält die bevorzugte RFC 1766-Sprache der Medienquelle.

## <a name="data-type"></a>Datentyp

**WCHAR**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.

## <a name="applies-to"></a>Gilt für:

[**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Bemerkungen

Das \_ bevorzugte Programmiersprachen Attribut von MF PD \_ \_ ist optional. Eine Anwendung kann dieses Attribut für eine Medienquelle (z. b. eine Netzwerkquelle) festlegen, um Ihre bevorzugte Sprache anzugeben.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




