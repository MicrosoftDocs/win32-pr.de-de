---
title: IDODownload::Finalize-Methode
description: Finalisiert den Download.
keywords:
- IDODownload::Finalize-Methode
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 620b8cf1671c18f2e4a79a798fac366d61c9e09f5a83ecda2c1ade531c6a558a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636033"
---
# <a name="idodownloadfinalize-method"></a>IDODownload::Finalize-Methode

Finalisiert den Download. Nach Abschluss des Abschlusses kann ein Download nicht fortgesetzt werden, indem **Start aufgerufen** wird.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |
