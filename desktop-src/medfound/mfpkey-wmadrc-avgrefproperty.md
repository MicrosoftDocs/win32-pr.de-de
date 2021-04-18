---
description: Gibt die durchschnittliche Volumeebene von Audioinhalten an.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354572"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>Eigenschaft "mfpkey \_ wmadrc \_ avgref"

Gibt die durchschnittliche Volumeebene von Audioinhalten an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmadrcaveragereferenzierung

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert aus dem Encoder nach der Verarbeitung des Inhalts erhalten. Dieser Wert kann auch für den Decoder für das dynamische Bereichs Steuerelement festgelegt werden, aber er wirkt sich nur dann aus, wenn die Eigenschaft " [mfpkey \_ wmadec \_ drcmode](mfpkey-wmadec-drcmodeproperty.md) " festgelegt ist.

Weitere Informationen zum dynamischen Bereichs Steuerelement finden Sie im Webartikel [Windows Media Audio Professional-Codec-Features](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
