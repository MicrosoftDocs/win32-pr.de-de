---
title: MrmCreateResourceIndexerFromPreviousPriFile-Funktion (MrmResourceIndexer.h)
description: Erstellt einen Ressourcenindexer aus einer PRI-Datei, die mit einem vorherigen Aufruf von MrmCreateResourceFile erstellt wurde. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Menüs und andere Ressourcen der MrmCreateResourceIndexerFromPreviousPriFile-Funktion
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e820ce2dee747165720e0e47388ec6e66104340dec77bf9617569b2b0a797d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733670"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a>MrmCreateResourceIndexerFromPreviousPriFile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt einen Ressourcenindexer aus einer PRI-Datei, die mit einem vorherigen Aufruf von [**MrmCreateResourceFile**](mrmcreateresourcefile.md)erstellt wurde. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für [die Paketressourcenindizierung (PACKAGE Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*projectRoot* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Der Projektstamm der UWP-App, für die Sie PRI-Dateien generieren. Das heißt, der Pfad zu den Ressourcendateien dieser App. Sie geben dies so an, dass Sie dann pfade relativ zu diesem Stamm in nachfolgenden API-Aufrufen an denselben Ressourcenindexer angeben können.

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

*priFile* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Ein vollständiger Dateipfad zu einer PRI-Datei.

</dd> <dt>

*Indexer* \[ in, out\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Ein Zeiger auf ein Ressourcenindexerhandle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um erfolg- oder fehlerbestimmend zu sein.

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

 

