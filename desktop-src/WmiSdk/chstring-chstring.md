---
description: Jeder der folgenden Konstruktoren initialisiert ein neues CHString-Objekt mit den angegebenen Daten.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: CHString::CHString-Konstruktoren (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 80ce10988fc335c5a16eff8507346dbcdffd6fa70f75d74fb48d3f84b0e2332b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320048"
---
# <a name="chstringchstring-constructors"></a>CHString::CHString-Konstruktoren

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframework, das jetzt als endgültig betrachtet wird, und es sind keine weiteren Entwicklungen, Erweiterungen oder Updates für nicht sich sicherheitsbezogene Probleme verfügbar, die sich auf diese Bibliotheken betreffen. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Jeder der folgenden Konstruktoren initialisiert ein neues [**CHString-Objekt**](chstring.md) mit den angegebenen Daten.

### <a name="overload-list"></a>Überladeliste



| Konstruktor                                                                        | BESCHREIBUNG                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CHString()**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | Erstellt ein leeres CHString-Objekt.<br/>                 |
| [**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))                              | Initialisiert mit dem LPCSTR-Wert.<br/>                |
| [**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))                            | Initialisiert mit dem LPCWSTR-Wert.<br/>               |
| [**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))                        | Initialisiert mit int-Kopien des WCHAR-Werts.<br/>   |
| [**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))                    | Initialisiert mit int-Kopien des LPCWSTR-Werts.<br/> |
| [**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))            | Repliziert den CHString-Parameter.<br/>                |
| [**CHString(const unsigned char \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar)) | Initialisiert mit dem Wert, auf den char \* zeigt.<br/>  |



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
