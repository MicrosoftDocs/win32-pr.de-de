---
description: Der com+-Katalog speichert com+-Anwendungs Attribute, Klassenattribute und Attribute auf Computer Ebene. Sie gewährleistet die Konsistenz zwischen diesen Attributen und bietet allgemeine Vorgänge oberhalb dieser Attribute.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Der com+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345427"
---
# <a name="the-com-catalog"></a>Der com+-Katalog

Der com+-Katalog speichert com+-Anwendungs Attribute, Klassenattribute und Attribute auf Computer Ebene. Sie gewährleistet die Konsistenz zwischen diesen Attributen und bietet allgemeine Vorgänge oberhalb dieser Attribute.

Der com+-Katalog verwendet zwei verschiedene Speicher wie folgt:

-   Die COM+-Registrierungsdatenbank
-   Die Windows-Registrierung (**HKEY \_ Classes \_ root**)

Der Katalog stellt eine einheitliche logische Ansicht dieser beiden Speicher bereit und macht Sie über die com+-Verwaltungs Bibliothek verfügbar. Diese Bibliothek bietet über eine Skriptsprache sämtliche Funktionen des Verwaltungs Programms Komponenten Dienste.

Für vorhandene COM-Komponenten, für die keine neuen com+-Dienste erforderlich sind, erfolgt die Suche in der vorhandenen Windows-Registrierung. Der com+-Katalog verwendet auch die Windows-Registrierung für die Typbibliothek und die Schnittstellen Proxy-/stubregistrierung.

## <a name="split-registration"></a>Geteilte Registrierung

Bei neuen Komponenten, die tatsächlich bereits vorhandene COM-Komponenten verwenden, die in der Dienst Umgebung verwendet werden (z. b. MTS-Komponenten), wird der grundlegende com-Aspekt der Registrierung in der Windows-Registrierung gespeichert, und neue Dienste und Attribute (z. b. in der Warteschlange befindliche Komponenten) werden in der COM+-Registrierungsdatenbank gespeichert. Dies wird als *geteilte Registrierung* bezeichnet.

Jedes Attribut wird nur an einem Speicherort gespeichert: entweder in der Windows-Registrierung oder in der COM+-Registrierungsdatenbank. Neue COM-Komponenten werden ausschließlich in der COM+-Registrierungsdatenbank registriert, wobei eine Duplizierung in der Windows-Registrierung möglich ist, damit vorhandene Tools Sie verwenden können.

## <a name="transactional-updates-to-the-catalog"></a>Transaktionale Aktualisierungen des Katalogs

Einige Vorgänge im Katalog werden auf transaktionale Weise ausgeführt. Wenn Sie die com+-Verwaltungs Bibliothek über eine transaktionale Komponente aufrufen, werden die Aktualisierungen der COM+-Registrierungsdatenbank innerhalb der Transaktionsgrenze der aufrufenden Komponente durchgeführt.

Updates, die Änderungen an anderen speichern (z. b. Dateisystem und Windows-Registrierung) betreffen, sind jedoch nicht unbedingt vollständig transaktional. Eine abgebrochene Transaktion kann diese Speicher in einem Zustand belassen, der nicht mit vorgenommenen Änderungen oder der COM+-Registrierungsdatenbank konsistent ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Installationspakete für COM+-Anwendungen werden erstellt.](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Anwendungs Proxys](deploying-application-proxies.md)
</dt> <dt>

[Das Hilfsprogramm zur Comrepl-Replikation](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



