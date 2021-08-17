---
title: IDODownload::Start-Methode
description: Startet oder setzt einen Download fort.
keywords:
- IDODownload::Start-Methode
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b2a06de8319ac07983fd13cb8523fa1dcf92365ca9275da80b699b290a4a6435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736257"
---
# <a name="idodownloadstart-method"></a>IDODownload::Start-Methode

Startet oder setzt einen Download fort und übergibt optionale Bereiche als Zeiger auf [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) Struktur.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Parameter

`ranges`

Optional. Ein Zeiger auf eine [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) -Struktur (um nur bestimmte Bereiche der Datei herunterzuladen). Übergeben `nullptr` Sie , um die gesamte Datei herunterzuladen.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](/windows/desktop/com/structure-of-com-error-codes) [](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, nur Win32-Anwendungen der Version 1809 \[\] |
| **Header** | Do.h |
