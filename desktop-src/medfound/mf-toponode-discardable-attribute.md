---
description: Gibt an, ob die Pipeline Beispiele von einem topologieknoten ablegen kann.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: MF_TOPONODE_DISCARDABLE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363740"
---
# <a name="mf_toponode_discardable-attribute"></a>Zu \_ verwerfbares MF-toponode- \_ Attribut

Gibt an, ob die Pipeline Beispiele von einem topologieknoten ablegen kann.

## <a name="data-type"></a>Datentyp

Bytearray

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für alle Knoten Typen. In der Regel legen Sie dieses Attribut auf Tee-Knoten fest, um anzugeben, dass die sekundären Ausgaben nicht von wesentlicher Bedeutung sind.

Der Wert des-Attributs ist ein Array von Indizes für Ausgabedaten Ströme auf dem Knoten.

Wenn dieses Attribut festgelegt ist, kann die Pipeline Beispiele aus den angegebenen Ausgabestreams ablegen, wenn der Stream ausfällt.

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

[**Imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




