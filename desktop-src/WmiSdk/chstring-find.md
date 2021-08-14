---
description: Die Find-Methode durchsucht eine Zeichenfolge nach der ersten Übereinstimmung einer Teilzeichenfolge.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: CHString::Find-Methoden (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a7f326b202d107dc192683517508446b3c785266c675e5cf27d92577311d453a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319994"
---
# <a name="chstringfind-methods"></a>CHString::Find-Methoden

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframework, das jetzt als endgültig betrachtet wird, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken betreffen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die **Find-Methode** durchsucht eine Zeichenfolge nach der ersten Übereinstimmung einer Teilzeichenfolge.

### <a name="overload-list"></a>Überladeliste



| Methode                                          | BESCHREIBUNG                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| [**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))     | Sucht in dieser **Zeichenfolge nach dem WSTR.**<br/>    |
| [**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr)) | Sucht in dieser **Zeichenfolge nach LPCWSTR.**<br/> |



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
