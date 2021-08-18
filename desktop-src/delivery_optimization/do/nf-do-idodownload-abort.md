---
title: IDODownload::Abort-Methode
description: Bricht den Download ab.
keywords:
- IDODownload::Abort-Methode
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 70ca7d25b702de8cd11214daf5d70491113d2f68959a9d48c5b4d0c97bc97dda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543977"
---
# <a name="idodownloadabort-method"></a>IDODownload::Abort-Methode

Bricht den Download ab.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Abort();
```

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |
