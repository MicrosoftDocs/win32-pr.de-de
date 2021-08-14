---
title: MrmIndexFile-Funktion (MrmResourceIndexer.h)
description: Indiziert eine Ressourcendatei, die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcenqualifizierern an. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- MrmIndexFile-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004e8d81f3af7d0aa7844ed5661f71713db3f7fc49616fba0d56bed833a87f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733680"
---
# <a name="mrmindexfile-function"></a>MrmIndexFile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Indiziert eine Ressourcendatei, die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcenqualifizierern an. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für [die Paketressourcenindizierung (PACKAGE Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Indexer* \[ In\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den Ressourcenindexer identifiziert, der die Ressourcendatei indiziert.

</dd> <dt>

*resourceUri* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Der Ressourcen-URI, der der Ressource zugewiesen werden soll. Der Pfad wird als Name der Ressourcenzuordnungsunterstruktur für diese Ressource verwendet, wenn Sie später eine PRI-Datei aus diesem Ressourcenindexer generieren.

</dd> <dt>

*filePath* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Ein relativer Pfad zu einer Datei, die eine Ressource enthält, die Sie indizieren möchten. Dieser Pfad ist relativ zum Projektstamm der UWP-App, für die Sie PRI-Dateien generieren. Dieser Projektstamm ist der Wert von *projectRoot,* den Sie an [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)übergeben haben.

</dd> <dt>

*Qualifizierer* \[ in, optional\]
</dt> <dd>

Typ: **PCWSTR**

Eine optionale Liste von Ressourcenqualifizierern, z.B. L"language-en-US \_ scale-100 \_ contrast-standard". Eine leere Zeichenfolge oder **nullptr** gibt eine neutrale Ressource an. Ressourcenqualifizierer werden *weder* von *resourceUri* noch von *containerPath* abgeleitet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um erfolg- oder fehlerbestimmend zu sein.

## <a name="remarks"></a>Hinweise

Wenn Sie Ressourcenqualifizierer angeben möchten, übergeben Sie sie im *Qualifiziererparameter.* Ressourcenqualifizierer werden *weder* von *resourceUri* noch von *filePath* abgeleitet.

Das Dateinamensegment von *resourceUri* (nicht *filePath*) wird als Ressourcenname verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1803 \[\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows \[Nur Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

