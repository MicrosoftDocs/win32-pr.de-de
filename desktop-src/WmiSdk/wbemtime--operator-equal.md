---
description: Die WBEMTime-Klassenzuweisungsoperatoren werden überladen, um Konvertierungen zwischen verschiedenen Windows und ANSI C-Laufzeitformaten zu ermöglichen. Die verschiedenen überladenen Signaturen sind unten aufgeführt.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: WBEMTime::operator=-Operatoren (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 321ca0ba75d40389fbd6eb2ba70dc67a9b8e16afd3b5390bbc9ec61bd875c79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502900"
---
# <a name="wbemtimeoperator-operators"></a>WBEMTime::operator=-Operatoren

\[Die [**WBEMTime-Klasse**](wbemtime.md) ist Teil des WMI-Anbieterframework, das jetzt als endgültig betrachtet wird, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken ausdrungen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die [**WBEMTime-Klassenzuweisungsoperatoren**](wbemtime.md) werden überladen, um Konvertierungen zwischen verschiedenen Windows und ANSI C-Laufzeitformaten zu ermöglichen. Die verschiedenen überladenen Signaturen sind unten aufgeführt.

### <a name="overload-list"></a>Überladeliste



| Operator                                                                     | Beschreibung                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Konvertiert einen **BSTR in das** **WBEMTime-Format.**<br/>         |
| [**operator=(time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Konvertiert die **Zeit \_ t** in das **WBEMTime-Format.**<br/>        |
| [**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Konvertiert **FILETIME in** das **WBEMTime-Format.**<br/>       |
| [**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Konvertiert eine **tm-Struktur** in das **WBEMTime-Format.**<br/> |
| [**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Konvertiert **SYSTEMTIME in** das **WBEMTime-Format.**<br/>     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
