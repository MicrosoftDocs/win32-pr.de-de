---
title: MrmDumpPriDataInMemory-Funktion (MrmResourceIndexer.h)
description: Gibt PRI-Informationen (als Blob im Arbeitsspeicher, das durch einen vorherigen Aufruf von MrmCreateResourceFileInMemory erstellt wurde) in die xml-Entsprechung (als In-Memory-Daten) zurück, um sie leichter lesbar zu machen.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menüs und andere Ressourcen der MrmDumpPriDataInMemory-Funktion
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbeec26f0741ebb77b742ff647e91cb5fd18afe633a1519228b887b4b438bb72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601780"
---
# <a name="mrmdumppridatainmemory-function"></a>MrmDumpPriDataInMemory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Gibt PRI-Informationen (als Blob im Arbeitsspeicher, das durch einen vorherigen Aufruf von [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)erstellt wurde) in die xml-Entsprechung (als In-Memory-Daten) zurück, um sie leichter lesbar zu machen. Die Funktion belegt Arbeitsspeicher und gibt einen Zeiger auf diesen Speicher in *outputXmlData* zurück. Rufen Sie [**MrmFreeMemory**](mrmfreememory.md) mit dem gleichen Zeiger auf, um diesen Arbeitsspeicher freizugeben. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für [die Paketressourcenindizierung (PACKAGE Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inputPriData* \[ In\]
</dt> <dd>

Typ: **BYTE \***

Ein Zeiger auf PRI-Daten, die durch einen vorherigen Aufruf von [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)erstellt wurden.

</dd> <dt>

*inputPriSize* \[ In\]
</dt> <dd>

Typ: **ULONG**

Die Größe der Daten, auf die *inputPriData* zeigt.

</dd> <dt>

*schemaPriData* \[ in, optional\]
</dt> <dd>

Typ: **BYTE \***

Ein optionaler Zeiger auf PRI-Informationen (als Blob im Arbeitsspeicher), die Schemadaten darstellen, die durch einen vorherigen Aufruf von [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)erstellt wurden. Geben Sie *schemaPriData* erst frei, nachdem Sie den Ressourcenindexer verwendet haben. Siehe auch Hinweise.

</dd> <dt>

*schemaPriSize* \[ In\]
</dt> <dd>

Typ: **ULONG**

Die Größe der Daten, auf die *schemaPriData* zeigt.

</dd> <dt>

*dumpType* \[ In\]
</dt> <dd>

Typ: **[ **MrmDumpType**](mrmdumptype.md)**

Gibt an, wie detailliert das XML-Dump sein soll oder ob ein Schema gedumpt werden soll.

</dd> <dt>

*outputXmlData* \[ out\]
</dt> <dd>

Typ: **BYTE \* \***

Die Adresse eines Zeigers auf BYTE. Die Funktion belegt Arbeitsspeicher und gibt einen Zeiger auf diesen Speicher in *outputXmlData* zurück. Rufen Sie [**MrmFreeMemory**](mrmfreememory.md) mit Ihrem Zeiger auf BYTE auf, um diesen Arbeitsspeicher freizugeben.

</dd> <dt>

*outputXmlSize* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Die Adresse eines ULONG. In *outputXmlSize* gibt die Funktion die Größe des zugeordneten Arbeitsspeichers zurück, auf den *outputXmlData* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um erfolg- oder fehlerbestimmend zu sein.

## <a name="remarks"></a>Hinweise

Ein schemafreies Ressourcenpaket wurde mit dem [**MrmPackagingOptionsOmitSchemaFromResourcePacks-Argument**](mrmpackagingoptions.md) erstellt, das an [**MrmCreateResourceFile**](mrmcreateresourcefile.md) oder [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) übergeben wurde (oder mit dem Schalter *omitSchemaFromResourcePacks* in der PRI-Konfigurationsdatei). Um ein schemafreies Ressourcenpaket zu speichern, übergeben Sie den Pfad zu Den PRI-Hauptpaketdaten als Argument für den *parameter schemaPriData.*

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

 

