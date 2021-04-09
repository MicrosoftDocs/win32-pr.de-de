---
title: 'Idodownloadinternal:: setpropertyex-Methode'
description: Legt eine erweiterte Download Eigenschaft fest. Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die einen bestimmten Eigenschafts Wert enthält, der auf den Download angewendet werden soll.
keywords:
- 'Idodownloadinternal:: setpropertyex-Methode'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948790"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>Idodownloadinternal:: setpropertyex-Methode

> [!IMPORTANT]
> Die **idodownloadinternal** -Schnittstelle ist veraltet. Verwenden Sie stattdessen die [idodownload](../do/nn-do-idodownload.md) -Schnittstelle.

Legt eine erweiterte Download Eigenschaft fest. Die-Methode akzeptiert einen Zeiger auf eine **Variante** , die einen bestimmten Eigenschafts Wert enthält, der auf den Download angewendet werden soll.

## <a name="syntax"></a>Syntax

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parameter

`propId`

Die erforderliche eigen schafts-ID, die festgelegt werden soll (vom Typ **dodownloadpropertyex**).

`propVal`

Der festzulegende Eigenschafts Wert, der in einem **Variant** gespeichert wird.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*PROPID* ist unbekannt.|
|DO_E_INVALID_STATE|Der Download befindet sich derzeit nicht in einem Zustand, der das Festlegen von Eigenschaften zulässt.|

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Dodownloadinternal. h |