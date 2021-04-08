---
description: Die getcapturemactype-Funktion gibt den Mac-Typ einer angegebenen Erfassung zurück.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Getcapturemactype-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750096"
---
# <a name="getcapturemactype-function"></a>Getcapturemactype-Funktion

Die **getcapturemactype** -Funktion gibt den Mac-Typ einer angegebenen Erfassung zurück.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcapture* \[ in\]
</dt> <dd>

Handle für die Erfassung. Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **getcapturemactype** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert einer der folgenden Mac-Typen.

-   Unbekannter Mac- \_ Typ. \_
-   Mac- \_ Typ \_ Ethernet
-   Mac- \_ Typ \_ TokenRing
-   Mac- \_ Typ " \_ f"

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode.



| Rückgabecode                                                                                              | Beschreibung                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Mac- \_ Typ \_ unbekannt**</dt> </dl> | Ein bekannter Mac-Typ konnte von Netzwerkmonitor nicht gefunden werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Handle der Erfassung kann auf verschiedene Weise abgerufen werden, abhängig von der Person, die den-Befehl aufruft. Für Experten wird das Handle im **hcapture** -Member der " [expertstartupinfo](expertstartupinfo.md) "-Struktur angegeben. Für Parser kann das Erfassungs Handle abgerufen werden, indem die [getframecapturehandle](getframecapturehandle.md) -Funktion aufgerufen wird.

[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturemactype** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




