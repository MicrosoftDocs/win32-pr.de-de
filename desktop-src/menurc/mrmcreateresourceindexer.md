---
title: Mrmkreateresourceingedexer-Funktion (mrmresourceingedexer. h)
description: Erstellt einen ressourcenindexer, der zum Generieren von PRI-Dateien (Package Resource Index) für eine UWP-App verwendet wird. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Funktionen von mrmcreateresourcindexer Functions und andere Ressourcen
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
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392144"
---
# <a name="mrmcreateresourceindexer-function"></a>Mrmkreateresourceingedexer-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt einen ressourcenindexer, der zum Generieren von PRI-Dateien (Package Resource Index) für eine UWP-App verwendet wird. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*packagefamilyname* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Der Paket Familienname der UWP-APP, für die Sie pri-Dateien erstellen. Dieser Wert wird als Ressourcen Zuordnungs Name verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.

</dd> <dt>

*projectroot* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Der Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen. Anders ausgedrückt: der Pfad zu den Ressourcen Dateien dieser app. Sie geben diese Angabe an, damit Sie in nachfolgenden API-aufrufen desselben ressourcenindexers Pfade relativ zu diesem Stamm angeben können.

</dd> <dt>

*platformversion* \[ in\]
</dt> <dd>

Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**

Die Version der Zielplattform für den ressourcenindexer.

</dd> <dt>

*defaultqualifizierer* \[ in, optional\]
</dt> <dd>

Typ: **pcwstr**

Eine Liste der Standard Ressourcen Qualifizierer. Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"

</dd> <dt>

*Indexer* \[ in, out\]
</dt> <dd>

Typ: **[**mrmresourceindexerhandle**](mrmresourceindexerhandle.md) \** _

Ein Zeiger auf ein ressourcenindexer-handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

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

 

