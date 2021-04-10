---
title: Mrmindexstring-Funktion (mrmresourcumdexer. h)
description: Indiziert eine einzelne Zeichen folgen Ressource, die zu einer UWP-App gehört.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Funktionen von mrmindexstring-Funktionen und andere Ressourcen
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
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102990"
---
# <a name="mrmindexstring-function"></a>Mrmindexstring-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Indiziert eine einzelne Zeichen folgen Ressource, die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcen Qualifizierern an. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*Indexer* \[ in\]
</dt> <dd>

Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den ressourcenindexer identifiziert, der die Zeichen folgen Ressourcen indiziert.

</dd> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Der Ressourcen-URI, der der Ressource zugewiesen werden soll. Der Pfad wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressource verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.

</dd> <dt>

*resourcestring* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Der Wert der Zeichen folgen Ressource.

</dd> <dt>

*Qualifizierer* \[ in, optional\]
</dt> <dd>

Typ: **pcwstr**

Eine optionale Liste der Ressourcen Qualifizierer, z. b. L "language-en-US \_ Scale-100 \_ Contrast-Standard". Eine leere Zeichenfolge oder **nullptr** weist auf eine neutrale Ressource hin. Ressourcen Qualifizierer werden *nicht* von *resourceUri* abgeleitet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

## <a name="remarks"></a>Bemerkungen

Wenn Sie Ressourcen Qualifizierer angeben möchten, übergeben Sie Sie an den *Qualifizierer* -Parameter. Ressourcen Qualifizierer werden *nicht* von *resourceUri* abgeleitet.

Das Dateinamen Segment von *resourceUri* wird als Ressourcen Name verwendet.

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

 

