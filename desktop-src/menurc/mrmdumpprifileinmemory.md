---
title: Mrmdumpprifilinput Memory-Funktion (mrmresourceingedexer. h)
description: Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Funktionen von "mrmdumpprifilinput Memory" und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338118"
---
# <a name="mrmdumpprifileinmemory-function"></a>Mrmdumpprifilinput Memory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als in-Memory-Daten), um Sie leichter lesbar zu machen. Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück. Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*indexfilename* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Ein vollständiger Dateipfad zu einer PRI-Datei. Dies ist die PRI-Datei, die in XML gekippt wird.

</dd> <dt>

*schemaprifile* \[ in, optional\]
</dt> <dd>

Typ: **pcwstr**

Ein optionaler Vollständiger Dateipfad zu einer Schema Datei (oder zu einer PRI-Datei, die ein Schema darstellt. siehe Hinweise).

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

Ein Schema freies Ressourcenpaket, das mit dem " [**mrmpackagingoptionsomitschemafromresourcepacks**](mrmpackagingoptions.md) "-Argument erstellt wurde, das an [**mrmkreateresourcefile**](mrmcreateresourcefile.md) oder [**mrmkreateresourcefileinmemory**](mrmcreateresourcefileinmemory.md) übergeben wurde (oder mit dem Schalter *omitschemafromresourcepacks* in der PRI-Konfigurationsdatei). Zum Sichern eines Ressourcen Pakets mit Schema freiem Speicher übergeben Sie den Pfad zu ihren Hauptpaket-PRI-Daten als Argument für den *schemaprifile* -Parameter.

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

 

