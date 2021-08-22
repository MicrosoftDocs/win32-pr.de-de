---
title: MrmCreateResourceIndexer-Funktion (MrmResourceIndexer.h)
description: Erstellt einen Ressourcenindexer, der zum Generieren von Paketressourcenindexdateien (PRI) für eine UWP-App verwendet wird. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (Package Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- MrmCreateResourceIndexer-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d427163862d084c4a386fdf47cbd8586cb1a3489b18fb081471fbd31c86854b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601810"
---
# <a name="mrmcreateresourceindexer-function"></a>MrmCreateResourceIndexer-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt einen Ressourcenindexer, der zum Generieren von Paketressourcenindexdateien (PRI) für eine UWP-App verwendet wird. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packageFamilyName* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Der Paketfamilienname der UWP-App, für die Sie PRI-Dateien generieren. Dieser Wert wird als Ressourcenzuordnungsname verwendet, wenn Sie später eine PRI-Datei aus diesem Ressourcenindexer generieren.

</dd> <dt>

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
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1803 \[\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur \[ Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

