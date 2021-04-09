---
description: Gibt an, ob die Media-Senke der Digital Living Network Alliance (DLNA) den Multimedia Class Scheduler Service (MMCSS) verwendet.
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: MF_MP2DLNA_USE_MMCSS-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042340"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a>MF \_ MP2DLNA \_ Verwenden des \_ MMCSS-Attributs

Gibt an, ob die Media-Senke der Digital Living Network Alliance (DLNA) den Multimedia Class Scheduler Service (MMCSS) verwendet.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Wenn Sie dieses Attribut für die DLNA-Medien Senke festlegen möchten, Fragen Sie die Medien Senke nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab. Legen Sie das-Attribut vor Beginn des Streamings fest.

Wenn dieses Attribut **true** ist, registriert sich die DLNA-Medien Senke bei MMCSS.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




