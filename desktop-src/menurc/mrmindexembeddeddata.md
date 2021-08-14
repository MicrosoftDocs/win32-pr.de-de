---
title: MrmIndexEmbeddedData-Funktion (MrmResourceIndexer.h)
description: Indiziert eine einzelne embeddeddata-Ressource, die zu einer UWP-App gehört.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- MrmIndexEmbeddedData-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7897df30506b66e74122c238e25a5b20fa5e1635e299c8a08db2519c842bdf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971999"
---
# <a name="mrmindexembeddeddata-function"></a>MrmIndexEmbeddedData-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Indiziert eine einzelne **embeddeddata-Ressource,** die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcenqualifizierern an. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
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

*embeddedData* \[ In\]
</dt> <dd>

Typ: **const \* BYTE**

Ein Zeiger auf die Daten der Ressource, die Sie indizieren möchten.

</dd> <dt>

*embeddedDataSize* \[ In\]
</dt> <dd>

Typ: **ULONG**

Die Größe der Daten, auf die *embeddedData zeigt.*

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
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1803 \[\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur \[ Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

