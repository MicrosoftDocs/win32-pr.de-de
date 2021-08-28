---
title: IDODownloadStatusCallback-Schnittstelle
description: Wird verwendet, um Benachrichtigungen zu einem Download zu erhalten.
keywords:
- IDODownloadStatusCallback-Schnittstelle
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: d91ff44e3b4f4247983ec81d53257347c8bcfa523f85855dcd0d37074f4b38fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498950"
---
# <a name="idodownloadstatuscallback-interface"></a>IDODownloadStatusCallback-Schnittstelle

Die **IDODownloadStatusCallback-Schnittstelle** wird verwendet, um Benachrichtigungen über einen Download zu empfangen.

## <a name="methods"></a>Methoden

Die **IDODownloadStatusCallback-Schnittstelle** verfügt über diese Methoden.

| Methode | Beschreibung |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | DO ruft Ihre Implementierung dieser Methode jedes Mal auf, wenn sich ein Downloadstatus geändert hat. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | \[Windows 10, Version 1809 Nur Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Windows Server, version 1809 Win32 applications only (Nur \[ Win32-Anwendungen der Version 1809)\] |
| **Header** | Do.h |