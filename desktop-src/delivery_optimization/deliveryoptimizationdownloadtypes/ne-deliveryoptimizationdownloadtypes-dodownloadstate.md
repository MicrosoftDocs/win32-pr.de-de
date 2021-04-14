---
title: Dodownloadstate-Enumeration
description: Gibt die ID des aktuellen Download Status an, der Teil der **DO_DOWNLOAD_STATUS** Struktur ist.
keywords:
- Dodownloadstate-Enumeration, dodownloadstate
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518545"
---
# <a name="dodownloadstate-enumeration"></a>Dodownloadstate-Enumeration

Die **dodownloadstate** -Enumeration gibt die ID des aktuellen Download Status an, der Teil der **DO_DOWNLOAD_STATUS** Struktur ist.

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a>Konstanten

| Anforderung | Wert |
|-|-|
| DODownloadState_Created | Das Download Objekt wurde erstellt, aber noch nicht gestartet. |
| DODownloadState_Transferring | Der Download wird ausgeführt. |
| DODownloadState_Transferred | Der Download wird übertragen und kann erneut gestartet werden, indem ein anderer Teil der Datei heruntergeladen wird. |
| DODownloadState_Finalized | Der Download wurde abgeschlossen und kann nicht erneut gestartet werden. |
| DODownloadState_Aborted | Der Download wurde abgebrochen. |
| DODownloadState_Paused | Der Download wurde bei Bedarf oder aufgrund eines vorübergehenden Fehlers angehalten. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Deliveryoptimizationdownloadtypes. h |
