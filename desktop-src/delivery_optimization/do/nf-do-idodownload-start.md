---
title: 'Idodownload:: Start-Methode'
description: Startet einen Download oder nimmt diesen wieder auf.
keywords:
- 'Idodownload:: Start-Methode'
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
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106365025"
---
# <a name="idodownloadstart-method"></a>Idodownload:: Start-Methode

Startet oder setzt einen Download fort und übergibt optionale Bereiche als Zeiger auf [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) Struktur.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Parameter

`ranges`

Optional. Ein Zeiger auf eine [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) Struktur (um nur bestimmte Bereiche der Datei herunterzuladen). Übergeben `nullptr` Sie, um die gesamte Datei herunterzuladen.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |
