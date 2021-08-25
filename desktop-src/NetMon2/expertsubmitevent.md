---
description: Die ExpertSubmitEvent-Funktion gibt an, dass eine Ereignisbedingung vorhanden ist, und stellt eine Datenstruktur zur Beschreibung der Bedingung zurEntspricht.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: ExpertSubmitEvent-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b6ce73d378e4d8432459a23a76b30ebf4d558a5f82ec230e6841eeeb621aed13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744220"
---
# <a name="expertsubmitevent-function"></a>ExpertSubmitEvent-Funktion

Die **ExpertSubmitEvent-Funktion** gibt an, dass eine Ereignisbedingung vorhanden ist, und stellt eine Datenstruktur zur Beschreibung der Bedingung zurEntspricht.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* \[ In\]
</dt> <dd>

Eindeutiger Bezeichner des Experten. Netzwerkmonitor *hExpertKey an* den Experten übergeben, wenn er die [Run-Funktion](run.md) aufruft.

</dd> <dt>

*pExpertEvent* \[ In\]
</dt> <dd>

Ein Zeiger auf eine **NMEVENTDATA-Struktur,** die die Ereignisbedingung beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, gibt der Rückgabewert den Grund für den Fehler an. Wenn der Rückgabewert NMERR EXPERT TERMINATE ist, bereinigt der Experte \_ \_ sofort und gibt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




