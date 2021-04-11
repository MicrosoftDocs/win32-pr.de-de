---
description: In diesem Abschnitt wird die Verwendung von Umgebungslichtsensor-Daten behandelt und erläutert, wie Benutzeroberflächen Features und Programminhalte für viele Beleuchtungsbedingungen optimiert werden können.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Erstellen Light-Aware Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4b6d404e366cb898114fe61729ab1ad722feb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960253"
---
# <a name="creating-light-aware-user-interfaces"></a>Erstellen Light-Aware Benutzeroberflächen

In diesem Abschnitt wird die Verwendung von Umgebungslichtsensor-Daten behandelt und erläutert, wie Benutzeroberflächen Features und Programminhalte für viele Beleuchtungsbedingungen optimiert werden können.

Umgebungslichtsensoren machen Daten verfügbar, mit denen verschiedene Aspekte der Beleuchtungsbedingungen bestimmt werden können, in denen sich der Sensor befindet. Umgebungslichtsensoren können die Gesamthelligkeit einer Umgebung (Beleuchtung) und andere Aspekte der umgebenden Beleuchtung, wie z. b. die Chromaticity-oder Farbtemperatur, verfügbar machen.

Computer können auf verschiedene Arten nützlicher sein, wenn das System auf Beleuchtungsbedingungen reagiert. Dazu gehört das Steuern der Helligkeit der Computer Anzeige (ein neues, vollständig unterstütztes Feature in Windows 7), das automatische Anpassen der Beleuchtungs Ebene von beleuchteten Tastaturen und sogar der Helligkeitssteuerung für andere Leuchten (z. b. Schaltflächen Beleuchtung, Aktivitäts Beleuchtung usw.).

Endbenutzer Programme können auch von Lichtsensoren profitieren. Programme können ein Design anwenden, das für eine bestimmte Beleuchtungs Bedingung geeignet ist, z. b. ein bestimmtes Outdoor-Design und ein spezielles Design. Der wichtigste Aspekt der Lichtsensor Integration in Programme sind Optimierungen der Lesbarkeit und Lesbarkeit auf der Grundlage von Beleuchtungsbedingungen.

Die Sensor-API ermöglicht es Ihnen, solche Programme zu erstellen. Stellen Sie sich folgendes Szenario vor:

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Szenario: Navigieren zu einem Restaurant mithilfe Ihres Laptops

Angenommen, Sie möchten Ihren Computer verwenden, um zu einem neuen Restaurant zu navigieren. Beginnen Sie in Ihrem Haus, und suchen Sie nach der Adresse des Restaurants und der Planung der Route. Der folgende Screenshot zeigt, wie Ihre Benutzeroberfläche von Ihrem Navigationsprogramm optimiert werden kann, um ausführliche Informationen in den Bereichen der Innenbeleuchtung anzuzeigen.

![Benutzeroberfläche, die für die Innenbeleuchtung konzipiert ist](images/nav-normal.png)

Wenn Sie zu Ihrem Auto wechseln, stoßen Sie auf direktes Sonnenlicht. Dadurch wird der Bildschirm des Laptops schwer lesbar. Der folgende Screenshot zeigt, wie Ihr Programm die Benutzeroberfläche ändern kann, um die Lesbarkeit/Lesbarkeit in direktem Licht zu maximieren. In dieser Ansicht wurde ein Großteil des Details ausgelassen und der Kontrast maximiert.

![die Benutzeroberfläche für direkte Beleuchtungsbedingungen.](images/nav-contrast.png)

Wenn Sie sich näher mit dem Restaurant auskennen, kommt es vor, und es wird nicht mehr angezeigt. Im folgenden Screenshot wurde die Benutzeroberfläche für das Navigationsprogramm für die Anzeige mit geringem Licht optimiert. Durch die Verwendung von dunkleren Farben insgesamt ist die Benutzeroberfläche auf dem dunklen Fahrzeug leicht zu betrachten.

![die Benutzeroberfläche, die für die Ansicht mit geringem Licht konzipiert](images/nav-lowlight.png)

Im restlichen Teil dieses Abschnitts werden einige Dinge erläutert, die Sie tun können, um Ihre Programme für verschiedene Beleuchtungsbedingungen zu optimieren, und wie Sie die Sensor-API verwenden können, um die helle Benutzeroberfläche zu ermöglichen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Grundlagen der Light-Aware Benutzeroberflächen](fundamentals-of-light-aware-user-interfaces.md)
-   [Beispiele für Light-Aware Benutzeroberflächen](examples-of-light-aware-user-interfaces.md)
-   [Optimieren der Benutzer Leistung](optimizing-the-user-experience.md)
-   [Verstehen und Interpretieren von Lux-Werten](understanding-and-interpreting-lux-values.md)
-   [Verwenden von Licht Sensor Daten](handling-data-from-multiple-light-sensors.md)

 

 



