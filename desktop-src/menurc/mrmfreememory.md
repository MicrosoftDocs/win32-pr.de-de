---
title: Mrmfrememory-Funktion (mrmresourceindexer. h)
description: Gibt Arbeitsspeicher frei, der von mrmkreateconfiginmemory, mrmkreateresourcefileinmemory, mrmdumpprifileinmemory und mrmdumppridatainmemory zugeordnet wird.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Funktionen von mrmfrememory-Funktionen und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339364"
---
# <a name="mrmfreememory-function"></a>Mrmfrememory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Gibt Arbeitsspeicher frei, der von [**mrmkreateconfiginmemory**](mrmcreateconfiginmemory.md), [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md), [**mrmdumpprifileinmemory**](mrmdumpprifileinmemory.md)und [**mrmdumppridatainmemory**](mrmdumppridatainmemory.md)zugeordnet wird. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Daten* \[ in\]
</dt> <dd>

Typ: **Byte \** _

Ein Zeiger auf den Arbeitsspeicher, der [von *_ mrmkreateconfiginmemory* *](mrmcreateconfiginmemory.md), [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md), [**mrmdumpprifileinmemory**](mrmdumpprifileinmemory.md)oder [**mrmdumppridatainmemory**](mrmdumppridatainmemory.md)zugeordnet und zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1803, \[ nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Mrmresourceingedexer. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

