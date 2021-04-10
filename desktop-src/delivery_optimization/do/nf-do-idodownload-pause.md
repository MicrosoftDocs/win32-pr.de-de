---
title: Idodownload::P ause-Methode
description: Hält den Download an.
keywords:
- Idodownload::P ause-Methode
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101134"
---
# <a name="idodownloadpause-method"></a>Idodownload::P ause-Methode

Hält den Download an.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Pause();
```

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
