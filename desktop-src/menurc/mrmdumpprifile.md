---
title: Mrmdumpprifile-Funktion (mrmresourceindexer. h)
description: Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als Datei auf dem Datenträger), um Sie leichter lesbar zu machen.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Funktionen der mrmdumpprifile-Funktion und weitere Ressourcen
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741825"
---
# <a name="mrmdumpprifile-function"></a>Mrmdumpprifile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Sichert eine PRI-Datei (die binär ist) in Ihre XML-Entsprechung (als Datei auf dem Datenträger), um Sie leichter lesbar zu machen. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
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

*outputxmlfile* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Der Pfad einer XML-Datei, die erstellt werden soll.

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

 

