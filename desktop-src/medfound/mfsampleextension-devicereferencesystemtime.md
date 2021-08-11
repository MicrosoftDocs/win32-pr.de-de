---
description: Gibt den ursprünglichen Gerätezeitstempel für das Beispiel an.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime -Attribut (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0458c1a2b0f5b204483cba0e6f571a2a5ace34b7b39463cc20ded664eecaaa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241135"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>MFSampleExtension \_ DeviceReferenceSystemTime-Attribut

Gibt den ursprünglichen Gerätezeitstempel für das Beispiel an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Hinweise

Dies ist der Geräteverweiszeitstempel von Medienbeispielen in einer Auflösung von 100ns. Dieser Zeitstempel kann je nach Quelle, die die Stichproben erzeugt, den tatsächlichen Wert des Abfrageleistungsindikators (Query Performance Counter, QPC) enthalten. Dieser Wert kann von anderen Komponenten in der Medienpipeline geändert werden. Dieser Wert ist für MFTs, die in die Erfassungspipeline eingefügt werden, nicht verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




