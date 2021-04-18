---
title: Überprüfen von IAccessible-Rückgabe Werten
description: Client Entwickler sollten sich nicht darauf verlassen, dass die Component Object Model (com)-Makros erfolgreich sind, und die IAccessible-Rückgabewerte konnten nicht getestet werden, da andere Werte als "S OK" als \_ erfolgreich angesehen werden.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338478"
---
# <a name="checking-iaccessible-return-values"></a>Überprüfen von IAccessible-Rückgabe Werten

Client Entwickler sollten sich nicht darauf verlassen, dass die Component Object Model (com) [**-Makros**](/windows/desktop/api/winerror/nf-winerror-failed) [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) sind, und die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Rückgabewerte konnten nicht getestet werden, da andere Werte als "S OK" als \_ erfolgreich angesehen werden. Eine Methode kann z. b. den Wert "false" zurückgeben \_ , was durch das Makro " **erfolgreich** " als erfolgreich angesehen wird, aber dennoch einen **null** -Zeiger in einem Output-Parameter erhält.

Client Entwickler müssen vor der Möglichkeit warnen, dass einige Server andere Fehlercodes als die dokumentierten Werte zurückgeben. Um sicher zu sein, müssen Sie sicherstellen, dass alle Ausgabeparameter gültige Informationen enthalten und die folgenden Kriterien erfüllen:

-   Alle Zeiger sind nicht **null**.
-   Der **VT** -Member einer beliebigen [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) -Struktur ist nicht gleich VT \_ empty.

 

 