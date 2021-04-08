---
title: Mrmkreateresourcefile-Funktion (mrmresourceindexer. h)
description: Erstellt eine PRI-Datei (mit dem Namen \ 0034; Resources. pri \ 0034;) oder Dateien auf dem Datenträger im angegebenen Ordner. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Mrmcreateresourcefile-Funktions Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743064"
---
# <a name="mrmcreateresourcefile-function"></a>Mrmkreateresourcefile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt eine PRI-Datei (mit dem Namen "Resources. pri") oder Dateien auf dem Datenträger im angegebenen Ordner. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Indexer* \[ in\]
</dt> <dd>

Typ: **[ **mrmresourceindexerhandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den ressourcenindexer identifiziert, von dem die PRI-Datei erstellt werden soll.

</dd> <dt>

*packagingmode* \[ in\]
</dt> <dd>

Typ: **[ **mrmpackagingmode**](mrmpackagingmode.md)**

Gibt an, ob die PRI-Datei eigenständig sein soll, automatisch nach Ressourcen Qualifizierer aufgeteilt werden oder ein Ressourcenpaket sein soll.

</dd> <dt>

*packagingoptions* \[ in\]
</dt> <dd>

Typ: **[ **mrmpackagingoptions**](mrmpackagingoptions.md)**

Gibt zusätzliche Optionen zur PRI-Datei an.

</dd> <dt>

*OutputDirectory* 
</dt> <dd>

Typ: **pcwstr**

Ein Pfad zu einem Ordner, in dem die PRI-Datei gespeichert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

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

 

