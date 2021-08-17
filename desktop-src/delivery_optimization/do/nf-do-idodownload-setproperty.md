---
title: IDODownload::SetProperty-Methode
description: Legt eine Downloadeigenschaft fest.
keywords:
- IDODownload::SetProperty-Methode
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7d966edb083107b80f0723bce195bfc588797efb8ad1931e0e75a468bec5a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543899"
---
# <a name="idodownloadsetproperty-method"></a>IDODownload::SetProperty-Methode

Legt eine Downloadeigenschaft fest. Die -Methode akzeptiert einen  Zeiger auf eine VARIANT-Datei, die eine bestimmte Eigenschaft enthält, die auf den Download angewendet werden soll.

## <a name="syntax"></a>Syntax

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parameter

`propId`

Die erforderliche Eigenschafts-ID, die festgelegt werden soll (vom **Typ DODownloadProperty**).

`propVal`

Der eigenschaftswert, der festgelegt werden soll und in einem **VARIANT-Objekt gespeichert ist.**

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [zurückgegeben.](/windows/desktop/com/com-error-codes-10)

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* ist unbekannt.|
|DO_E_INVALID_STATE|Der Download befindet sich derzeit nicht in einem Zustand, der das Festlegen von Eigenschaften zulässt.|

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | Do.h |
