---
title: MrmCreateResourceFileInMemory-Funktion (MrmResourceIndexer.h)
description: Erstellt PRI-Informationen als Blob im Arbeitsspeicher, nicht als Datei auf dem Datenträger.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menüs und andere Ressourcen der MrmCreateResourceFileInMemory-Funktion
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
ms.openlocfilehash: ff34ddaab25f47f537c1270ad3a70719a43e2e1efa978fbad19cbe9ae77ba937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886750"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>MrmCreateResourceFileInMemory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt PRI-Informationen als Blob im Arbeitsspeicher, nicht als Datei auf dem Datenträger. Die Funktion belegt Arbeitsspeicher und gibt einen Zeiger auf diesen Speicher in *outputPriData* zurück. Rufen Sie [**MrmFreeMemory**](mrmfreememory.md) mit dem gleichen Zeiger auf, um diesen Arbeitsspeicher freizugeben. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für [die Paketressourcenindizierung (PACKAGE Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

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

*Indexer* \[ In\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den Ressourcenindexer identifiziert, aus dem die PRI-Informationen erstellt werden sollen.

</dd> <dt>

*packagingMode* \[ In\]
</dt> <dd>

Typ: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Gibt an, ob die PRI-Informationen eigenständig oder ein Ressourcenpaket sein sollen. **MrmPackagingModeAutoSplit** wird nicht unterstützt.

</dd> <dt>

*packagingOptions* \[ In\]
</dt> <dd>

Typ: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Gibt zusätzliche Optionen zu den PRI-Informationen an.

</dd> <dt>

*outputPriData* \[ out\]
</dt> <dd>

Typ: **BYTE \* \***

Die Adresse eines Zeigers auf BYTE. Die Funktion belegt Arbeitsspeicher und gibt einen Zeiger auf diesen Speicher in *outputPriData* zurück. Rufen Sie [**MrmFreeMemory**](mrmfreememory.md) mit Ihrem Zeiger auf BYTE auf, um diesen Arbeitsspeicher freizugeben.

</dd> <dt>

*outputPriSize* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Die Adresse eines ULONG. In *outputPriSize* gibt die Funktion die Größe des zugeordneten Arbeitsspeichers zurück, auf den *outputPriData* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um erfolg- oder fehlerbestimmend zu sein.

## <a name="remarks"></a>Hinweise

Wenn Sie *outputPriData* an [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md)übergeben, geben Sie den Arbeitsspeicher erst frei, nachdem Sie den Ressourcenindexer verwendet haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1803 \[\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows \[Nur Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

