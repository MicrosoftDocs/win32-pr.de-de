---
description: Die getlocaloffsetfordate-Methode gibt den Offset in Minuten zurück (+ oder &\# 8211;) zwischen GMT und Ortszeit für die im-Argument angegebene Zeit.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Wbemtime:: getlocaloffsetfordate-Methode (wbemtime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866860"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>Wbemtime:: getlocaloffsetfordate-Methoden

\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Die **getlocaloffsetfordate** -Methode gibt den Offset in Minuten (+ oder) zwischen GMT und Ortszeit für die im Argument angegebene Zeit zurück.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                           | BESCHREIBUNG                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**Getlocaloffsetfordate (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | Das Argument ist ein Verweis auf eine **Uhrzeit \_ t**.<br/>  |
| [**Getlocaloffsetfordate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | Das Argument ist ein Zeiger auf eine **FILETIME**.<br/>   |
| [**Getlocaloffsetfordate (struct TM \* )**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | Das Argument ist ein Zeiger auf die **TM** -Struktur.<br/> |
| [**Getlocaloffsetfordate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | Das Argument ist ein Zeiger auf eine **Systemzeit**.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Wbemtime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
