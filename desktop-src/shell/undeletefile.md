---
description: Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer den Befehl "Undelete" aus dem Menü Datei auswählt.
title: FM_UNDELETE_PROC Funktionszeiger (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_UNDELETE_PROC
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 456b053e-e83d-43af-9691-57e1d4fd3f8f
ms.openlocfilehash: 3bed8995954cdfe05bcc8eea82dc47415033e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218057"
---
# <a name="fm_undelete_proc-function-pointer"></a>FM \_ Undelete \_ proc-Funktionszeiger

Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer den Befehl " **Undelete** " aus dem Menü **Datei** auswählt.

## <a name="syntax"></a>Syntax


```C++
typedef DWORD ( APIENTRY *FM_UNDELETE_PROC)(
   HWND  hwndOwner,
   LPSTR lpszDir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndOwner* 
</dt> <dd>

Typ: **HWND**

Das Fenster Handle für den Datei-Manager. Eine wiederherstellen-dll sollte dieses Handle verwenden, um das Besitzer Fenster für ein beliebiges Dialogfeld oder Meldungs Feld anzugeben, das die dll möglicherweise anzeigt.

</dd> <dt>

*lpszdir* 
</dt> <dd>

Typ: **LPSTR**

Die Adresse einer auf NULL endenden Zeichenfolge, die den Namen des ursprünglichen Verzeichnisses enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **DWORD**

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                             | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Ein Fehler ist aufgetreten.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | Eine Datei wurde wieder hergestellt. Das Fenster wird vom Datei-Manager neu gezeichnet.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | Es wurde keine Datei wieder hergestellt.<br/>                                  |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



 

 




