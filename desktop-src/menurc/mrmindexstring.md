---
title: MrmIndexString-Funktion (MrmResourceIndexer.h)
description: Indiziert eine einzelne Zeichenfolgenressource, die zu einer UWP-App gehört.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- MrmIndexString-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99da5b63c08d0068553ca9240798eabe360671fa94139b31841831dd68df3958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687252"
---
# <a name="mrmindexstring-function"></a>MrmIndexString-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Indiziert eine einzelne Zeichenfolgenressource, die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcenqualifizierern an. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Indexer* \[ In\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den Ressourcenindexer identifiziert, der die Zeichenfolgenressourcen indiziert.

</dd> <dt>

*resourceUri* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Der Ressourcen-URI, der der Ressource zugewiesen werden soll. Der Pfad wird als Name der Ressourcenzuordnungsunterstruktur für diese Ressource verwendet, wenn Sie später eine PRI-Datei aus diesem Ressourcenindexer generieren.

</dd> <dt>

*resourceString* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Der Wert der Zeichenfolgenressource.

</dd> <dt>

*Qualifizierer* \[ in, optional\]
</dt> <dd>

Typ: **PCWSTR**

Eine optionale Liste von Ressourcenqualifizierern, z.B. L"language-en-US \_ scale-100 \_ contrast-standard". Eine leere Zeichenfolge oder **nullptr gibt** eine neutrale Ressource an. Ressourcenqualifizierer *werden nicht* von *resourceUri abgeleitet.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um den Erfolg oder Fehler zu bestimmen.

## <a name="remarks"></a>Hinweise

Wenn Sie Ressourcenqualifizierer angeben möchten, übergeben Sie sie im *Qualifiziererparameter.* Ressourcenqualifizierer *werden nicht* von *resourceUri abgeleitet.*

Das Dateinamensegment *von resourceUri* wird als Ressourcenname verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1803 desktop apps only (Nur \[ Desktop-Apps der Version 1803)\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur \[ Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

