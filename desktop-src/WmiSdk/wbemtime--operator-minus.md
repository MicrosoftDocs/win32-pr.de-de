---
description: 'Der wbemtime-Klassen Subtraktions Operator (&\# 8211;) wurde überladen zu:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: 'Wbemtime:: Operator-Operatoren (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 39256ba9d922ea9d3eef8e442115e840b963ca71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352575"
---
# <a name="wbemtimeoperator--operators"></a>Wbemtime:: Operator-Operatoren

\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Der [**wbemtime**](wbemtime.md) -Klassen Subtraktions Operator () wurde überladen zu:

-   Subtrahieren Sie eine Zeitspanne von der Zeit eines Objekts, um ein neues Zeit Objekt zu schaffen, das die resultierende Zeit enthält.
-   Subtrahieren Sie eine Uhrzeit aus der-Zeit des-Objekts, um ein neues Zeitspannen Objekt zu erhalten, das die Differenz zwischen den beiden vorkommen enthält.

### <a name="overload-list"></a>Überladeliste



| Operator                                                                         | BESCHREIBUNG                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**Operator-(wbemtime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Subtrahiert eine **wbemtime** von einer **wbemtime**.<br/>                         |
| [**Operator-(wbemtimespan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | Subtrahiert [**wbemtimespan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) von einem **wbemtime**-Zeichen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Wbemtime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
