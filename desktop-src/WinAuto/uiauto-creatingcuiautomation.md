---
title: Erstellen des cuiautomation-Objekts
description: In diesem Abschnitt wird beschrieben, wie Sie mit dem Schreiben einer Microsoft UI Automation-Client Anwendung beginnen, indem Sie ein Objekt instanziieren, das iuiautomation implementiert.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- Clients, Erstellen eines cuiautomation-Objekts
- Clients, cuiautomation-Objekt
- Benutzeroberflächenautomatisierungs-, cuiautomation-Objekt
- UI-Automatisierung, Erstellen eines cuiautomation-Objekts
- cuiautomation-Objekt wird erstellt
- Cuiautomation-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948799"
---
# <a name="creating-the-cuiautomation-object"></a>Erstellen des cuiautomation-Objekts

In diesem Abschnitt wird beschrieben, wie Sie mit dem Schreiben einer Microsoft UI Automation-Client Anwendung beginnen, indem Sie ein Objekt instanziieren, das [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)implementiert.

Dieses Thema enthält folgende Abschnitte:

-   [Das cuiautomation-Objekt](#the-cuiautomation-object)
-   [Erstellen des Objekts](#creating-the-object)
-   [Zugehörige Themen](#related-topics)

## <a name="the-cuiautomation-object"></a>Das cuiautomation-Objekt

Der erste Schritt bei der Verwendung der Benutzeroberflächen Automatisierung besteht darin, ein Objekt der Klasse " [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) " zu erstellen. Dieses Objekt macht die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle verfügbar, die das Gateway für alle anderen Objekte und Schnittstellen ist, die von Client Anwendungen verwendet werden. Unter anderem wird **iuiautomation** für die folgenden Aufgaben verwendet:

-   Ereignisse werden abonniert.
-   Erstellen von Bedingungen. Bedingungen sind Objekte, die verwendet werden, um den Suchbereich für Benutzeroberflächenautomatisierungs-Elemente einzuschränken.
-   Abrufen von Benutzeroberflächenautomatisierungs-Elementen direkt vom Desktop (dem Stamm Element) oder von Bildschirm Koordinaten oder Fenster Handles.
-   Erstellen von Tree Walker-Objekten, die zum Navigieren in der Hierarchie der Benutzeroberflächenautomatisierungs-Elemente verwendet werden können
-   Datentypen werden umgerechnet.

## <a name="creating-the-object"></a>Erstellen des Objekts

Führen Sie die folgenden Schritte aus, um die Verwendung der Benutzeroberflächen Automatisierung in Ihrer Anwendung zu starten:

-   Fügen Sie "uiautomation. h" in Ihre Projekt Header ein. Uiautomation. h führt die anderen Header ein, die die API definieren.
-   Deklarieren Sie einen Zeiger auf [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).
-   Initialisieren Sie die Component Object Model (com).
-   Erstellen Sie eine Instanz von [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , und rufen Sie die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle in Ihrem Zeiger ab.

Die folgende Beispiel Funktion initialisiert com und erstellt dann das [**cuiautomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) -Objekt, das die [**iuiautomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) -Schnittstelle im *ppautomation* -Zeiger abruft.


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> </dl>

 

 