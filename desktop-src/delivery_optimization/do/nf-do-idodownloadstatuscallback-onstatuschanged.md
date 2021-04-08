---
title: 'Idodownloadstatus Callback:: OnStatusChange-Methode'
description: Ruft die Implementierung dieser Methode immer dann auf, wenn sich ein Download Status geändert hat.
keywords:
- 'Idodownloadstatus Callback:: OnStatusChange-Methode'
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
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104038394"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>Idodownloadstatus Callback:: OnStatusChange-Methode

Ruft die Implementierung dieser Methode immer dann auf, wenn sich ein Download Status geändert hat.

## <a name="syntax"></a>Syntax

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parameter

`download`

Ein Zeiger auf die **idodownload** -Schnittstelle, deren Status geändert wurde.

`status`

Ein Zeiger auf eine **DO_DOWNLOAD_STATUS** Struktur, die den Download Status enthält.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
