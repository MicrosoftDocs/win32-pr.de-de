---
title: "\"Zuweisung\"-Funktion (\"naputil. h\")"
description: Weist Arbeitsspeicher für eine fixupinfo-Struktur der angegebenen Größe zu.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- "' Zuweisung ' der Funktion ' ' der Funktion ' NAP '"
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
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858700"
---
# <a name="allocfixupinfo-function"></a>' Zuweisung '-Funktion

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die Funktion " **belegcfixupinfo** " weist Speicher für eine [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur der angegebenen Größe zu.

## <a name="syntax"></a>Syntax


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fixupinfo* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Adresse einer neu zugewiesenen [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur.

</dd> <dt>

*countrytresultcodes* \[ in\]
</dt> <dd>

Die Anzahl der der *fixupinfo* zuzuordnenden Ergebnis Codes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                                   | Beschreibung                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>                       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ein ungültiges Argument wurde übergeben.<br/>                                 |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Das System verfügt nicht über den virtuellen Arbeitsspeicher. Bei diesem Vorgang ist ein Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):

-   **In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.
-   Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.
-   **In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.

Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Naputil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Freifixupinfo"**](freefixupinfo-func.md)
</dt> </dl>

 

 





