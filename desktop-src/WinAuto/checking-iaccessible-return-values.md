---
title: Überprüfen von IAccessible-Rückgabewerten
description: Cliententwickler sollten sich nicht auf die COM-Makros SUCCEEDED (Component Object Model) und FAILED zum Testen der Rückgabewerte von IAccessible verlassen, da andere Werte als S \_ OK als erfolgreich angesehen werden.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1df43a316898ceeb751b114251ca8fbc91a8fc5360558a3929bcc3ecc47cce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759630"
---
# <a name="checking-iaccessible-return-values"></a>Überprüfen von IAccessible-Rückgabewerten

Cliententwickler sollten sich nicht auf die COMPONENT OBJECT MODEL (COM)-Makros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) und [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) zum Testen von [**IAccessible-Rückgabewerten**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) verlassen, da andere Werte als S \_ OK als erfolgreich angesehen werden. Beispielsweise kann eine Methode S \_ FALSE zurückgeben, was vom **SUCCEEDED-Makro** als erfolgreich betrachtet wird, aber dennoch einen **NULL-Zeiger** in einem Ausgabeparameter empfängt.

Cliententwickler müssen sich vor der Möglichkeit schützen, dass einige Server andere Fehlercodes als die dokumentierten Werte zurückgeben. Um sicher zu sein, müssen Sie sicherstellen, dass alle Ausgabeparameter gültige Informationen enthalten und die folgenden Kriterien erfüllen:

-   Alle Zeiger sind ungleich **NULL.**
-   Der **vt-Member** einer [VARIANT-Struktur](/windows/win32/api/oaidl/ns-oaidl-variant) ist nicht gleich VT \_ EMPTY.

 

 