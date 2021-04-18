---
title: Die Entwicklung von Dateisystemen
description: Bevor Computer für Betriebssysteme entwickelt wurden, wurde jeder Computer erstellt, um eine einzelne, proprietäre Anwendung auszuführen, die vollständige und exklusive Kontrolle über den gesamten Computer hatte.
ms.assetid: 46d497b5-c325-4395-8512-1ed4b88441de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc34dc699488b5952d52dfd13f49ea63aaa85aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339806"
---
# <a name="the-evolution-of-file-systems"></a>Die Entwicklung von Dateisystemen

Bevor Computer für Betriebssysteme entwickelt wurden, wurde jeder Computer erstellt, um eine einzelne, proprietäre Anwendung auszuführen, die vollständige und exklusive Kontrolle über den gesamten Computer hatte. Die Anwendung schreibt die persistenten Daten direkt auf einen Datenträger oder eine Trommel, indem Befehle direkt an den Datenträger Controller gesendet werden. Die Anwendung ist dafür verantwortlich, die absoluten Speicherorte der Daten auf dem Datenträger zu verwalten und sicherzustellen, dass Sie bereits vorhandene Daten nicht überschrieben haben. Da immer nur eine Anwendung auf dem Computer ausgeführt wurde, war diese Aufgabe nicht zu schwierig.

Die Einführung von Computersystemen, die mehrere Anwendungen ausführen konnten, erforderte einen Mechanismus, mit dem sichergestellt werden kann, dass die Anwendungen nicht über die Daten der anderen Anwendungen geschrieben wurden. Anwendungsentwickler haben dieses Problem gelöst, indem Sie einen einzelnen Standard für die Unterscheidung von Datenträger Sektoren verwenden, die freigegeben wurden, indem Sie Sie entsprechend markieren. In der Zeit wurden diese Standards zu einem Betriebssystem zusammengestellt, das verschiedene Dienste für die Anwendungen bereitstellte, einschließlich eines Dateisystems für die Verwaltung von persistenten Speicher. Bei der Einführung eines Dateisystems mussten Anwendungen nicht mehr direkt mit dem physischen Speichermedium umgehen. Stattdessen haben Sie einfach das Dateisystem angewiesen, Datenblöcke auf den Datenträger zu schreiben, und das Dateisystem muss sich Gedanken über die Vorgehensweise machen. Außerdem erlaubte das Dateisystem Anwendungen, Daten Hierarchien über eine Abstraktion zu erstellen, die als Verzeichnis bezeichnet wird. Ein Verzeichnis kann nicht nur Dateien, sondern auch andere Verzeichnisse enthalten, die wiederum eigene Dateien und Verzeichnisse enthalten könnten usw.

Das Dateisystem hat eine einzelne Dereferenzierungsebene zwischen Anwendungen und dem Datenträger bereitgestellt, und das Ergebnis war, dass jede Anwendung eine Datei als einzelner zusammenhängender Stream von Bytes auf dem Datenträger sah, obwohl das Dateisystem tatsächlich die Datei in separaten Sektoren gespeichert hat. Die Dereferenzierung gab an, dass die Anwendungen die absolute Position von Daten auf einem Speichergerät nicht verfolgen mussten.

Heute bieten praktisch alle System-APIs für die Dateieingabe und-Ausgabe Anwendungen zum Schreiben von Informationen in eine Flatfile. Anwendungen sehen diese Datei als einen einzelnen Datenstrom, der so groß wie erforderlich vergrößert werden kann, bis der Datenträger voll ist. Lange Zeit waren diese APIs für Anwendungen ausreichend, um Ihre permanenten Informationen zu speichern. Anwendungen haben bedeutende Neuerungen in Bezug auf den Umgang mit einem einzelnen Informationsdaten Strom hergestellt, um Features wie inkrementelle "schnelle" Speicherungen bereitzustellen.

In einer Welt von Komponenten Objekten ist das Speichern von Daten in einer einzelnen Flatfile jedoch nicht mehr effizient. Ebenso wie es bei Dateisystemen nicht mehr erforderlich ist, dass mehrere Anwendungen dasselbe Speichermedium gemeinsam verwenden, benötigen Komponenten Objekte jetzt ein System, das es Ihnen ermöglicht, Speicher innerhalb des konzeptionellen Frameworks einer einzelnen Datei freizugeben. Obwohl es möglich ist, die separaten Objekte mithilfe von herkömmlichem Flatfile-Speicher zu speichern, wenn sich eines der Objekte vergrößert, oder wenn Sie einfach ein anderes Objekt hinzufügen, ist es erforderlich, die gesamte Datei in den Arbeitsspeicher zu laden, das neue Objekt einzufügen und die gesamte Datei zu speichern. Dieser Prozess kann sehr zeitaufwändig sein.

Die von com bereitgestellte Lösung besteht darin, eine zweite Dereferenzierungsebene zu implementieren: ein Dateisystem in einer Datei. Der Flatfile-Speicher erfordert, dass eine große zusammenhängende Sequenz von Bytes auf dem Datenträger durch ein einzelnes Datei Handle mit einem einzelnen Such Zeiger manipuliert wird. Im Gegensatz dazu definiert com-strukturierter Speicher, wie eine einzelne Dateisystem Entität als strukturierte Auflistung von zwei Typen von Objekten behandelt werden kann – Speicher und Streams –, die wie Verzeichnisse und Dateien fungieren.

 

 




