---
description: Die reorderfunktionalitäten-Methode legt eine neue Reihenfolge für Formatierungsfunktionen fest.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'Itformatcontrol:: reorderfunktionalitäten-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364766"
---
# <a name="itformatcontrolreordercapabilities-method"></a>Itformatcontrol:: reorderfunktionalitäten-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **reorderfunktionalitäten** -Methode legt eine neue Reihenfolge für Formatierungsfunktionen fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwindices* \[ in\]
</dt> <dd>

Index des umordneten Formats.

</dd> <dt>

*pfaktivierte* \[ in\]
</dt> <dd>

Gibt an, ob das Format aktiviert oder deaktiviert werden soll.

</dd> <dt>

*pfpublicize* \[ in\]
</dt> <dd>

Gibt an, ob das Format verfügbar gemacht werden soll.

</dd> <dt>

*dwnumindizes* \[ in\]
</dt> <dd>

Neue Indexnummer für das Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Vor der Verwendung dieser Methode muss die [**getnumoffunktionalitäten**](itformatcontrol-getnumberofcapabilities.md) -Methode aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itformatcontrol**](itformatcontrol.md)
</dt> <dt>

[**Getnumof-Funktionen**](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




