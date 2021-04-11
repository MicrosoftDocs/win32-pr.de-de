---
description: Jeder der folgenden Konstruktoren initialisiert ein neues chstring-Objekt mit den angegebenen Daten.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: 'Chstring:: chstring-Konstruktoren (chstring. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 711d2f28680a9f273ff808876e30e92f66336b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216320"
---
# <a name="chstringchstring-constructors"></a>Chstring:: chstring-Konstruktoren

\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Jeder der folgenden Konstruktoren initialisiert ein neues [**chstring**](chstring.md) -Objekt mit den angegebenen Daten.

### <a name="overload-list"></a>Überladeliste



| Konstruktor                                                                        | BESCHREIBUNG                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**Chstring ()**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | Erstellt ein leeres chstring-Objekt.<br/>                 |
| [**Chstring (LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))                              | Initialisiert mit dem LPCSTR-Wert.<br/>                |
| [**Chstring (LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))                            | Initialisiert mit dem LPCWSTR-Wert.<br/>               |
| [**Chstring (WCHAR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))                        | Initialisiert mit int-Kopien des WCHAR-Werts.<br/>   |
| [**Chstring (LPCWSTR, int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))                    | Initialisiert mit int-Kopien des LPCWSTR-Werts.<br/> |
| [**Chstring (konstantenchstring-&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))            | Repliziert den chstring-Parameter.<br/>                |
| [**Chstring (Konstante ohne Vorzeichen \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar)) | Initialisiert mit dem Wert, auf den von char verwiesen wird \* .<br/>  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Chstring. h (Include-Datei "f")</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>Framedyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
