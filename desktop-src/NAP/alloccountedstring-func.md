---
title: "\"Zuweisung\"-Funktion (\"naputil. h\")"
description: Ordnet Speicher für eine NULL-terminierte Zeichenfolge zu und gibt Sie in einer rattedstring-Struktur zurück.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- Zuweisung der "Zuweisung"-Funktion
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340766"
---
# <a name="alloccountedstring-function"></a>' Zuweisung '-Funktion

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die " **belegczähltedstring** "-Funktion ordnet Arbeitsspeicher für eine auf NULL endenden Zeichenfolge zu und gibt Sie in einer " [**count String**](/windows/win32/api/naptypes/ns-naptypes-countedstring) "-Struktur zurück.

## <a name="syntax"></a>Syntax


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *zählzeichen Folge* \[ " in, out\]
</dt> <dd>

Ein Zeiger auf die Adresse einer neu zugeordneten [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur.

</dd> <dt>

*Zeichenfolge* \[ in\]
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, die in der " *zähltedstring*" zurückgegeben werden soll.

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

[**Freizähltedstring**](freecountedstring-func.md)
</dt> </dl>

 

 





