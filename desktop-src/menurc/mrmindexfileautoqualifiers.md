---
title: MrmIndexFileAutoQualifiers-Funktion (MrmResourceIndexer.h)
description: Indiziert eine Ressourcendatei, die zu einer UWP-App gehört. Abgeleitet eine Liste von Ressourcenqualifizierern aus dem filePath-Parameter. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (Package Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- MrmIndexFileAutoQualifiers-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10dbdb564f7e2d830d1edea59be6ca6f11b72d2650a937f96b6d305b6c7f61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886730"
---
# <a name="mrmindexfileautoqualifiers-function"></a>MrmIndexFileAutoQualifiers-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Indiziert eine Ressourcendatei, die zu einer UWP-App gehört. Abgeleitet eine Liste von Ressourcenqualifizierern aus dem *filePath-Parameter.* Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Indexer* \[ In\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den Ressourcenindexer identifiziert, der die Ressourcendatei indiziert.

</dd> <dt>

*filePath* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Ein relativer Pfad zu einer Datei, die eine Ressource enthält, die Sie indizieren möchten. Dieser Pfad ist relativ zum Projektstamm der UWP-App, für die Sie PRI-Dateien generieren. Dieser Projektstamm ist der Wert von *projectRoot,* den Sie an [**MrmCreateResourceIndexer übergeben haben.**](mrmcreateresourceindexer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um den Erfolg oder Fehler zu bestimmen.

## <a name="remarks"></a>Hinweise

Das Dateinamensegment von *filePath* wird als Ressourcenname verwendet. und Ressourcenqualifizierer werden von ihrem Pfad abgeleitet. Wenn Sie beispielsweise L"Images de-DE scale-100background.png" an filePath übergeben, fügt der Ressourcenindexer eine Ressource namens "background.png" mit den \\ \\ \\ Ressourcenqualifizierern "language-de-DE" und "scale-100" hinzu. 

L"Files" wird als Name der Ressourcenzuordnungsunterstruktur für diese Ressource verwendet, wenn Sie später eine PRI-Datei aus diesem Ressourcenindexer generieren.

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

 

