---
description: Gibt an, ob eine Media Foundation Transformation (MFT) nur im Anwendungsprozess registriert ist.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: MFT_PROCESS_LOCAL_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753944"
---
# <a name="mft_process_local_attribute-attribute"></a>\_ \_ Lokales \_ Attribut Attribut des MFT-Prozesses

Gibt an, ob eine Media Foundation Transformation (MFT) nur im Prozess der Anwendung registriert ist.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird wie folgt verwendet:

1.  Die Anwendung registriert eine lokale MFT, indem Sie entweder die [**mftregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) -oder die [**mftregisterlocalbyclsid**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) -Funktion aufrufen. Diese Funktionen registrieren die MFT im Prozess der Anwendung.
2.  Die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion wird aufgerufen, um MFTs aufzuzählen, die einem bestimmten Satz von Kriterien entsprechen. Die Anwendung ruft die **mftenumex** -Funktion möglicherweise direkt auf, aber häufig wird diese Funktion vom topologielader aufgerufen.
3.  Die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion Ruft ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern ab, die jeweils ein Aktivierungs Objekt für einen MFT darstellen. Wenn eine MFT lokal registriert ist, wird das lokale Attribut Attribut des MFT- \_ Prozesses \_ \_ für das entsprechende Aktivierungs Objekt auf **true** festgelegt.

Der Standardwert für dieses Attribut ist **false**.

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

 

 




