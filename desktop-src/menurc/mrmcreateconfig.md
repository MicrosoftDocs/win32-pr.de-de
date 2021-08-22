---
title: MrmCreateConfig-Funktion (MrmResourceIndexer.h)
description: Erstellt eine neue, initialisierte PRI-Konfigurationsdatei, die die von Ihnen angegebenen Qualifizierer-Standardwerte definiert. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung (Package Resource Indexing, PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- MrmCreateConfig-Funktionsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618823054914a609a451d6a0fe77ed6380e2d95982e14158f5965bf3f9c82260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601920"
---
# <a name="mrmcreateconfig-function"></a>MrmCreateConfig-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Erstellt eine neue, initialisierte PRI-Konfigurationsdatei, die die von Ihnen angegebenen Qualifizierer-Standardwerte definiert. Weitere Informationen und szenariobasierte exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter APIs für die Paketressourcenindizierung und benutzerdefinierte [Buildsysteme.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Syntax


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*platformVersion* \[ In\]
</dt> <dd>

Typ: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Die Plattformversion (*targetOsVersion*), die für die generierte Konfigurationsdatei verwendet werden soll.

</dd> <dt>

*defaultQualifiers* \[ in, optional\]
</dt> <dd>

Typ: **PCWSTR**

Eine Liste der Standardressourcenqualifizierer. Beispiel: L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*outputXmlFile* \[ In\]
</dt> <dd>

Typ: **PCWSTR**

Der Pfad der zu erstellenden Konfigurationsdatei.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

