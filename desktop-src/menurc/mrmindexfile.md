---
title: Mrmindexfile-Funktion (mrmresourceindexer. h)
description: Indiziert eine Ressourcen Datei, die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcen Qualifizierern an. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Funktionen der mrtrexfile-Funktion und weitere Ressourcen
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
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478645"
---
# <a name="mrmindexfile-function"></a>Mrmindexfile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Indiziert eine Ressourcen Datei, die zu einer UWP-App gehört. Nimmt eine explizite (aber optionale) Liste von Ressourcen Qualifizierern an. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*Indexer* \[ in\]
</dt> <dd>

Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den ressourcenindexer identifiziert, der die Ressourcen Datei indiziert.

</dd> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Der Ressourcen-URI, der der Ressource zugewiesen werden soll. Der Pfad wird als Name der Unterstruktur der Ressourcen Zuordnung für diese Ressource verwendet, wenn Sie später eine PRI-Datei von diesem ressourcenindexer generieren.

</dd> <dt>

*FilePath* \[ in\]
</dt> <dd>

Typ: **pcwstr**

Ein relativer Pfad zu einer Datei, die eine Ressource enthält, die Sie indizieren möchten. Dieser Pfad ist relativ zum Projektstamm der UWP-APP, für die Sie pri-Dateien erstellen. Der Projektstamm ist der Wert von *projectroot* , den Sie an [**mrmkreateresourceingedexer**](mrmcreateresourceindexer.md)übergeben haben.

</dd> <dt>

*Qualifizierer* \[ in, optional\]
</dt> <dd>

Typ: **pcwstr**

Eine optionale Liste der Ressourcen Qualifizierer, z. b. L "language-en-US \_ Scale-100 \_ Contrast-Standard". Eine leere Zeichenfolge oder **nullptr** weist auf eine neutrale Ressource hin. Ressourcen Qualifizierer werden *nicht* von *resourceUri* und *ContainerPath* abgeleitet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros Success () oder failed () (in WinError. h definiert), um den Erfolg oder Misserfolg zu ermitteln.

## <a name="remarks"></a>Bemerkungen

Wenn Sie Ressourcen Qualifizierer angeben möchten, übergeben Sie Sie an den *Qualifizierer* -Parameter. Ressourcen Qualifizierer werden *nicht* von *resourceUri* oder von *FilePath* abgeleitet.

Das Dateinamen Segment von *resourceUri* (nicht *FilePath*) wird als Ressourcen Name verwendet.

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

 

