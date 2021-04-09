---
description: Enthält den Klassen Bezeichner (CLSID) einer Media Foundation Transformation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959237"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>Attribut Attribut der MFT- \_ Transformation für \_ CLSID \_

Enthält den Klassen Bezeichner (CLSID) einer Media Foundation Transformation (MFT).

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.

Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben werden.

Dieses Attribut wird vom Aktivierungs Objekt intern verwendet, wenn es die MFT erstellt. Anwendungen sollten diese CLSID nicht direkt verwenden, um die MFT zu erstellen, da das Aktivierungs Objekt möglicherweise die MFT initialisieren muss. Um eine Instanz des MFT zu erstellen, rufen Sie daher [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) für das Aktivierungs Objekt auf.

Beachten Sie, dass sich die [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion in dieser Hinsicht anders verhält als die [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion. Die **mftenum** -Funktion gibt CLSIDs zurück, die von der Anwendung an die **cokreatumstance** -Funktion übergeben werden. Die **MF** -Funktion gibt anstelle von CLSIDs Aktivierungs Objekte zurück.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




