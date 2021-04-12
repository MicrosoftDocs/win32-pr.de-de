---
description: Die wbemtime-Klassen Zuweisungs Operatoren sind überladen, um Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten zu vereinfachen. Die verschiedenen überladenen Signaturen sind unten aufgeführt.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Wbemtime:: Operator =-Operatoren (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349609"
---
# <a name="wbemtimeoperator-operators"></a>Wbemtime:: Operator =-Operatoren

\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die [**wbemtime**](wbemtime.md) -Klassen Zuweisungs Operatoren sind überladen, um Konvertierungen zwischen verschiedenen Windows-und ANSI C-Lauf Zeitformaten zu vereinfachen. Die verschiedenen überladenen Signaturen sind unten aufgeführt.

### <a name="overload-list"></a>Überladeliste



| Operator                                                                     | BESCHREIBUNG                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**Operator = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Konvertiert ein **BSTR** -in ein **wbemtime** -Format.<br/>         |
| [**Operator = (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Konvertiert **time \_ t** in das **wbemtime** -Format.<br/>        |
| [**Operator = (FILETIME-&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Konvertiert **FILETIME** in das **wbemtime** -Format.<br/>       |
| [**Operator = (struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Konvertiert eine **TM** -Struktur in das **wbemtime** -Format.<br/> |
| [**Operator = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Konvertiert **SYSTEMTIME** in das **wbemtime** -Format.<br/>     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Wbemtime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
