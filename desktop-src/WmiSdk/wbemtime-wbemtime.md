---
description: Der wbemtime-Klassenkonstruktor vereinfacht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: 'Wbemtime:: wbemtime-Konstruktoren (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 778b9af2e732b3d294b0348ff2d2b91b60518d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350151"
---
# <a name="wbemtimewbemtime-constructors"></a>Wbemtime:: wbemtime-Konstruktoren

\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Der **wbemtime** -Klassenkonstruktor vereinfacht Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten.

### <a name="overload-list"></a>Überladeliste



| Konstruktor                                                                 | BESCHREIBUNG                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**Wbemtime ()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | Erstellt ein nicht initialisiertes Zeit Objekt.<br/>                          |
| [**Wbemtime (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.<br/> |
| [**Wbemtime (Konstante Zeit \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.<br/> |
| [**Wbemtime (Konstante struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.<br/> |
| [**Wbemtime (Konstante FILETIME-&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.<br/> |
| [**Wbemtime (konstant Systemzeit&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | Initialisiert das neue Zeit Objekt mit dem Wert im-Parameter.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Wbemtime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
