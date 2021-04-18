---
description: Die Methode "ltalias" konfiguriert einen standardmäßigen H. 323-Alias für die Adresse. Dieser Alias wird im H. 323-Setup Austausch verwendet, damit die andere Partei den Namen dieser Partei kennt.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: IH323LineEx::/talias-Methode (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358000"
---
# <a name="ih323lineexsetalias-method"></a>IH323LineEx::/talias-Methode

\[Der **Server ist für** die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Methode " **ltalias** " konfiguriert einen standardmäßigen H. 323-Alias für die Adresse. Dieser Alias wird im H. 323-Setup Austausch verwendet, damit die andere Partei den Namen dieser Partei kennt.

Wenn Sie diese Methode ein zweites Mal aufrufen, wird der vorherige Alias überschrieben.

Der für diese Schnittstelle festgelegte Alias wird nur verwendet, wenn es keine andere Möglichkeit gibt, dass der TSP einen richtigen Alias findet. Wenn die Gatekeeper-Unterstützung in der Zukunft dem TSP hinzugefügt wird, überschreibt der Alias, der für den Gatekeeper registriert ist oder von Gatekeeper zugewiesen wurde, das, was durch diese Methode festgelegt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

"-"  \[ in\]
</dt> <dd>

Der zu verwendende Alias in Unicode. **Null** -Beendigung ist nicht erforderlich.

</dd> <dt>

*dwLength* \[ in\]
</dt> <dd>

Die Länge des Alias Namens in Anzahl von Zeichen, einschließlich des **null** -Terminator.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                               | Beschreibung                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Methode war erfolgreich.<br/>                                                                                                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | Die Anzahl von Zeichen, die in *dwLength* angegeben wird, überschreitet die tatsächliche Anzahl von Zeichen *im Parameter "* -Parameter".<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




