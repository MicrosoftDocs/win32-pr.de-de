---
description: Der COM+-Katalog speichert COM+-Anwendungsattribute, Klassenattribute und Attribute auf Computerebene. Sie garantiert Konsistenz zwischen diesen Attributen und stellt allgemeine Vorgänge neben diesen Attributen zur Seite.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Der COM+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b345c45fddab245c1e2290dc279742ac7b3b6b25c093d677c74b232077b43ae1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305267"
---
# <a name="the-com-catalog"></a>Der COM+-Katalog

Der COM+-Katalog speichert COM+-Anwendungsattribute, Klassenattribute und Attribute auf Computerebene. Sie garantiert Konsistenz zwischen diesen Attributen und stellt allgemeine Vorgänge neben diesen Attributen zur Seite.

Der COM+-Katalog verwendet wie folgt zwei verschiedene Speicher:

-   Die COM+-Registrierungsdatenbank
-   Die Windows -Registrierung (**HKEY \_ CLASSES \_ ROOT**)

Der Katalog bietet eine einheitliche, logische Ansicht dieser beiden Speicher und macht sie über die COM+-Verwaltungsbibliothek verfügbar. Diese Bibliothek stellt über eine Skriptsprache alle Funktionen des Komponentendienste-Verwaltungstools zur Verfügung.

Für vorhandene COM-Komponenten, die keine neuen COM+-Dienste erfordern, erfolgt die Suche in der vorhandenen Windows Registrierung. Der COM+-Katalog verwendet auch die Windows für die Typbibliotheks- und Schnittstellenproxy-/Stubregistrierung.

## <a name="split-registration"></a>Registrierung aufteilen

Bei neuen Komponenten, bei denen es sich tatsächlich um bereits vorhandene COM-Komponenten handelt, die in der Dienstumgebung verwendet werden (z. B. MTS-Komponenten), wird der grundlegende COM-Aspekt der Registrierung in der Windows-Registrierung gespeichert, und neue Dienste und Attribute (z. B. Komponenten in der Warteschlange) werden in der COM+-Registrierungsdatenbank gespeichert. Dies wird als *geteilte Registrierung bezeichnet.*

Jedes Attribut wird nur an einem Speicherort gespeichert: entweder in Windows Registrierung oder in der COM+-Registrierungsdatenbank. Neue COM-Komponenten werden ausschließlich in der COM+-Registrierungsdatenbank registriert, mit einer Duplizierung in Windows Registrierung, damit vorhandene Tools sie verwenden können.

## <a name="transactional-updates-to-the-catalog"></a>Transaktionsupdates für den Katalog

Einige Vorgänge für den Katalog werden transaktional ausgeführt. Wenn Sie die COM+-Verwaltungsbibliothek über eine Transaktionskomponente aufrufen, werden die Updates der COM+-Registrierungsdatenbank innerhalb der Transaktionsgrenze der aufrufenden Komponente ausgeführt.

Updates, die Änderungen an anderen Speichern (z. B. das Dateisystem und die Windows) beinhalten, sind jedoch nicht garantiert vollständig transaktional. Eine abgebrochene Transaktion kann diese Speicher in einem Zustand be lassen, der nicht mit änderungen aneinander oder an der COM+-Registrierungsdatenbank inkonsistent ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Installationspaketen für COM+-Anwendungen](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Bereitstellen von Anwendungsproxies](deploying-application-proxies.md)
</dt> <dt>

[Das COMREPL-Replikations-Hilfsprogramm](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



