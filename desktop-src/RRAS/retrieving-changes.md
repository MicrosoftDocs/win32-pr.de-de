---
title: Abrufen von Änderungen
description: Sobald sich ein Client für die Benachrichtigung über bestimmte Änderungen registriert hat und mindestens eine dieser Änderungen auftritt, erhält der Client eine Benachrichtigung vom Routingtabellen-Manager.
ms.assetid: 5ddebf2d-e3cb-451c-b082-708d2c7d0f79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea0de478a1f46e2281b18644026c2d8db44d113679f4f4f9bd5b18a1123e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788170"
---
# <a name="retrieving-changes"></a>Abrufen von Änderungen

Sobald sich ein Client für die Benachrichtigung über bestimmte Änderungen registriert hat und mindestens eine dieser Änderungen auftritt, erhält der Client eine Benachrichtigung vom Routingtabellen-Manager. Der Routingtabellen-Manager verwendet den [**RTM \_ EVENT \_ CALLBACK-Rückruf,**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) der in einem vorherigen Aufruf von [**RtmRegisterEntity bereitgestellt wurde.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) Der Routingtabellen-Manager gibt an, dass ein RTM \_ CHANGE \_ NOTIFICATION-Ereignis aufgetreten ist.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Verwenden des Ereignisbenachrichtigungsrückrufs.](use-the-event-notification-callback.md)

 

 




