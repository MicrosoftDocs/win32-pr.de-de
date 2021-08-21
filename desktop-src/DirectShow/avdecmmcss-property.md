---
description: Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungsthread an.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: AVDecMmcss-Eigenschaft (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9084db3cce8d555afa44097271a6b08f58cfea2f2edcb7acb5845730afc86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159944"
---
# <a name="avdecmmcss-property"></a>AVDecMmcss-Eigenschaft

Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungsthread an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecMmcssClass**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist der Name der MMCSS-Klasse.

## <a name="remarks"></a>Hinweise

MIT MMCSS können Anwendungen sicherstellen, dass bei der zeitkritischen Verarbeitung prioritätsbasierter Zugriff auf CPU-Ressourcen vorliegt. Dies funktioniert, indem registrierte Threads zu höheren Threadprioritäten erhöht werden, während ihre Prioritäten in regelmäßigen Abständen verringert werden, um zeitaufwendige Zeit für andere Prozesse zu schaffen.

Der empfohlene Wert für Audiodecoder ist "Audio", und der empfohlene Wert für Videodecoder ist "Playback".

Wenn der MMCSS-Dienst nicht verfügbar ist oder die angegebene MMCSS-Klasse nicht vorhanden ist, hat das Festlegen der -Eigenschaft keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




