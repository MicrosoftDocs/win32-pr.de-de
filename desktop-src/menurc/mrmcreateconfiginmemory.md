---
title: MrmCreateConfigInMemory-Funktion (MrmResourceIndexer.h)
description: Erstellt neue, initialisierte PRI-Konfigurationsinformationen (als In-Memory-Daten, nicht als Datei), die die von Ihnen angegebenen Qualifizierer-Standardwerte definieren.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- MrmCreateConfigInMemory-Funktionsmenüs und andere Ressourcen
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
ms.openlocfilehash: b30b4a64313952d48662a82e2f62cdef25106136e7757220668fc094c9258d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011790"
---
# <a name="mrmcreateconfiginmemory-function"></a>MrmCreateConfigInMemory-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt neue, initialisierte PRI-Konfigurationsinformationen (als In-Memory-Daten, nicht als Datei), die die von Ihnen angegebenen Qualifizierer-Standardwerte definieren. Die Funktion weist Arbeitsspeicher zu und gibt einen Zeiger auf diesen Arbeitsspeicher in *outputXmlData zurück.* Rufen [**Sie MrmFreeMemory**](mrmfreememory.md) mit demselben Zeiger auf, um diesen Arbeitsspeicher frei zu geben. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

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

*platformVersion* \[ In\]
</dt> <dd>

Typ: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Die Plattformversion (*targetOsVersion*), die für die generierten Konfigurationsinformationen verwendet werden soll.

</dd> <dt>

*defaultQualifiers* \[ in, optional\]
</dt> <dd>

Typ: **PCWSTR**

Eine Liste der Standardressourcenqualifizierer. Beispiel: L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*outputXmlData* \[ out\]
</dt> <dd>

Typ: **BYTE \* \***

Die Adresse eines Zeigers auf BYTE. Die Funktion weist Arbeitsspeicher zu und gibt einen Zeiger auf diesen Arbeitsspeicher in *outputXmlData zurück.* Rufen [**Sie MrmFreeMemory mit**](mrmfreememory.md) Ihrem Zeiger auf BYTE auf, um diesen Arbeitsspeicher frei zu geben.

</dd> <dt>

*outputXmlSize* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Die Adresse eines ULONG. In *outputXmlSize gibt* die Funktion die Größe des zugeordneten Arbeitsspeichers zurück, auf den *outputXmlData zeigt.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

S \_ OK, wenn die Funktion erfolgreich war, andernfalls ein anderer Wert. Verwenden Sie die Makros SUCCEEDED() oder FAILED() (definiert in winerror.h), um den Erfolg oder Fehler zu bestimmen.

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

 

