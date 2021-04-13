---
title: Idodownloadstatus Callback-Schnittstelle
description: Wird zum Empfangen von Benachrichtigungen zu einem Download verwendet.
keywords:
- Idodownloadstatus Callback-Schnittstelle
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
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390370"
---
# <a name="idodownloadstatuscallback-interface"></a>Idodownloadstatus Callback-Schnittstelle

Die **idodownloadstatus Callback** -Schnittstelle wird verwendet, um Benachrichtigungen zu einem Download zu empfangen.

## <a name="methods"></a>Methoden

Die **idodownloadstatus Callback** -Schnittstelle verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
| ---- |:---- |
| [Idodownloadstatucallback:: onstatuschge](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | Ruft die Implementierung dieser Methode immer dann auf, wenn sich ein Download Status geändert hat. |

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Nur Windows 10, Version 1809, \[ Win32-Anwendungen\] |
| **Unterstützte Mindestversion (Server)** | Nur Windows Server, Version 1809, \[ Win32-Anwendungen\] |
| **Header** | Do. h |