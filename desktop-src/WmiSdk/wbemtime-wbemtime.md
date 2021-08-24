---
description: Der WBEMTime-Klassenkonstruktor ermöglicht Konvertierungen zwischen verschiedenen Windows- und ANSI C-Laufzeitformaten.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: WBEMTime::WBEMTime-Konstruktoren (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ac02e3ee2a7a77ed1cc2cc9157b0d6c191563f234bf594cb53029a76e76f0137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757620"
---
# <a name="wbemtimewbemtime-constructors"></a>WBEMTime::WBEMTime-Konstruktoren

\[Die [**WBEMTime-Klasse**](wbemtime.md) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Der **WBEMTime-Klassenkonstruktor** ermöglicht Konvertierungen zwischen verschiedenen Windows- und ANSI C-Laufzeitformaten.

### <a name="overload-list"></a>Überladeliste



| Konstruktor                                                                 | BESCHREIBUNG                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | Erstellt ein nicht initialisiertes Zeitobjekt.<br/>                          |
| [**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | Initialisiert das neue Zeitobjekt mit dem Wert im -Parameter.<br/> |
| [**WBEMTime(const time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | Initialisiert das neue Zeitobjekt mit dem Wert im -Parameter.<br/> |
| [**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | Initialisiert das neue Zeitobjekt mit dem Wert im -Parameter.<br/> |
| [**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | Initialisiert das neue Zeitobjekt mit dem Wert im -Parameter.<br/> |
| [**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | Initialisiert das neue Zeitobjekt mit dem Wert im -Parameter.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
