---
title: MrmCreateResourceIndexerFromPreviousPriData-Funktion (MrmResourceIndexer.h)
description: Erstellt einen Ressourcenindexer aus PRI-Daten, die durch einen vorherigen Aufruf von MrmCreateResourceFileInMemory erstellt wurden. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (Package Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- MrmCreateResourceIndexerFromPreviousPriData-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d178532a77e01bc724276b40881685e0ec44d5364617fd856ffc55acfd99cf98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952352"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a>MrmCreateResourceIndexerFromPreviousPriData-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt einen Ressourcenindexer aus PRI-Daten, die durch einen vorherigen Aufruf von [**MrmCreateResourceFileInMemory erstellt wurden.**](mrmcreateresourcefileinmemory.md) Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
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

*priData* \[ In\]
</dt> <dd>

Typ: **BYTE \***

Ein Zeiger auf PRI-Daten, die durch einen vorherigen Aufruf von [**MrmCreateResourceFileInMemory erstellt wurden.**](mrmcreateresourcefileinmemory.md) Geben Sie *priData erst frei,* nachdem Sie die Verwendung des von dieser Funktion erstellten Ressourcenindexers abgeschlossen haben.

</dd> <dt>

*priSize* \[ In\]
</dt> <dd>

Typ: **ULONG**

Die Größe der Daten, auf die *priData zeigt.*

</dd> <dt>

*Indexer* \[ in, out\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Ein Zeiger auf ein Ressourcenindexerhand handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um den Erfolg oder Fehler zu bestimmen.

## <a name="remarks"></a>Hinweise

Geben Sie *priData erst frei,* nachdem Sie die Verwendung des von dieser Funktion erstellten Ressourcenindexers abgeschlossen haben.

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

 

