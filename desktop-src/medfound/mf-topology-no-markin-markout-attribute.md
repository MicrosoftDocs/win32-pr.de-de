---
description: Gibt an, ob die Pipeline nur Stichproben Abtastungen
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: MF_TOPOLOGY_NO_MARKIN_MARKOUT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215138"
---
# <a name="mf_topology_no_markin_markout-attribute"></a>MF- \_ Topologie \_ kein \_ Markin \_ markout-Attribut

Gibt an, ob die Pipeline nur Stichproben Abtastungen

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Standardmäßig werden die Beispiele für die Pipeline mit den richtigen Präsentations Zeiten getestet. Die Kürzung erfolgt auf den topologieknoten, die über das [**MF- \_ toponode- \_ Markin \_ hier**](mf-toponode-markin-here-attribute.md) und die [**MF- \_ toponode- \_ markout \_**](mf-toponode-markout-here-attribute.md) -Attribute verfügen. Wenn die **MF- \_ Topologie \_ kein \_ Markin \_ markout** -Attribut für die Topologie auf **true** festgelegt ist, werden die Beispiele von der Pipeline nicht beschnitten, und die hier aufgeführten Attribute " **MF \_ toponode \_ Markin \_ here** " und " **MF \_ toponode \_ markout \_** " werden ignoriert. Wenn das Attribut nicht festgelegt ist oder den Wert **false** aufweist, werden die Beispiele für die Pipeline getestet.

Eine Anwendung kann die **MF- \_ Topologie \_ kein \_ Markin \_ markout** -Attribut auf " **true** " festlegen, wenn die Anwendung komprimierte Beispiele von der Pipeline empfängt und alle Keyframes erhalten muss, die andernfalls gekürzt werden.

Der Standardwert dieses Attributs ist **false**.

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

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Hier finden Sie ein MF- \_ toponode- \_ Markin \_**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[**MF \_ toponode \_ markout \_ hier**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




