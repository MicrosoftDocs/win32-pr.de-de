---
description: Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus in einem Video Decoder.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Avdecvideothumbnailgenerationmode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958073"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Avdecvideothumbnailgenerationmode-Eigenschaft

Aktiviert oder deaktiviert den Miniatur Ansichts Generierungs Modus in einem Video Decoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideothumbnailgenerationmode**

## <a name="remarks"></a>Bemerkungen

Wenn der Wert **Variant \_ true** ist, verwendet der Decoder eine Einstellung, die für die schnelle Generierung von Miniaturbildern optimiert ist. (Beispielsweise können B-oder P-Frames übersprungen werden.) Andernfalls verwendet der Decoder die normalen Decodierungs Einstellungen, wenn der Wert **Variant \_ false** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




