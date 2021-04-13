---
title: 'Idodownloadinternal:: getpropertyex-Methode'
description: Ruft einen Zeiger auf einen **Variant** -Wert ab, der einen bestimmten erweiterten Download-Eigenschafts Wert enthält.
keywords:
- 'Idodownloadinternal:: getpropertyex-Methode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390577"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>Idodownloadinternal:: getpropertyex-Methode

> [!IMPORTANT]
> Die **idodownloadinternal** -Schnittstelle ist veraltet. Verwenden Sie stattdessen die [idodownload](../do/nn-do-idodownload.md) -Schnittstelle.

Ruft einen Zeiger auf einen **Variant** -Wert ab, der einen bestimmten erweiterten Download-Eigenschafts Wert enthält.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parameter

`propId`

Die erforderliche eigen schafts-ID (vom Typ " **dodownloadpropertyex**").

`propVal`

Der resultierende Eigenschafts Wert, der in einem **Variant**-Objekt gespeichert ist.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*PROPID* ist unbekannt.|
|DO_E_WRITE_ONLY_PROPERTY|Die-Eigenschaft ist schreibgeschützt und kann nicht gelesen werden.|
|E_NOT_SET|Es wurde keine solche Eigenschaft über **setpropertyex** festgelegt.|

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Dodownloadinternal. h |