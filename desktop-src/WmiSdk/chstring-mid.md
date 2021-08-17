---
description: Die Mid-Methode extrahiert eine Teilzeichenfolge der Länge nCount-Zeichen aus einer CHString-Zeichenfolge, beginnend bei Position nFirst (nullbasiert). Die -Methode gibt eine Kopie der extrahierten Teilzeichenfolge zurück.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: CHString::Mid-Methoden (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cbe5b7fc6e3f0d4130e106217c46c82202c230f180dd4c90d09f90073dee08ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319842"
---
# <a name="chstringmid-methods"></a>CHString::Mid-Methoden

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Die **Mid-Methode** extrahiert eine Teilzeichenfolge der Länge *nCount-Zeichen* aus einer [**CHString-Zeichenfolge,**](chstring.md) beginnend bei Position *nFirst* (nullbasiert). Die -Methode gibt eine Kopie der extrahierten Teilzeichenfolge zurück.

### <a name="overload-list"></a>Überladeliste



| Methode                                        | Beschreibung                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Mid(int, int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | Extrahiert eine Teilzeichenfolge der angegebenen Länge und des Angegebenen Anfangspunkts.<br/> |
| [**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | Extrahiert eine Teilzeichenfolge, die bei int beginnt.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChString.h (include FwCommon.h)</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
