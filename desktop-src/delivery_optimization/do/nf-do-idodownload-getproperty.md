---
title: 'Idodownload:: GetProperty-Methode'
description: Ruft einen Zeiger auf eine **Variante** ab, die eine bestimmte Download Eigenschaft enthält.
keywords:
- 'Idodownload:: GetProperty-Methode'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857847"
---
# <a name="idodownloadgetproperty-method"></a>Idodownload:: GetProperty-Methode

Ruft einen Zeiger auf eine **Variante** ab, die eine bestimmte Download Eigenschaft enthält.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parameter

`propId`

Die erforderliche Eigenschaften-ID, die (vom Typ " **dodownloadproperty**") erhalten werden soll.

`propVal`

Der resultierende Eigenschafts Wert, der in einem **Variant**-Objekt gespeichert ist.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*PROPID* ist unbekannt.|
|DO_E_WRITE_ONLY_PROPERTY|Die-Eigenschaft ist schreibgeschützt und kann nicht gelesen werden.|
|E_NOT_SET|Es wurde keine solche Eigenschaft über " **SetProperty**" festgelegt.|

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
