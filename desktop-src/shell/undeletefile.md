---
description: Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer im Menü Datei den Befehl Undelete ausgibt.
title: FM_UNDELETE_PROC Funktionszeiger (Wfext.h)
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
ms.openlocfilehash: b7549b521c241429f1c5c7edb7f83eadf25f5d37
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842421"
---
# <a name="fm_undelete_proc-function-pointer"></a>FM \_ UNDELETE \_ PROC-Funktionszeiger

Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer im Menü **Datei** den Befehl **Wiederherstellen** ausgibt.

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

Das Fensterhandle für den Datei-Manager. Eine wiederherstellende DLL sollte dieses Handle verwenden, um das Besitzerfenster für jedes Dialogfeld oder Meldungsfeld anzugeben, das die DLL möglicherweise anzeigt.

</dd> <dt>

*lpszDir* 
</dt> <dd>

Typ: **LPSTR**

Die Adresse einer auf NULL endende Zeichenfolge, die den Namen des ursprünglichen Verzeichnisses enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **DWORD**

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                             | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**-1**</dt> </dl>       | Ein Fehler ist aufgetreten.<br/>                                      |
| <dl> <dt>**IDOK**</dt> </dl>     | Eine Datei wurde gelöscht. Der Datei-Manager bemalt das Fenster neu.<br/> |
| <dl> <dt>**IDCANCEL**</dt> </dl> | Es wurde keine Datei gelöscht.<br/>                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



 

 




