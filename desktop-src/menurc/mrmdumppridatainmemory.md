---
title: Mrmdumppridatainmemory-Funktion (mrmresourceindexer. h)
description: Sichert PRI-Informationen (als BLOB im Arbeitsspeicher, erstellt durch einen vorherigen-Befehl von mrmkreateresourcefileinmemory) an die zugehörige XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Funktionen von mrmdumppridatainmemory-Funktionen und andere Ressourcen
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
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345505"
---
# <a name="mrmdumppridatainmemory-function"></a>Mrmdumppridatainmemory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Sichert PRI-Informationen (als BLOB im Arbeitsspeicher, erstellt durch einen vorherigen-Befehl von [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md)) an die zugehörige XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen. Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück. Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*inputpridata* \[ in\]
</dt> <dd>

Typ: **Byte \** _

Ein Zeiger auf PRI-Daten, die durch einen vorherigen-Befehl von [_ *mrmkreateresourcefileinmemory* *](mrmcreateresourcefileinmemory.md)erstellt wurden.

</dd> <dt>

*Input prisize* \[ in\]
</dt> <dd>

Typ: **ulong**

Die Größe der Daten, auf die von *inputpridata* verwiesen wird.

</dd> <dt>

*schemapridata* \[ in, optional\]
</dt> <dd>

Typ: **Byte \** _

Ein optionaler Zeiger auf PRI Info (als BLOB im Arbeitsspeicher), der Schema Daten darstellt, die durch einen vorherigen-Befehl von [_ *mrmkreateresourcefileinmemory* *](mrmcreateresourcefileinmemory.md)erstellt wurden. Machen Sie *schemapridata* erst frei, wenn Sie die Verwendung des ressourcenindexers abgeschlossen haben. Siehe auch Hinweise.

</dd> <dt>

*schemaprisize* \[ in\]
</dt> <dd>

Typ: **ulong**

Die Größe der Daten, auf die von *schemapridata* verwiesen wird.

</dd> <dt>

*dumptype* \[ in\]
</dt> <dd>

Typ: **[ **mrmdumptype**](mrmdumptype.md)**

Gibt an, wie detailliert das XML-Dump sein soll oder ob ein Schema gekippt werden soll.

</dd> <dt>

*outputxmldata* \[ vorgenommen\]
</dt> <dd>

Type: **Byte \* \***

Die Adresse eines Zeigers auf ein Byte. Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück. Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem Zeiger auf Byte, um diesen Arbeitsspeicher freizugeben.

</dd> <dt>

*outputxmlsize* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Die Adresse eines ulong. In _outputXmlSize * gibt die-Funktion die Größe des belegten Speichers zurück, auf den von *outputxmldata* verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

## <a name="remarks"></a>Bemerkungen

Ein Schema freies Ressourcenpaket, das mit dem " [**mrmpackagingoptionsomitschemafromresourcepacks**](mrmpackagingoptions.md) "-Argument erstellt wurde, das an [**mrmkreateresourcefile**](mrmcreateresourcefile.md) oder [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md) übergeben wurde (oder mit dem Schalter *omitschemafromresourcepacks* in der PRI-Konfigurationsdatei). Zum Sichern eines Ressourcen Pakets, das Schema frei ist, übergeben Sie den Pfad zu ihren Hauptpaket-PRI-Daten als Argument für den *schemapridata* -Parameter.

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

 

