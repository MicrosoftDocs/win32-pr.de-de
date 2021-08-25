---
title: IDODownloadInternal::SetPropertyEx-Methode
description: Legt eine erweiterte Downloadeigenschaft fest. Die -Methode akzeptiert  einen Zeiger auf eine VARIANT-Datei, die einen bestimmten Eigenschaftswert enthält, der auf den Download angewendet werden soll.
keywords:
- IDODownloadInternal::SetPropertyEx-Methode
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
ms.openlocfilehash: d6156f4309c0eac9d2d250c85f7e9ab365e4a3b1e4072aabec7f6aa7e17c437f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858800"
---
# <a name="idodownloadinternalsetpropertyex-method"></a>IDODownloadInternal::SetPropertyEx-Methode

> [!IMPORTANT]
> Die **IDODownloadInternal-Schnittstelle** ist veraltet. Verwenden Sie stattdessen die [IDODownload-Schnittstelle.](../do/nn-do-idodownload.md)

Legt eine erweiterte Downloadeigenschaft fest. Die -Methode akzeptiert  einen Zeiger auf eine VARIANT-Datei, die einen bestimmten Eigenschaftswert enthält, der auf den Download angewendet werden soll.

## <a name="syntax"></a>Syntax

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>Parameter

`propId`

Die erforderliche Festzulegende Eigenschaften-ID (vom Typ **DODownloadPropertyEx**).

`propVal`

Der festzulegende Eigenschaftswert, der in einer **VARIANT** gespeichert wird.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* ist unbekannt.|
|DO_E_INVALID_STATE|Der Download befindet sich derzeit nicht in einem Zustand, der das Festlegen von Eigenschaften zulässt.|

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | DODownloadInternal.h |