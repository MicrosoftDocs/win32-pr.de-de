---
description: Gibt an, welche Ausgabe die primäre Ausgabe auf einem Tee-Knoten ist.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: MF_TOPONODE_PRIMARYOUTPUT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344168"
---
# <a name="mf_toponode_primaryoutput-attribute"></a>MF \_ toponode \_ primaryoutput-Attribut

Gibt an, welche Ausgabe die primäre Ausgabe auf einem Tee-Knoten ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Tee-Knoten (**MF- \_ topologieknoten \_ \_**).

Der Wert dieses Attributs ist der null basierte Index einer Ausgabe Verbindung auf diesem Tee-Knoten. Dieser Wert gibt an, welche Ausgabe der primäre Ausgabestream ist. Die Pipeline wartet auf eine Anforderung von der primären Ausgabe, bevor Anforderungen aus den anderen Ausgaben verarbeitet werden.

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

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




