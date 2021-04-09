---
description: Die in diesem Abschnitt beschriebene Taxonomie unterscheidet zunächst die Steuerungsebene, die sich auf die Art und Weise der Einrichtung einer Multipoint-Sitzung bezieht, von der Datenebene, die die Übertragung von Daten zwischen Sitzungsteilnehmern behandelt.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Multipoint-Taxonomie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97159312a2e431cb82b73336a13904c6b5ab021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862559"
---
# <a name="multipoint-taxonomy"></a>Multipoint-Taxonomie

Die in diesem Abschnitt beschriebene Taxonomie unterscheidet zunächst die Steuerungsebene, die sich auf die Art und Weise der Einrichtung einer Multipoint-Sitzung bezieht, von der Datenebene, die die Übertragung von Daten zwischen Sitzungsteilnehmern behandelt.

## <a name="session-establishment-in-the-control-plane"></a>Einrichtung der Sitzung auf der Steuerungsebene

Auf der Steuerungsebene gibt es zwei unterschiedliche Arten der Sitzungs Einrichtung:

-   zeln
-   nicht Stamm

Im Fall von rootsteuerelementen ist ein spezieller Teilnehmer, c \_ root, vorhanden, der sich von den restlichen Membern dieser Multipoint-Sitzung unterscheidet, die jeweils als c- \_ Blatt bezeichnet werden. Der c-Stamm \_ muss für die gesamte Dauer der Multipoint-Sitzung vorhanden sein, da die Sitzung in Abwesenheit des c-Stamms untergliedert ist \_ . Der c-Stamm \_ initiiert in der Regel die Multipoint-Sitzung, indem er die Verbindung mit einem c- \_ Blatt oder eine Reihe von c-Blättern einrichtet \_ . Der c-Stamm kann \_ Weitere c-Blätter hinzufügen \_ , oder (in einigen Fällen) kann ein c- \_ Blatt \_ zu einem späteren Zeitpunkt dem c-Stamm beitreten. Beispiele für die Stamm Steuerungsebene finden Sie unter ATM und St-II.

Bei einer nicht stammenden Steuerungsebene werden alle Member, die zu einer Multipoint-Sitzung gehören, verlassen, d. h., es ist kein spezieller Teilnehmer vorhanden, der als c-Stamm fungiert \_ . Jedes c- \_ Blatt muss sich selbst einer bereits vorhandenen Multipoint-Sitzung hinzufügen, die immer verfügbar ist (wie bei einer IP-Multicast Adresse) oder durch einen Out-of-Band-Mechanismus (OOB) eingerichtet wurde, der außerhalb des Bereichs der Windows Sockets-Spezifikation liegt.

Eine andere Möglichkeit, dies zu überprüfen, besteht darin, dass ein c-Stamm \_ weiterhin vorhanden ist, aber als Teilnehmer in der netzwerkcloud betrachtet werden kann. Da immer noch ein Steuerelement Stamm vorhanden ist, kann eine nicht-Stamm Steuerungsebene auch als implizit zu einem Stamm angesehen werden. Beispiele für diese Art von implizit stammenden Multipoint-Schemas:

-   Eine teleconferferenzierungsbrücke.
-   Das IP-Multicast System.
-   Eine Multipoint-Steuerungseinheit (MCU) in einer H. 320-Videokonferenz.

## <a name="data-transfer-in-the-data-plane"></a>Datenübertragung in der Datenebene

In der Datenebene gibt es zwei Arten von Daten Übertragungs Stilen:

-   zeln
-   nicht Stamm

In einer Datenebene mit Stamms ist ein spezieller Teilnehmer namens d \_ root vorhanden. Die Datenübertragung erfolgt nur zwischen dem d-Stamm \_ und den restlichen Membern dieser Multipoint-Sitzung, die jeweils als d-Blatt bezeichnet werden \_ . Der Datenverkehr kann unidirektional oder bidirektional sein. Die Daten, die aus dem Stammverzeichnis von d gesendet \_ werden, werden (falls erforderlich) dupliziert und an jedes d-Blatt übermittelt \_ , während die Daten von d- \_ Leafs nur in den d-Stamm fließen \_ . Bei einer Datenebene mit Stammdaten ist kein Datenverkehr unter d- \_ Blätter zulässig. Ein Beispiel für ein Protokoll, das in der Datenebene verankert ist, ist St-II.

In einer Datenebene ohne Stamm sind alle Teilnehmer gleich, d. h. alle Daten, die Sie senden, werden an alle anderen Teilnehmer in derselben Multipoint-Sitzung übermittelt. Ebenso kann jeder d- \_ Blattknoten Daten von allen anderen d- \_ Blättern empfangen und in einigen Fällen von anderen Knoten, die nicht an der Multipoint-Sitzung teilnehmen. Es ist kein spezieller d-Stamm \_ Knoten vorhanden. IP-Multicast ist nicht in der Datenebene verankert.

Beachten Sie, dass die Frage, wo die Duplizierung von Dateneinheiten auftritt oder ob eine freigegebene Struktur oder mehrere kürzeste Pfad Strukturen für die Multipoint-Verteilung verwendet werden, Protokoll Probleme sind und für die Schnittstelle, die die Anwendung zum Ausführen von Multipoint-Kommunikationen verwenden würde, irrelevant ist. Diese Probleme werden daher in diesem Anhang oder der Windows Sockets-Schnittstelle nicht behandelt.

Die folgende Tabelle zeigt die oben beschriebene Taxonomie und gibt an, wie vorhandene Schemas in die einzelnen Kategorien passen. Beachten Sie, dass es anscheinend keine vorhandenen Schemas gibt, die eine nicht-rooting-Steuerungsebene und eine Datenebene mit Stamm Ebene verwenden.

|                      | Stamm Steuerungsebene | Nicht-Stamm Steuerungsebene (impliziter Stamm) |
|----------------------|----------------------|-------------------------------------------|
| Datenebene mit Stamm    | ATM, St-II           | Keine bekannten Beispiele.                        |
| Datenebene ohne Stamm | T. 120                | IP-Multicast, H. 320 (MCU)                 |



 

 

 



