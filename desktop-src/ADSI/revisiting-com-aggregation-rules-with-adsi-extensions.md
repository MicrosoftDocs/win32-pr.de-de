---
title: Rebesuchen von com-Aggregations Regeln mit ADSI-Erweiterungen
description: Im folgenden finden Sie eine kurze Überprüfung der com-Aggregations-und ADSI-Erweiterungs Regeln.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, com-Aggregations Regeln
- COM-Aggregations-ADSI
- Rebesuchen von com-Aggregations Regeln mit ADSI Extensions ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730257"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>Rebesuchen von com-Aggregations Regeln mit ADSI-Erweiterungen

Im folgenden finden Sie eine kurze Überprüfung der com-Aggregations-und ADSI-Erweiterungs Regeln.

-   Die Methode " **kreatanstance** " gibt wie folgt einen Zeiger auf eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle zurück, die keine Funktionsaufrufe an den Aggregator delegiert.

    Die [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode gibt Zeiger auf die unterstützten Schnittstellen und Fehler für Schnittstellen zurück, die Sie nicht unterstützt.

    Die [**IUnknown:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode erhöht den Verweis Zähler für das aggregierte Erweiterungs Objekt selbst.

    Die [**iunkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode Dekremente den Verweis Zähler für das aggregierte Erweiterungs Objekt selbst und zerstört sich selbst, wenn der Verweis Zähler 0 ist.

-   Das Erweiterungs Objekt sollte den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger des Aggregators (z. b. m \_ pouterunknown) während der Implementierung der Methode " **kreateinstance** " speichern.
-   Alle Schnittstellen, die das Erweiterungs Objekt unterstützt (einschließlich [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)), sollten von [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)erben, das alle Funktionsaufrufe an den Aggregator zurück delegiert.
    -   [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ruft "m \_ pouterunknown->QueryInterface" auf
    -   [**IUnknown:: adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ruft "m \_ pouterunknown->adressf" auf
    -   [**Iunkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ruft "m \_ pouterunknown->Release" auf

Erweiterungs Schreiber können eine beliebige interne Implementierung auswählen, die Sie bevorzugen, sofern Sie den standardmäßigen com-Aggregations Regeln folgen. Beachten Sie, dass ein Erweiterungs Objekt nicht als eigenständiges Objekt funktionieren muss. Erweiterungen sind so konzipiert, dass Sie als Aggregate funktionieren. Eine Erweiterung kann jedoch so geschrieben werden, dass Sie sowohl als eigenständiges Objekt als auch als Aggregat funktioniert.

Zusätzlich zur Standard-com-Aggregations Unterstützung unterstützt ein Erweiterungs Objekt [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) für erweiterte Funktionen. Wenn die späte Bindung unterstützt wird, sollte die Erweiterung wie folgt lauten:

-   Delegieren Sie Funktionen für [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurück an den Aggregator.
-   Implementieren Sie die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle in [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

 

 