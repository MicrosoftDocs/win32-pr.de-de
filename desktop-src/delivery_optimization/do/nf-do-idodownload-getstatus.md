---
title: IDODownload::GetStatus-Methode
description: Ruft einen Zeiger auf eine DO_DOWNLOAD_STATUS **struktur** ab, die den aktuellen Status des Downloads widerspiegelt.
keywords:
- IDODownload::GetStatus-Methode
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e3a5aec5e35187a51865e074dae26ff012b75dfa3a41ffd13a8bed7371515fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047108"
---
# <a name="idodownloadgetstatus-method"></a>IDODownload::GetStatus-Methode

Ruft einen Zeiger auf eine DO_DOWNLOAD_STATUS **struktur** ab, die den aktuellen Status des Downloads widerspiegelt.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parameter

`status`

Ein Zeiger auf eine **DO_DOWNLOAD_STATUS** Struktur.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [zurückgegeben.](/windows/desktop/com/com-error-codes-10)

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | Do.h |
