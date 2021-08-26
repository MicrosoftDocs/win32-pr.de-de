---
description: Die InsertAt-Methode fügt ein Element (oder mehrere Kopien eines Elements) oder alle Elemente eines anderen Arrays an einem angegebenen Index ein.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: CHStringArray::InsertAt-Methoden (ChStrArr.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 75332e300987233c0a6f3d6755d27fd7c305a7d86fb6cd9a6143c417222c0dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097250"
---
# <a name="chstringarrayinsertat-methods"></a>CHStringArray::InsertAt-Methoden

\[Die [**CHStringArray-Klasse**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) ist Teil des WMI-Anbieterframework, das jetzt im endgültigen Zustand betrachtet wird, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken betreffen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die **InsertAt-Methode** fügt ein Element (oder mehrere Kopien eines Elements) oder alle Elemente eines anderen Arrays an einem angegebenen Index ein.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                               | BESCHREIBUNG                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))       | Fügt ein oder mehrere Elemente an einem angegebenen Index in ein Array ein.<br/>                                               |
| [**InsertAt(int,CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)) | Fügt alle Elemente eines anderen [**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) an einem angegebenen Index in einem Array ein.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChStrArr.h (include FwCommon.h)</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

�

�
