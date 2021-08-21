---
title: DODownloadState-Enumeration
description: Gibt die ID des aktuellen Downloadzustands an, der Teil der **DO_DOWNLOAD_STATUS** ist.
keywords:
- DODownloadState-Enumeration, DODownloadState
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
ms.openlocfilehash: 5df8f7b20c8cff3b905acec9852b26c9a5ee360645fddb1bec22990a8bb9daba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047138"
---
# <a name="dodownloadstate-enumeration"></a>DODownloadState-Enumeration

Die **DODownloadState-Enumeration** gibt die ID des aktuellen Downloadzustands an, der Teil der **DO_DOWNLOAD_STATUS** ist.

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
| DODownloadState_Created | Das Downloadobjekt wird erstellt, wurde aber noch nicht gestartet. |
| DODownloadState_Transferring | Der Download wird in Bearbeitung. |
| DODownloadState_Transferred | Der Download wird übertragen und kann erneut gestartet werden, indem ein anderer Teil der Datei heruntergeladen wird. |
| DODownloadState_Finalized | Der Download ist abgeschlossen und kann nicht erneut gestartet werden. |
| DODownloadState_Aborted | Der Download wurde abgebrochen. |
| DODownloadState_Paused | Der Download wurde bei Bedarf oder aufgrund eines vorübergehenden Fehlers angehalten. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |
