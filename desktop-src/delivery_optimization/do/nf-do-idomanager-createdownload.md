---
title: 'Idomanager:: kreatedownload-Methode'
description: Erstellt einen neuen Download.
keywords:
- 'Idomanager:: kreatedownload-Methode'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389650"
---
# <a name="idomanagercreatedownload-method"></a>Idomanager:: kreatedownload-Methode

Erstellt einen neuen Download.

## <a name="syntax"></a>Syntax

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a>Parameter

`download`

Die Adresse eines **idodownload** -Schnittstellen Zeigers.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
