---
description: Mit der unten beschriebenen Taxonomie wird die Steuerungsebene, die sich auf sich selbst bezieht, durch die Art und Weise, wie eine Multipoint-Sitzung eingerichtet wird, von der Datenebene unterschieden, die die Übertragung von Daten zwischen Sitzungsteilnehmern behandelt
ms.assetid: d138347a-826a-4615-afbd-ffa7726a47eb
title: Multipoint-Taxonomie und Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ecdfe59640ec58b592aace4e46c66faf752281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348775"
---
# <a name="multipoint-taxonomy-and-glossary"></a>Multipoint-Taxonomie und Glossar

Mit der unten beschriebenen Taxonomie wird die Steuerungsebene, die sich auf sich selbst bezieht, durch die Art und Weise, wie eine Multipoint-Sitzung eingerichtet wird, von der Datenebene unterschieden, die die Übertragung von Daten zwischen Sitzungsteilnehmern behandelt

Auf der Steuerungsebene gibt es zwei unterschiedliche Arten der Sitzungs Einrichtung:

-   zeln
-   nicht Stamm

Für eine Stamm Steuerungsebene gibt es einen speziellen Teilnehmer mit dem Namen "c root", der sich \_ von den restlichen Membern dieser Multipoint-Sitzung unterscheidet, die jeweils als "c-Blatt" bezeichnet werden \_ . Der c-Stamm \_ muss für die gesamte Dauer der Multipoint-Sitzung vorhanden sein, da die Sitzung in Abwesenheit des c-Stamms aufgeschlüsselt wird \_ . Der c-Stamm \_ initiiert in der Regel die Multipoint-Sitzung, indem er die Verbindung mit einem c- \_ Blatt oder eine Reihe von c-Blättern einrichtet \_ . Der c-Stamm kann \_ Weitere c-Blätter hinzufügen \_ , oder (in einigen Fällen) kann ein c- \_ Blatt \_ zu einem späteren Zeitpunkt dem c-Stamm beitreten. Beispiele für die Stamm Steuerungsebene finden Sie unter ATM und St-II.

Bei einer nicht stammenden Steuerungsebene werden alle Member, die einer Multipoint-Sitzung angehören, verlassen, d. h., es ist kein spezieller Teilnehmer vorhanden, der als c-Stamm fungiert \_ . Jedes c- \_ Blatt muss sich selbst einer bereits vorhandenen Multipoint-Sitzung hinzufügen, die entweder immer verfügbar ist (wie bei einer IP-Multicast Adresse) oder über einen OOB-Mechanismus eingerichtet wurde, der außerhalb des Umfangs dieser Diskussion liegt (und daher nicht in den vorgeschlagenen Windows Sockets-Erweiterungen behandelt wird). Eine andere Möglichkeit, dies zu überprüfen, besteht darin, dass ein c-Stamm \_ weiterhin vorhanden ist, aber als Teilnehmer in der netzwerkcloud betrachtet werden kann. Da immer noch ein Steuerelement Stamm vorhanden ist, kann eine nicht-Stamm Steuerungsebene auch als implizit zu einem Stamm angesehen werden. Beispiele für diese Art von implizit zu entfernenden Multipoint-Schemas: eine teleconferferenzierungsbrücke, das IP-Multicast System, eine Multipoint-Steuerungseinheit (MCU) in einer H. 320-Videokonferenz usw.

In der Datenebene gibt es auch zwei Arten von Daten Übertragungs Stilen:

-   zeln
-   nicht Stamm

In einer Datenebene mit Stamms ist ein spezieller Teilnehmer namens d \_ root vorhanden. Die Datenübertragung erfolgt nur zwischen dem d-Stamm \_ und den restlichen Membern dieser Multipoint-Sitzung, die jeweils als d-Blatt bezeichnet werden \_ . Der Datenverkehr kann unidirektional oder bidirektional sein. Die Daten, die aus dem Stammverzeichnis d gesendet werden \_ , werden (falls erforderlich) dupliziert und an jedes d-Blatt übermittelt \_ , während die Daten von d- \_ Leafs nur an den d-Stamm gesendet werden \_ . Im Fall einer Datenebene mit Stammdaten ist unter d-Blätter kein Datenverkehr zulässig \_ . Ein Beispiel für ein Protokoll, das eine Datenebene mit Stammdaten verwendet, ist St-II.

In einer Datenebene, die keine Daten enthält, sind alle Teilnehmer in dem Sinne gleich, dass alle gesendeten Daten an alle anderen Teilnehmer in derselben Multipoint-Sitzung übermittelt werden. Ebenso kann jeder d- \_ Blattknoten Daten von allen anderen d-Blättern empfangen \_ , in einigen Fällen auch von anderen Knoten, die nicht an der Multipoint-Sitzung teilnehmen. Es ist kein spezieller d-Stamm \_ Knoten vorhanden. IP-Multicast ist ein Beispiel für ein Protokoll, das eine Datenebene ohne Stamm verwendet.

Beachten Sie, dass die Frage, ob die Duplizierung von Dateneinheiten auftritt oder ob eine freigegebene Struktur oder mehrere kürzeste Pfad Strukturen für die Multipoint-Verteilung verwendet werden, Protokoll Probleme sind. Daher sind Sie für die Schnittstelle, die der Client zum Durchführen von Multipoint-Kommunikationen verwendet, irrelevant. Diese Probleme werden daher nicht von der Windows Sockets-Schnittstelle adressiert.

Die folgende Tabelle zeigt die oben beschriebene Taxonomie und gibt an, wie vorhandene Schemas in die einzelnen Kategorien von Steuerelementen und Daten Ebenen passen. Beachten Sie, dass es anscheinend keine Multipoint-Schemas gibt, die eine nicht-rooting-Steuerungsebene zusammen mit einer Datenebene mit Stamm Ebene verwenden.

| Datenebene           | Beispiele für die Steuerelement Ebene | Beispiele für eine nicht Stamm Ende (implizite Stamm Ende) Steuerungsebene |
|----------------------|-------------------------------|----------------------------------------------------|
| Datenebene mit Stamm    | ATM, St-II                    | Keine bekannten Beispiele                                  |
| Datenebene ohne Stamm | T. 120                         | IP-Multicast, H. 320 (MCU)                          |



 

 

 



