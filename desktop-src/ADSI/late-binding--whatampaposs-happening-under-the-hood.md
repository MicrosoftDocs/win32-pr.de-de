---
title: Späte Bindung, was im Hintergrund passiert
description: In diesem Thema wird beschrieben, wie die späte Bindung in ADSI funktioniert.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, späte Bindung, was geschieht im Hintergrund
- Binden von AD, späte Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474228"
---
# <a name="late-binding-whats-happening-under-the-hood"></a>Späte Bindung: Was geschieht im Hintergrund?

In der folgenden Liste wird der allgemeine Prozess zum Durchführen einer späten Bindung beschrieben:

-   Etwas wird an ein ADSI-Verzeichnis Objekt gebunden. Beispielsweise wird "LDAP://CN = JeffSmith, OU = Sales, DC = fabrikam, DC = com" mithilfe der com-späten Bindung gebunden. Dies bewirkt, dass ADSI die [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Methode für die **IDispatch** -Schnittstelle aufruft.
-   ADSI findet ein Objekt in der Benutzerklasse und erstellt ein Objekt, das die entsprechenden Schnittstellen unterstützt, z. b. [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).
-   ADSI führt eine Suche in der Registrierung durch und findet Erweiterungs-CLSIDs für den Benutzer. Beachten Sie, dass ADSI diese Daten zwischenspeichert.
-   Ein Vorgang ruft die **mynewmethod** -Methode auf. ADSI sucht nach der Dispatch-ID und den dispatchids für andere ADSI-Erweiterungen. ADSI findet dann die Erweiterung, die diesen Aufruf verarbeitet, und ruft die [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) -Schnittstelle für diese Erweiterung auf.
-   Die-Erweiterung führt die-Funktion aus.
-   Nun ruft der Client-Writer die **yournewmethod** -Methode mithilfe der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle für die aktuelle Erweiterung auf. Die **IDispatch** -Implementierung der Erweiterung delegiert zurück an den **IDispatch** für ADSI.
-   Der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) für ADSI sucht erneut nach der entsprechenden Erweiterung oder selbst und ruft dann die entsprechende Erweiterung mithilfe der [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) -Schnittstelle für diese Erweiterung auf.

 

 