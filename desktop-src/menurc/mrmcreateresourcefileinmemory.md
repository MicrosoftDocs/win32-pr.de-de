---
title: Mrmkreateresourcefilinput Memory-Funktion (mrmresourceingedexer. h)
description: Erstellt PRI-Informationen als BLOB im Speicher, nicht als Datei auf dem Datenträger.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Funktionen von "mrmcreateresourcefilinput Memory" und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478651"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>Mrmkreateresourcefilinput Memory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt PRI-Informationen als BLOB im Speicher, nicht als Datei auf dem Datenträger. Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputpridata* zurück. Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Indexer* \[ in\]
</dt> <dd>

Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den ressourcenindexer identifiziert, von dem die PRI-Informationen erstellt werden sollen.

</dd> <dt>

*packagingmode* \[ in\]
</dt> <dd>

Typ: **[ **mrmpackagingmode**](mrmpackagingmode.md)**

Gibt an, ob die PRI-Informationen eigenständig oder ein Ressourcenpaket sein sollen. **Mrmpackagingmodeautosplit** wird nicht unterstützt.

</dd> <dt>

*packagingoptions* \[ in\]
</dt> <dd>

Typ: **[ **mrmpackagingoptions**](mrmpackagingoptions.md)**

Gibt zusätzliche Optionen zu den PRI-Informationen an.

</dd> <dt>

*outputpridata* \[ vorgenommen\]
</dt> <dd>

Type: **Byte \* \***

Die Adresse eines Zeigers auf ein Byte. Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputpridata* zurück. Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem Zeiger auf Byte, um diesen Arbeitsspeicher freizugeben.

</dd> <dt>

*outputprisize* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Die Adresse eines ulong. In _outputPriSize * gibt die-Funktion die Größe des belegten Speichers zurück, auf den von *outputpridata* verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

## <a name="remarks"></a>Bemerkungen

Wenn Sie *outputpridata* an [**mrmkreateresourcindexerfrompreviouspridata**](mrmcreateresourceindexerfrompreviouspridata-.md)übergeben, geben Sie den Arbeitsspeicher erst frei, nachdem Sie den ressourcenindexer verwendet haben.

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

 

