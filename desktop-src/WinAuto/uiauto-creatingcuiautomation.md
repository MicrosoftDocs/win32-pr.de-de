---
title: Erstellen des CUIAutomation-Objekts
description: In diesem Abschnitt wird beschrieben, wie Sie mit dem Schreiben einer Microsoft Benutzeroberflächenautomatisierung-Clientanwendung beginnen, indem Sie ein Objekt instanziieren, das IUIAutomation implementiert.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- Clients,Erstellen eines CUIAutomation-Objekts
- clients,CUIAutomation-Objekt
- Benutzeroberflächenautomatisierung,CUIAutomation-Objekt
- Benutzeroberflächenautomatisierung,Erstellen eines CUIAutomation-Objekts
- Erstellen eines CUIAutomation-Objekts
- CUIAutomation-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b9720ce31f883c4561ae3f82372d902a0dcc3fbfca4bae6de998ce438a6d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795490"
---
# <a name="creating-the-cuiautomation-object"></a>Erstellen des CUIAutomation-Objekts

In diesem Abschnitt wird beschrieben, wie Sie mit dem Schreiben einer Microsoft Benutzeroberflächenautomatisierung-Clientanwendung beginnen, indem Sie ein Objekt instanziieren, das [**IUIAutomation implementiert.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)

Dieses Thema enthält folgende Abschnitte:

-   [Das CUIAutomation-Objekt](#the-cuiautomation-object)
-   [Erstellen des Objekts](#creating-the-object)
-   [Zugehörige Themen](#related-topics)

## <a name="the-cuiautomation-object"></a>Das CUIAutomation-Objekt

Der erste Schritt bei der Verwendung Benutzeroberflächenautomatisierung ist das Erstellen eines Objekts der [**CUIAutomation-Klasse.**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) Dieses Objekt macht die [**IUIAutomation-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) verfügbar, die das Gateway für alle anderen Objekte und Schnittstellen ist, die von Clientanwendungen verwendet werden. **IUIAutomation** wird unter anderem für die folgenden Aufgaben verwendet:

-   Abonnieren von Ereignissen.
-   Erstellen von Bedingungen. Bedingungen sind Objekte, die verwendet werden, um den Bereich der Suchvorgänge für Benutzeroberflächenautomatisierung zu engen.
-   Abrufen von Benutzeroberflächenautomatisierung direkt vom Desktop (dem Stammelement) oder von Bildschirmkoordinaten oder Fensterhandles.
-   Erstellen von Tree-Tree-Tree-Objekten, die verwendet werden können, um durch die Hierarchie der Benutzeroberflächenautomatisierung zu navigieren.
-   Konvertieren von Datentypen.

## <a name="creating-the-object"></a>Erstellen des Objekts

Führen Sie zum Einstieg Benutzeroberflächenautomatisierung in Ihrer Anwendung die folgenden Schritte aus:

-   Schließen Sie UIAutomation.h in Ihre Projektheader ein. UIAutomation.h enthält die anderen Header, die die API definieren.
-   Deklarieren Sie einen Zeiger auf [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).
-   Initialisieren Sie Component Object Model (COM).
-   Erstellen Sie eine Instanz von [**CUIAutomation,**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) und rufen Sie die [**IUIAutomation-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) in Ihrem Zeiger ab.

Die folgende Beispielfunktion initialisiert COM und erstellt dann das [**CUIAutomation-Objekt,**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) indem die [**IUIAutomation-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) im *ppAutomation-Zeiger abgerufen* wird.


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

**Konzeptionellen**
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Abrufen von Benutzeroberflächenautomatisierungs-Elementen](uiauto-obtainingelements.md)
</dt> </dl>

 

 