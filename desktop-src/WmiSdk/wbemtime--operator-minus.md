---
description: 'Subtraktionsoperator der WBEMTime-Klasse (&\# 8211;) wurde überladen zu:'
audience: developer
ms.assetid: 0fa51aab-7ea2-4af7-bb12-1646388b0405
ms.tgt_platform: multiple
title: WBEMTime::operator-Operatoren (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 7748020c1dcf1e332384c3a29c18b37da53e020f42d6cb608d9bf3233608aaaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120750"
---
# <a name="wbemtimeoperator--operators"></a>WBEMTime::operator-Operatoren

\[Die [**WBEMTime-Klasse**](wbemtime.md) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Der Subtraktionsoperator der [**WBEMTime-Klasse**](wbemtime.md) ( ) wurde für Folgendes überladen:

-   Subtrahiert eine Zeitspanne von der Zeit eines Objekts, um ein neues Zeitobjekt zu erzeugen, das die resultierende Zeit enthält.
-   Subtrahiert eine Zeit von der Zeit des Objekts, um ein neues Zeitspannenobjekt zu erzeugen, das die Differenz zwischen den beiden Zeiten enthält.

### <a name="overload-list"></a>Überladeliste



| Operator                                                                         | Beschreibung                                                                      |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**operator-(WBEMTime&)**](/windows/win32/api/rrascfg/nf-rrascfg-ieapproviderconfig-initialize)         | Subtrahiert eine **WBEMTime** von einer **WBEMTime.**<br/>                         |
| [**operator-(WBEMTimeSpan&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-sub(constwbemtimespan_)) | Subtrahiert ein [**WBEMTimeSpan**](/windows/win32/api/wbemtime/nl-wbemtime-wbemtimespan) von einem **WBEMTime -.**<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
