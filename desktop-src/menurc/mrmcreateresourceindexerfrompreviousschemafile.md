---
title: MrmCreateResourceIndexerFromPreviousSchemaFile-Funktion (MrmResourceIndexer.h)
description: Erstellt einen Ressourcenindexer aus einer Schemadatei, die mit einem vorherigen Aufruf von MrmDumpPriFile erstellt wurde. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (Package Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- MrmCreateResourceIndexerFromPreviousSchemaFile-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622fe76c9206b4a8223d27d810f3d02bc0dca1d08730623b595ead24eab719d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847370"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a>MrmCreateResourceIndexerFromPreviousSchemaFile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt einen Ressourcenindexer aus einer Schemadatei, die mit einem vorherigen Aufruf von [**MrmDumpPriFile erstellt wurde.**](mrmdumpprifile.md) Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*projectRoot* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Der Projektstamm der UWP-App, für die Sie PRI-Dateien generieren. Das heißt, der Pfad zu den Ressourcendateien dieser App. Sie geben dies an, damit Sie in nachfolgenden API-Aufrufen desselben Ressourcenindexers Pfade relativ zu diesem Stamm angeben können.

</dd> <dt>

*platformVersion* \[ In\]
</dt> <dd>

Typ: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Die Zielplattformversion für den Ressourcenindexer.

</dd> <dt>

*defaultQualifiers* \[ in, optional\]
</dt> <dd>

Typ: **PCWSTR**

Eine Liste der Standardressourcenqualifizierer. Beispiel: L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*schemaFile* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Ein vollständiger Dateipfad zu einer Schemadatei, die durch einen vorherigen Aufruf von [**MrmDumpPriFile erstellt wurde.**](mrmdumpprifile.md)

</dd> <dt>

*Indexer* \[ in, out\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Ein Zeiger auf ein Ressourcenindexerhand handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um den Erfolg oder Fehler zu bestimmen.

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

 

