---
title: Mrmindexresourcecontainerautoqualifiqualifizierungsfunktion (mrmresourceingedexer. h)
description: Indiziert die Zeichen folgen Ressourcen, die in einer Ressourcen Datei (. resw/. resjson) oder einer priinfo-oder prifile-Datei enthalten sind, die zu einer UWP-App gehört.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Funktionen von mrmindexresourcecontainerautoqualifizierern und anderen Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344703"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a>Mrmindexresourcecontainerautoqualifiqualifizierungfunktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Indiziert die Zeichen folgen Ressourcen, die in einer Ressourcen Datei (. resw/. resjson) oder einer priinfo-oder prifile-Datei enthalten sind, die zu einer UWP-App gehört. Leitet eine Liste von Ressourcen Qualifizierern aus dem *Container Path* -Parameter ab. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Indexer* \[ in\]
</dt> <dd>

Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den ressourcenindexer identifiziert, der die Zeichen folgen Ressourcen indiziert.

</dd> <dt>

*ContainerPath* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Ein relativer Pfad zu einer. resw-, resjson-, priinfo-oder prifile-Datei, die Zeichen folgen Ressourcen enthält, die Sie indizieren möchten. Dieser Pfad ist relativ zum Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen. Der Projektstamm ist der Wert von *projectroot* , den Sie an [**mrmkreateresourceingedexer**](mrmcreateresourceindexer.md)übergeben haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

## <a name="remarks"></a>Bemerkungen

Ressourcen Qualifizierer werden aus *ContainerPath* abgeleitet. Beispielsweise fügt der Wert L "en-US \\ \\ Resources. resw" Zeichen folgen Ressourcen mit dem Qualifizierer "language-en-US" hinzu.

Der Name der Ressourcen Datei wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressourcen verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.

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

 

