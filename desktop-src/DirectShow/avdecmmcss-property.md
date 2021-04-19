---
description: Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungs Thread an.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Avdecmmcss-Eigenschaft (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370815"
---
# <a name="avdecmmcss-property"></a>Avdecmmcss (Eigenschaft)

Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungs Thread an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecmmcssclass**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist der Name der MMCSS-Klasse.

## <a name="remarks"></a>Bemerkungen

Mit MMCSS können Anwendungen sicherstellen, dass die Zeit empfindliche Verarbeitung einen priorisierten Zugriff auf CPU-Ressourcen hat. Dies funktioniert, indem registrierte Threads auf höhere Thread Prioritäten erhöht werden, während ihre Prioritäten in regelmäßigen Abständen gesenkt werden, um Zeit für andere Prozesse zu erzielen.

Der empfohlene Wert für Audiodecoder lautet "Audiodatei", und der empfohlene Wert für Video-Decoder ist "Wiedergabe".

Wenn der MMCSS-Dienst nicht verfügbar ist oder die angegebene MMCSS-Klasse nicht vorhanden ist, hat das Festlegen der-Eigenschaft keine Auswirkung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




