---
description: Gibt den ursprünglichen Geräte Zeitstempel für das Beispiel an.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863427"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a>MF Sample Extension \_ devicereferencesystemtime-Attribut

Gibt den ursprünglichen Geräte Zeitstempel für das Beispiel an.

## <a name="data-type"></a>Datentyp

**UINT64**

## <a name="remarks"></a>Bemerkungen

Dies ist der Zeitstempel eines Geräte Verweises von Medien Beispielen in einer 100-ns-Auflösung. Dieser Zeitstempel kann den tatsächlichen Wert des Abfrage Leistungs Zählers (QPC) enthalten, abhängig von der Quelle, die die Beispiele erzeugt. Dieser Wert kann von anderen Komponenten in der Medien Pipeline geändert werden. Dieser Wert ist nicht für MFTs verfügbar, die in die Aufzeichnungs Pipeline eingefügt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                        |
| Header<br/>                   | <dl> <dt>"MF"-Engine. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>MF-Engine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




