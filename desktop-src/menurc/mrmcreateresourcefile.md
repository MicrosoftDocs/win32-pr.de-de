---
title: MrmCreateResourceFile-Funktion (MrmResourceIndexer.h)
description: Erstellt eine PRI-Datei (mit dem Namen \ 0034;resources.pri \ 0034;) oder Dateien auf dem Datenträger im angegebenen Ordner. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menüs und andere Ressourcen der MrmCreateResourceFile-Funktion
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
ms.openlocfilehash: 8f58cd2ca366e2eeb4c594df986016d29c9aafbee0fa3310beded7a0b9bb12ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687333"
---
# <a name="mrmcreateresourcefile-function"></a>MrmCreateResourceFile-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt eine PRI-Datei (mit dem Namen "resources.pri") oder Dateien auf dem Datenträger im angegebenen Ordner. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für [die Paketressourcenindizierung (PACKAGE Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

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

*Indexer* \[ In\]
</dt> <dd>

Typ: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Ein Handle, das den Ressourcenindexer identifiziert, aus dem die PRI-Datei erstellt werden soll.

</dd> <dt>

*packagingMode* \[ In\]
</dt> <dd>

Typ: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Gibt an, ob die PRI-Datei eigenständig, automatisch nach Ressourcenqualifizierer aufgeteilt oder ein Ressourcenpaket sein soll.

</dd> <dt>

*packagingOptions* \[ In\]
</dt> <dd>

Typ: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Gibt zusätzliche Optionen zur PRI-Datei an.

</dd> <dt>

*outputDirectory* 
</dt> <dd>

Typ: **PCWSTR**

Ein Pfad zu einem Ordner, in dem die PRI-Datei gespeichert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um erfolg- oder fehlerbestimmend zu sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1803 \[\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows \[Nur Serverdesktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

