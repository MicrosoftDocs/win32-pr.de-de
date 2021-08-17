---
title: IDODownloadStatusCallback::OnStatusChange-Methode
description: DO ruft Ihre Implementierung dieser Methode jedes Mal auf, wenn sich ein Downloadstatus geändert hat.
keywords:
- IDODownloadStatusCallback::OnStatusChange-Methode
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0395b6bc64ad3abe102a0a4f0dc7afd8e8d59f336949a3b97eaf683a4f4900cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736217"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>IDODownloadStatusCallback::OnStatusChange-Methode

DO ruft Ihre Implementierung dieser Methode jedes Mal auf, wenn sich ein Downloadstatus geändert hat.

## <a name="syntax"></a>Syntax

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parameter

`download`

Ein Zeiger auf die **IDODownload-Schnittstelle,** deren Status sich geändert hat.

`status`

Ein Zeiger auf eine **DO_DOWNLOAD_STATUS** Struktur, die den Downloadstatus enthält.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |
