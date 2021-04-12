---
title: Mrmkreateconfiginmemory-Funktion (mrmresourceingedexer. h)
description: Erstellt neue, initialisierte PRI-Konfigurationsinformationen (als in-Memory-Daten, nicht als Datei), die die von Ihnen angegebenen qualifiziererstandardwerte definieren.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Funktionen von mrmcreateconfginmemory-Funktionen und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518695"
---
# <a name="mrmcreateconfiginmemory-function"></a>Mrmkreateconfginmemory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt neue, initialisierte PRI-Konfigurationsinformationen (als in-Memory-Daten, nicht als Datei), die die von Ihnen angegebenen qualifiziererstandardwerte definieren. Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück. Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem gleichen Zeiger, um diesen Arbeitsspeicher freizugeben. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*platformversion* \[ in\]
</dt> <dd>

Typ: **[ **mrmplatformversion**](mrmplatformversion.md)**

Die Platt Form Version (*targetosversion*), die für die generierten Konfigurationsinformationen verwendet werden soll.

</dd> <dt>

*defaultqualifizierer* \[ in, optional\]
</dt> <dd>

Typ: **pcwstr**

Eine Liste der Standard Ressourcen Qualifizierer. Beispiel: L "language-en-US \_ Scale-100 \_ Contrast-Standard"

</dd> <dt>

*outputxmldata* \[ vorgenommen\]
</dt> <dd>

Type: **Byte \* \***

Die Adresse eines Zeigers auf ein Byte. Die-Funktion ordnet Speicher zu und gibt einen Zeiger auf diesen Speicher in *outputxmldata* zurück. Nennen Sie [**mrmfreememory**](mrmfreememory.md) mit dem Zeiger auf Byte, um diesen Arbeitsspeicher freizugeben.

</dd> <dt>

*outputxmlsize* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Die Adresse eines ulong. In _outputXmlSize * gibt die-Funktion die Größe des belegten Speichers zurück, auf den von *outputxmldata* verwiesen wird.

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

 

