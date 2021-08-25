---
title: AllocFixupInfo-Funktion (NapUtil.h)
description: Belegt Arbeitsspeicher für eine FixupInfo-Struktur der angegebenen Größe.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- Nap-Funktion "AllocFixupInfo"
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95ce329a433439716700b6ffc990d446c5d22faab91fa256f6abc0c73734327d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803490"
---
# <a name="allocfixupinfo-function"></a>AllocFixupInfo-Funktion

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **AllocFixupInfo-Funktion** belegt Arbeitsspeicher für eine [**FixupInfo-Struktur**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) der angegebenen Größe.

## <a name="syntax"></a>Syntax


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fixupInfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Adresse einer neu zugeordneten [**FixupInfo-Struktur.**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)

</dd> <dt>

*countResultCodes* \[ In\]
</dt> <dd>

Die Anzahl der Ergebniscodes, die *fixupInfo* zugeordnet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                   | Beschreibung                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ein ungültiges Argument wurde übergeben.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Das System verfügt nicht über genügend virtuellen Arbeitsspeicher. Dieser Vorgang ist fehlgeschlagen.<br/> |



 

## <a name="remarks"></a>Hinweise

Alle com-Schnittstellen, die vom NAP-System unterstützt werden, verwenden COM-Standardspeicherverwaltungsregeln und die COM-Speicherbezuweisungen (**CoTaskMemAlloc** und **CoTaskMemFree**):

-   **In** werden Parameter vom Aufrufer zugeordnet und freigegeben.
-   **Out-Parameter** werden vom Aufgerufenen zugeordnet und vom Aufrufer mit **coTaskMem** freigegeben.
-   **Ein-/Aus-Parameter** werden vom Aufrufer zugeordnet, vom Aufgerufenen freigegeben und neu zugeordnet und schließlich vom Aufrufer freigegeben, indem **CoTaskMem** verwendet wird.

Alle NAP-Funktionen zum Freigeben von Arbeitsspeicher gibt auch alle eingebetteten Zeiger frei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 





