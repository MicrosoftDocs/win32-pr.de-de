---
title: Schnittstellen und Schnittstellen Implementierungen
description: COM ist ein grundlegender Unterschied zwischen Schnittstellendefinitionen und ihren Implementierungen.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8df92ac8b851925d82a4b03505fa4c5ab3dc39
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "104038659"
---
# <a name="interfaces-and-interface-implementations"></a>Schnittstellen und Schnittstellen Implementierungen

COM ist ein grundlegender Unterschied zwischen Schnittstellendefinitionen und ihren Implementierungen.

Eine *Schnittstelle* ist tatsächlich ein Vertrag, der aus einer Gruppe verwandter Funktionsprototypen besteht, deren Verwendung definiert ist, deren Implementierung jedoch nicht ist. Diese Funktionsprototypen entsprechen reinen virtuellen Basisklassen in der C++-Programmierung. Eine Schnittstellen Definition gibt die Element Funktionen der Schnittstelle an, sogenannte *Methoden*, die Rückgabe Typen, die Anzahl und die Typen ihrer Parameter und deren Anforderungen. Einer Schnittstelle ist keine Implementierung zugeordnet.

Eine *Schnittstellen Implementierung* ist der Code, den ein Programmierer bereitstellt, um die in einer Schnittstellen Definition angegebenen Aktionen auszuführen. Implementierungen von vielen der Schnittstellen, die ein Programmierer in einer objektbasierten Anwendung verwenden kann, sind in den COM-Bibliotheken enthalten. Programmierer können diese Implementierungen jedoch ignorieren und eigene schreiben. Eine Schnittstellen Implementierung muss einem-Objekt zugeordnet werden, wenn eine Instanz dieses Objekts erstellt wird, und die-Implementierung stellt die Dienste bereit, die das-Objekt anbietet.

Eine hypothetische Schnittstelle namens IStack könnte z. b. zwei Methoden mit dem Namen Push und Pop definieren, die angeben, dass aufeinanderfolgende Aufrufe der Pop-Methode in umgekehrter Reihenfolge Werte zurückgeben, die zuvor an die Push-Methode übermittelt wurden. Diese Schnittstellen Definition gibt nicht an, wie die Funktionen im Code implementiert werden. Beim Implementieren der Schnittstelle kann ein Programmierer den Stapel als Array implementieren und die Push-und Pop-Methoden so implementieren, dass er auf dieses Array zugreift, während ein anderer Programmierer eine verknüpfte Liste verwenden und die Methoden entsprechend implementieren würde. Unabhängig von einer bestimmten Implementierung der Push-und Pop-Methoden wird die Speicher interne Darstellung eines Zeigers auf eine IStack-Schnittstelle und somit die Verwendung durch einen Client vollständig durch die Schnittstellen Definition bestimmt.

Einfache Objekte unterstützen nur eine einzige Schnittstelle. Kompliziertere Objekte, wie z. b. einbettbare Objekte, unterstützen in der Regel mehrere Schnittstellen. Clients haben Zugriff auf ein COM-Objekt nur über einen Zeiger auf eine der Schnittstellen. Dies ermöglicht es dem Client wiederum, jede der Methoden aufzurufen, die diese Schnittstelle bilden. Diese Methoden bestimmen, wie ein Client die Daten des Objekts verwenden kann.

Schnittstellen definieren einen Vertrag zwischen einem Objekt und seinen Clients. Der Vertrag gibt die Methoden an, die jeder Schnittstelle zugeordnet werden müssen, und das Verhalten der einzelnen Methoden muss in Bezug auf Eingabe und Ausgabe sein. Der Vertrag definiert in der Regel nicht, wie die Methoden in einer Schnittstelle implementiert werden. Ein weiterer wichtiger Aspekt des Vertrags besteht darin, dass ein Objekt, das eine Schnittstelle unterstützt, alle Methoden der Schnittstelle auf irgendeine Weise unterstützen muss. Nicht alle Methoden in einer Implementierung müssen etwas tun. Wenn ein Objekt die von einer Methode implizierte Funktion nicht unterstützt, ist die Implementierung möglicherweise eine einfache Rückgabe oder möglicherweise die Rückgabe einer aussagekräftigen Fehlermeldung – aber die Methoden müssen vorhanden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Objekte und-Schnittstellen](com-objects-and-interfaces.md)
</dt> </dl>

 

 




