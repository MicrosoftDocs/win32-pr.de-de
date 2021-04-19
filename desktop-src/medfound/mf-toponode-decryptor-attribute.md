---
description: Gibt an, ob ein-Objekt, das dem-Objekt zugrunde liegt, eine Entschlüsselung ist.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: MF_TOPONODE_DECRYPTOR-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363375"
---
# <a name="mf_toponode_decryptor-attribute"></a>MF- \_ Attribut "toponode \_ decryptor"

Gibt an, ob das zugrunde liegende Objekt eines topologiedjektes eine Entschlüsselung ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für alle Knoten Typen.

Wenn der Wert dieses Attributs ungleich 0 (null) ist, ist das zugrunde liegende Objekt des Knotens eine Entschlüsselung.

Anwendungen verwenden dieses Attribut in der Regel nicht direkt. Die Medien Sitzung legt dieses Attribut fest, wenn ein Knoten für eine Entschlüsselung erstellt wird, die von der [**imfinputtrustauthority:: getdecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) -Methode abgerufen wird.

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

 

 




