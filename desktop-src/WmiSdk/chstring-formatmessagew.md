---
description: Die überladene FormatMessageW-Methode formatiert eine Nachrichtenzeichenfolge.
audience: developer
ms.assetid: 45780467-d3aa-4927-aa53-60e5ee277c27
ms.tgt_platform: multiple
title: CHString::FormatMessageW-Methoden (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 53f8a9663994ffbc6b50aebddc7d9877c17c1067a074bcdddbe2fc79bc525e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050938"
---
# <a name="chstringformatmessagew-methods"></a>CHString::FormatMessageW-Methoden

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Die überladene **FormatMessageW-Methode** formatiert eine Nachrichtenzeichenfolge.

### <a name="overload-list"></a>Überladeliste



| Methode                                                              | Beschreibung                                                                                     |
|:--------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**FormatMessageW(UINT)**](/previous-versions/windows/desktop/legacy/aa385519(v=vs.85))       | Formatiert diese Nachricht entsprechend dem ressourcenbezeichner, der durch den **UINT** angegeben wird.<br/> |
| [**FormatMessageW(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-formatmessagew(lpcwstr_---)) | Formatiert diese Meldungszeichenfolge gemäß dem von **LPCWSTR** angegebenen Format.<br/>    |



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
