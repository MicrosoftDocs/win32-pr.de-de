---
title: 'Idodownload:: GetStatus-Methode'
description: Ruft einen Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur ab, die den aktuellen Status des Downloads widerspiegelt.
keywords:
- 'Idodownload:: GetStatus-Methode'
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
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389652"
---
# <a name="idodownloadgetstatus-method"></a>Idodownload:: GetStatus-Methode

Ruft einen Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur ab, die den aktuellen Status des Downloads widerspiegelt.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>Parameter

`status`

Ein Zeiger auf eine **DO_DOWNLOAD_STATUS** -Struktur.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
