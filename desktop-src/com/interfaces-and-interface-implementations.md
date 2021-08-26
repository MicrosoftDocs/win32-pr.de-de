---
title: Schnittstellen und Schnittstellenimplementierung
description: COM unterscheidet grundlegend zwischen Schnittstellendefinitionen und deren Implementierungen.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee00521b847acbd063f1cd7ad84a0eb231f78d7bd274b7a4658996dbdd61150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992700"
---
# <a name="interfaces-and-interface-implementations"></a>Schnittstellen und Schnittstellenimplementierung

COM unterscheidet grundlegend zwischen Schnittstellendefinitionen und deren Implementierungen.

Eine *Schnittstelle* ist eigentlich ein Vertrag, der aus einer Gruppe verwandter Funktionsprototypen besteht, deren Verwendung definiert ist, deren Implementierung jedoch nicht ist. Diese Funktionsprototypen entsprechen reinen virtuellen Basisklassen in der C++-Programmierung. Eine Schnittstellendefinition gibt die Memberfunktionen der Schnittstelle an, die als Methoden bezeichnet werden, deren Rückgabetypen, die Anzahl und Typen ihrer Parameter und deren Aufgaben. Einer Schnittstelle ist keine Implementierung zugeordnet.

Eine *Schnittstellenimplementierung* ist der Code, den ein Programmierer zur Ausführung der in einer Schnittstellendefinition angegebenen Aktionen liefert. Implementierungen vieler Schnittstellen, die ein Programmierer in einer objektbasierten Anwendung verwenden kann, sind in den COM-Bibliotheken enthalten. Programmierer können diese Implementierungen jedoch ignorieren und eigene Implementierungen schreiben. Eine Schnittstellenimplementierung muss einem -Objekt zugeordnet werden, wenn eine Instanz dieses Objekts erstellt wird, und die Implementierung stellt die Dienste bereit, die das -Objekt anbietet.

Beispielsweise kann eine hypothetische Schnittstelle mit dem Namen IStack zwei Methoden namens Push und Pop definieren, die angeben, dass aufeinander folgende Aufrufe der Pop-Methode Werte in umgekehrter Reihenfolge zurückgeben, die zuvor an die Push-Methode übergeben wurden. Diese Schnittstellendefinition würde nicht angeben, wie die Funktionen im Code implementiert werden sollen. Bei der Implementierung der -Schnittstelle könnte ein Programmierer den Stapel als Array implementieren und die Push- und Pop-Methoden so implementieren, dass auf dieses Array zugreifen kann, während ein anderer Programmierer eine verknüpfte Liste verwenden und die Methoden entsprechend implementieren würde. Unabhängig von einer bestimmten Implementierung der Push- und Pop-Methoden wird die Darstellung eines Zeigers im Arbeitsspeicher auf eine IStack-Schnittstelle und somit deren Verwendung durch einen Client vollständig durch die Schnittstellendefinition bestimmt.

Einfache Objekte unterstützen nur eine einzelne Schnittstelle. Kompliziertere Objekte, z. B. einbettbare Objekte, unterstützen in der Regel mehrere Schnittstellen. Clients haben nur über einen Zeiger auf eine ihrer Schnittstellen Zugriff auf ein COM-Objekt, wodurch der Client wiederum eine der Methoden aufrufen kann, aus denen diese Schnittstelle erstellt wird. Diese Methoden bestimmen, wie ein Client die Daten des Objekts verwenden kann.

Schnittstellen definieren einen Vertrag zwischen einem Objekt und seinen Clients. Der Vertrag gibt die Methoden an, die den einzelnen Schnittstellen zugeordnet werden müssen, und gibt an, wie das Verhalten der einzelnen Methoden in Bezug auf Eingabe und Ausgabe sein muss. Der Vertrag definiert im Allgemeinen nicht, wie die Methoden in einer Schnittstelle implementiert werden. Ein weiterer wichtiger Aspekt des Vertrags ist, dass ein Objekt, das eine Schnittstelle unterstützt, alle Methoden dieser Schnittstelle in irgendeiner Weise unterstützen muss. Nicht alle Methoden in einer Implementierung müssen etwas tun. Wenn ein Objekt die von einer Methode implizierte Funktion nicht unterstützt, kann seine Implementierung eine einfache Rückgabe oder vielleicht die Rückgabe einer aussagekräftigen Fehlermeldung sein. Die Methoden müssen jedoch vorhanden sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Objekte und -Schnittstellen](com-objects-and-interfaces.md)
</dt> </dl>

 

 




