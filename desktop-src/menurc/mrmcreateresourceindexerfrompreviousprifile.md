---
title: Mrmkreateresourceindexerfrompreviousprifile-Funktion (mrmresourceindexer. h)
description: Erstellt einen ressourcenindexer aus einer PRI-Datei, die mit einem vorherigen Aufruf von mrmkreateresourcefile erstellt wurde. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Mrmcreateresourceindexerfrompreviousprifile-Funktions Menüs und weitere Ressourcen
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
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340795"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a>Mrmkreateresourceindexerfrompreviousprifile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt einen ressourcenindexer aus einer PRI-Datei, die mit einem vorherigen Aufruf von [**mrmkreateresourcefile**](mrmcreateresourcefile.md)erstellt wurde. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*prifile* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Ein vollständiger Dateipfad zu einer PRI-Datei.

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

 

