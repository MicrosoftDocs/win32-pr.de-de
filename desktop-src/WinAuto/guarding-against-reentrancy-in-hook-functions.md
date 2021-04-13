---
title: Schutz vor erneuten eintreten in Hook-Funktionen
description: Während eine Hook-Funktion ein Ereignis verarbeitet, können zusätzliche Ereignisse ausgelöst werden, was dazu führen kann, dass die Hook-Funktion erneut eintritt, bevor die Verarbeitung für das ursprüngliche Ereignis abgeschlossen ist.
ms.assetid: 2382e7a4-82df-423a-8479-66e28baf8105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e2b0dc6f8951bf48ce3fecabd3a81bd345388d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390777"
---
# <a name="guarding-against-reentrancy-in-hook-functions"></a>Schutz vor erneuten eintreten in Hook-Funktionen

Während eine Hook-Funktion ein Ereignis verarbeitet, können zusätzliche Ereignisse ausgelöst werden, was dazu führen kann, dass die Hook-Funktion erneut eintritt, bevor die Verarbeitung für das ursprüngliche Ereignis abgeschlossen ist. Das Problem mit dem erneuten eintreten in Hook-Funktionen besteht darin, dass Ereignisse außerhalb der Reihenfolge abgeschlossen werden, es sei denn, die Hook-Funktion behandelt diese Situation.

Stellen Sie sich z. b. einen Fall vor, in dem eine Hook-Funktion in einem Bildschirm Leseprogramm das [**Ereignis \_ Objekt \_ ValueChange**](event-constants.md) -Ereignis für ein Bearbeitungs Steuerelement verarbeitet. Wenn beim Verarbeiten des ersten Wert Änderungs Ereignisses die Hook-Funktion erneut eingegeben wird, um ein nachfolgendes Wert Änderungs Ereignis zu verarbeiten, wird das zweite Ereignis vor dem ersten Ereignis abgeschlossen. Diese Situation führt dazu, dass die Bildschirmausgabe falsche Informationen an den Benutzer übermittelt.

Da die Ereignisverarbeitung unterbrochen wird, werden möglicherweise jederzeit weitere Ereignisse empfangen, wenn die Hook-Funktion eine Funktion aufruft, die bewirkt, dass die Nachrichten Warteschlange des besitzenden Threads überprüft wird. Dies geschieht, wenn eine der folgenden Aktionen innerhalb der Hook-Funktion aufgerufen wird:

-   Die Windows [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)-, [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)-, [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)-, [**Dialogbox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)-oder [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) -Funktion
-   Die Microsoft Active Accessibility Functions [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   Eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle oder eine andere Component Object Model (com)-Eigenschaft oder-Methode, die Prozess Grenzen überschneidet

Da Hook-Funktionen [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) -und [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften und-Methoden aufzurufen, ist es nicht möglich, den erneuten eintreten zu verhindern. Die einzige Lösung besteht darin, dass Client Entwickler in der Hook-Funktion Code hinzufügen können, der einen erneuten eintreten erkennt und geeignete Maßnahmen ergreifen soll, wenn die Hook-Funktion erneut eingegeben wird.

 

 