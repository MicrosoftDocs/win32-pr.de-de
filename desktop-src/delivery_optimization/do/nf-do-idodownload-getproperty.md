---
title: IDODownload::GetProperty-Methode
description: Ruft einen Zeiger auf eine **VARIANT-Datei** ab, die eine bestimmte Downloadeigenschaft enthält.
keywords:
- IDODownload::GetProperty-Methode
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
ms.openlocfilehash: f498900e8dd2e87460a5fe4e75ea1269272788488159379d64f5332f2006f97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736247"
---
# <a name="idodownloadgetproperty-method"></a>IDODownload::GetProperty-Methode

Ruft einen Zeiger auf eine **VARIANT-Datei** ab, die eine bestimmte Downloadeigenschaft enthält.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parameter

`propId`

Die erforderliche Abzurufende Eigenschaften-ID (vom Typ **DODownloadProperty**).

`propVal`

Der resultierende Eigenschaftswert, der in einer **VARIANT** gespeichert ist.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10)zurückgegeben.

|Rückgabewert|Beschreibung|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* ist unbekannt.|
|DO_E_WRITE_ONLY_PROPERTY|Die Eigenschaft ist schreibgeschützt und kann nicht gelesen werden.|
|E_NOT_SET|Diese Eigenschaft wurde nicht über **SetProperty** festgelegt.|

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |
