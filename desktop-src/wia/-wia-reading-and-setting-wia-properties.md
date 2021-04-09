---
description: Die iwiapropertystorage-Schnittstelle stellt Methoden zum Lesen und Schreiben der Eigenschaften eines Windows-Abbild Erwerbs (WIA) dar. Zu den Element Eigenschaften zählen Geräte Befehle, Informationen zum Element Format und Geräteinformationen.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lesen und Festlegen von WIA-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129401"
---
# <a name="reading-and-setting-wia-properties"></a>Lesen und Festlegen von WIA-Eigenschaften

Die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle stellt Methoden zum Lesen und Schreiben der Eigenschaften eines Windows-Abbild Erwerbs (WIA) dar. Zu den Element Eigenschaften zählen Geräte Befehle, Informationen zum Element Format und Geräteinformationen.

Eine Anwendung kann einen Zeiger auf eine [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle eines Elements abrufen, indem Sie die Geräteinformationen oder Ereignis Informationen des Elements aufzählt, indem Sie [**iwiaitem:: enumdevicecapabilior**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) [**iwiaitem:: enumregistereventinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) aufrufen oder indem Sie die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle des Elements Abfragen. (In WIA 2,0 rufen Sie dies durch Aufrufen von [**IWiaItem2:: enumdevicecapabilior**](-wia-iwiaitem2-enumdevicecapabilities.md) [**IWiaItem2:: enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) oder durch Abfragen der [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Elements auf.)

[**Iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) erbt von [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) , und die geerbten Methoden werden implementiert, wie im Referenz Abschnitt von strukturiertem Speicher im Windows Software Development Kit (SDK) beschrieben.

> [!Note]
>
> WIA-Anwendungen sollten Bild Daten Header immer für genaue Bild Informationen lesen. Der WIA-Treiber kann die WIA-Eigenschaften und Bild Daten Header während der Datenübertragung ändern.
>
> Wenn kein Bild Daten Header im angegebenen Format angegeben ist, sollte die WIA-Anwendung die WIA-Eigenschaften als Informationsquelle für die Datenübertragung verwenden. Die WIA-Anwendung sollte die benötigten WIA-Eigenschaften nach Abschluss der Überprüfung oder Erfassung erneut registrieren, um die aktualisierten Einstellungen zu erhalten.

 

In den folgenden Abschnitten werden die verschiedenen WIA-Eigenschaften beschrieben:

-   [Überprüfung der WIA-Eigenschaft](-wia-wia-property-validation.md)
-   [Geräte Informations Eigenschaften](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Geräteeigenschaften](-wia-device-properties.md)
-   [Element Eigenschaften](-wia-item-properties.md)
-   [Zusätzliche WIA-Eigenschaften](-wia-additional-wia-properties.md)
-   [Definieren von benutzerdefinierten Eigenschaften](-wia-defining-custom-properties.md)
-   [Verwenden von benutzerdefinierten Eigenschaften](-wia-using-custom-properties.md)
-   [Profil Schema überprüfen](-wia-scan-profile-schema.md)

 

 
