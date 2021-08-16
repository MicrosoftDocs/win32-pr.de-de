---
title: WMT_STATUS Ereignisbenachrichtigung in DirectShow
description: WMT \_ STATUS-Ereignisbenachrichtigung in DirectShow
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Medienformat-SDK, WMT_STATUS Ereignisbenachrichtigungen in DirectShow
- Windows Medienformat-SDK, Ereignisbenachrichtigungen
- Windows Medienformat-SDK, DirectShow
- Advanced Systems Format (ASF),WMT_STATUS Ereignisbenachrichtigungen in DirectShow
- ASF (Advanced Systems Format), WMT_STATUS Ereignisbenachrichtigungen in DirectShow
- Advanced Systems Format (ASF), Ereignisbenachrichtigungen
- ASF (Advanced Systems Format), Ereignisbenachrichtigungen
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Ereignisbenachrichtigungen
- DirectShow,WMT_STATUS Ereignisbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4bbe430f16872baf94a0d47417381bc8bcd23d5c9fbbdb69ff2496cd873908
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089630"
---
# <a name="wmt_status-event-notification-in-directshow"></a>WMT \_ STATUS-Ereignisbenachrichtigung in DirectShow

Sowohl der ASF-Reader als auch der ASF Writer leiten [**WMT \_ STATUS-Ereignisse**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) an Anwendungen weiter. Der Writer leitet alle derartigen Ereignisse weiter, und der Reader leitet nur diejenigen weiter, die sich auf den DRM-Lizenzerwerb beziehen. Um diese Ereignisbenachrichtigungen in Ihrer Anwendung zu erhalten, fügen Sie in Ihrer Ereignisbehandlungsfunktion einen Fall für das **EC \_ WMT \_ EVENT** hinzu. Der *lParam1-Parameter,* der dem Ereignis zugeordnet ist, enthält den **WMT \_ STATUS-Code** (kann **WMT \_ ERROR** sein), und lParam2 enthält eine [**AM \_ WMT EVENT \_ \_ DATA,die**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) das **HRESULT** enthält.

 

 