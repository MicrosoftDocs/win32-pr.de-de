---
description: In diesem Abschnitt wird die Verwendung von Umgebungslichtsensordaten behandelt, und es wird beschrieben, wie Benutzeroberflächenfeatures und Programminhalte für viele Beleuchtungsbedingungen optimiert werden können.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Erstellen Light-Aware Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd97bb304c3a8718ae4b32d8b9100a1e7eb7a18240b9089c112272f588ee209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890287"
---
# <a name="creating-light-aware-user-interfaces"></a>Erstellen Light-Aware Benutzeroberflächen

In diesem Abschnitt wird die Verwendung von Umgebungslichtsensordaten behandelt, und es wird beschrieben, wie Benutzeroberflächenfeatures und Programminhalte für viele Beleuchtungsbedingungen optimiert werden können.

Umgebungslichtsensoren machen Daten verfügbar, die verwendet werden können, um verschiedene Aspekte der Beleuchtungsbedingungen zu bestimmen, in denen sich der Sensor befindet. Umgebungslichtsensoren können die allgemeine Helligkeit einer Umgebung (Leuchtdichte) und andere Aspekte des umgebenden Lichts verfügbar machen, wie z. B. Die Durchlässigkeit oder Farbtemperatur.

Computer können auf verschiedene Weise nützlicher sein, wenn das System auf Beleuchtungsbedingungen reagiert. Dazu gehören die Steuerung der Helligkeit der Computeranzeige (ein neues, vollständig unterstütztes Feature in Windows 7), das automatische Anpassen des Beleuchtungsgrads von Tastaturen und sogar die Helligkeitssteuerung für andere Beleuchtungen (z. B. Schaltflächenlichter, Aktivitätslichter usw.).

Endbenutzerprogramme können auch von Lichtsensoren profitieren. Programme können ein Design anwenden, das für einen bestimmten Beleuchtungszustand geeignet ist, z. B. ein bestimmtes Außen- und Gebäudedesign. Der vielleicht wichtigste Aspekt der Integration von Lichtsensorn in Programme sind Lesbarkeits- und Lesbarkeitsoptimierungen, die auf Beleuchtungsbedingungen basieren.

Mit der Sensor-API können Sie solche Programme erstellen. Stellen Sie sich folgendes Szenario vor:

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Szenario: Verwenden Ihres Laptops zum Navigieren zu einem Restaurant

Angenommen, Sie möchten Ihren Computer verwenden, um zu einem neuen Restaurant zu navigieren. Sie beginnen in Ihrem Haus, suchen die Adresse des Restaurants und planen Ihre Route. Der folgende Screenshot zeigt, wie Ihr Navigationsprogramm die Benutzeroberfläche optimieren kann, um detaillierte Informationen zu Beleuchtungsbedingungen in Gebäudefenstern anzuzeigen.

![Benutzeroberfläche für Gebäudebeleuchtung.](images/nav-normal.png)

Wenn Sie nach außen zu Ihrem Auto fahren, stoßen Sie auf direktes Licht, wodurch der Bildschirm des Laptops schwer zu lesen ist. Der folgende Screenshot zeigt, wie Ihr Programm seine Benutzeroberfläche ändern kann, um Lesbarkeit/Lesbarkeit im direkten Licht zu maximieren. In dieser Ansicht wurde ein Großteil der Details weggelassen, und der Kontrast wird maximiert.

![Benutzeroberfläche für direkte Beleuchtungsbedingungen.](images/nav-contrast.png)

Wenn Sie sich dem Restaurant nähern, nähert sich der Abend, und es wird außen dunkel. Im folgenden Screenshot wurde die Benutzeroberfläche für das Navigationsprogramm für die Anzeige mit geringem Licht optimiert. Durch die Verwendung von dunkleren Farben insgesamt ist diese Benutzeroberfläche im dunklen Auto leicht zu betrachten.

![Benutzeroberfläche, die für die Anzeige mit geringem Licht konzipiert ist.](images/nav-lowlight.png)

Im weiteren Verlauf dieses Abschnitts erfahren Sie, wie Sie Ihre Programme für verschiedene Beleuchtungsbedingungen optimieren können und wie Sie die Sensor-API verwenden können, um die lichtfähige Benutzeroberfläche zu aktivieren.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Grundlagen Light-Aware Benutzeroberflächen](fundamentals-of-light-aware-user-interfaces.md)
-   [Beispiele für Light-Aware Benutzeroberflächen](examples-of-light-aware-user-interfaces.md)
-   [Optimieren der Benutzerfreundlichkeit](optimizing-the-user-experience.md)
-   [Grundlegendes zu und Interpretieren von Lux-Werten](understanding-and-interpreting-lux-values.md)
-   [Verwenden von Lichtsensordaten](handling-data-from-multiple-light-sensors.md)

 

 



