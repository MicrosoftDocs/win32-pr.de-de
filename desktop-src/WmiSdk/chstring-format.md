---
description: Die Format-Methode formatiert und speichert eine Reihe von Zeichen und Werten in einer CHString-Zeichenfolge.
audience: developer
ms.assetid: 95d24b0e-3580-4a5d-8dad-50d44ef1ca39
ms.tgt_platform: multiple
title: CHString::Format-Methoden (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5432ac16b3e59b3f5e56d862a5bf66f5b23f732f74d586066584b6b937327830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319939"
---
# <a name="chstringformat-methods"></a>CHString::Format-Methoden

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframework, das jetzt als endgültig betrachtet wird, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken betreffen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die **Format-Methode** formatiert und speichert eine Reihe von Zeichen und Werten in einer [**CHString-Zeichenfolge.**](chstring.md)

### <a name="overload-list"></a>Überladeliste



| Methode                                              | Beschreibung                                                                                      |
|:----------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Format(UINT)**](/previous-versions/windows/desktop/legacy/aa385532(v=vs.85))       | Formatiert diese CHString gemäß dem ressourcenbezeichner, der durch **den UINT angegeben wird.**<br/> |
| [**Format(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-format(lpcwstr_---)) | Formatiert diese CHString-Datei gemäß dem von **LPCWSTR angegebenen Format.**<br/>           |



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
