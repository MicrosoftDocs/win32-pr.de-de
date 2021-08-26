---
title: MrmDumpPriFileInMemory-Funktion (MrmResourceIndexer.h)
description: Gibt eine PRI-Datei (binär) in der XML-Entsprechung (als In-Memory-Daten) ab, um sie leichter lesbar zu machen.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- MrmDumpPriFileInMemory-Funktionsmenüs und andere Ressourcen
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
ms.openlocfilehash: 17c591f95b772d71fd0ce614598bbf793d84dff70a0c29664da460c8be33569d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092150"
---
# <a name="mrmdumpprifileinmemory-function"></a>MrmDumpPriFileInMemory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Gibt eine PRI-Datei (binär) in der XML-Entsprechung (als In-Memory-Daten) ab, um sie leichter lesbar zu machen. Die Funktion weist Arbeitsspeicher zu und gibt einen Zeiger auf diesen Arbeitsspeicher in *outputXmlData zurück.* Rufen [**Sie MrmFreeMemory**](mrmfreememory.md) mit demselben Zeiger auf, um diesen Arbeitsspeicher frei zu geben. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

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

*indexFileName* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Ein vollständiger Dateipfad zu einer PRI-Datei. Dies ist die PRI-Datei, die in XML gespeichert wird.

</dd> <dt>

*schemaPriFile* \[ in, optional\]
</dt> <dd>

Typ: **PCWSTR**

Ein optionaler vollständiger Dateipfad zu einer Schemadatei (oder zu einer PRI-Datei, die ein Schema darstellt; siehe Hinweise).

</dd> <dt>

*dumpType* \[ In\]
</dt> <dd>

Typ: **[ **MrmDumpType**](mrmdumptype.md)**

Gibt an, wie detailliert das XML-Speicherabbild sein soll oder ob ein Schema gedumpt werden soll.

</dd> <dt>

*outputXmlData* \[ out\]
</dt> <dd>

Typ: **BYTE \* \***

Die Adresse eines Zeigers auf BYTE. Die Funktion weist Arbeitsspeicher zu und gibt einen Zeiger auf diesen Arbeitsspeicher in *outputXmlData zurück.* Rufen [**Sie MrmFreeMemory mit**](mrmfreememory.md) Ihrem Zeiger auf BYTE auf, um diesen Arbeitsspeicher frei zu geben.

</dd> <dt>

*outputXmlSize* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Die Adresse eines ULONG. In *outputXmlSize gibt* die Funktion die Größe des zugeordneten Arbeitsspeichers zurück, auf den *outputXmlData zeigt.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um den Erfolg oder Fehler zu bestimmen.

## <a name="remarks"></a>Hinweise

Ein schemafreies Ressourcenpaket wurde mit dem [**MrmPackagingOptionsOmitSchemaFromResourcePacks-Argument**](mrmpackagingoptions.md) erstellt, das an [**MrmCreateResourceFile**](mrmcreateresourcefile.md) oder [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (oder mit dem Schalter *omitSchemaFromResourcePacks* in der PRI-Konfigurationsdatei) übergeben wurde. Um ein schemafreies Ressourcenpaket zu erstellen, übergeben Sie den Pfad zu Ihren PRI-Hauptpaketdaten als Argument für den *parameter schemaPriFile.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1803 desktop apps only (Nur \[ Desktop-Apps der Version 1803)\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur \[ Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

