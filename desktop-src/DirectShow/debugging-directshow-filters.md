---
description: Viele der in diesem Thema beschriebenen Debugmöglichkeiten sind in der DirectShow-Basisklassenbibliothek implementiert. Weitere Informationen finden Sie unter DirectShow-Basisklassen.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Debuggen von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54532b68df09b78b3b03aa95d7dda5c84cdf7d770cffd131e47228e6d88cba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953289"
---
# <a name="debugging-directshow-filters"></a>Debuggen von DirectShow-Filtern

Viele der in diesem Thema beschriebenen Debugmöglichkeiten sind in der DirectShow-Basisklassenbibliothek implementiert. Weitere Informationen finden Sie unter [DirectShow-Basisklassen.](directshow-base-classes.md)

## <a name="assertion-checking"></a>Assertionsüberprüfung

Verwenden Sie assertionsüberprüfungen. Assertionen können Annahmen überprüfen, die Sie in Ihrem Code zu Vorbedingungen und Nachbedingungen treffen. DirectShow bietet mehrere Assertionsmakros. Weitere Informationen finden Sie unter [Assert- und Breakpointmakros.](assert-and-breakpoint-macros.md)

## <a name="object-names"></a>Objektnamen

In Debugbuilds gibt es eine globale Liste von -Objekten, die von der [**CBaseObject-Klasse abgeleitet**](cbaseobject.md) werden. Wenn Objekte erstellt werden, werden sie der Liste hinzugefügt. Wenn sie zerstört werden, werden sie aus der Liste entfernt. Um eine Liste dieser Objekte anzuzeigen, rufen Sie die [**DbgDumpObjectRegister-Funktion**](dbgdumpobjectregister.md) auf.

Die Konstruktormethode für die [**CBaseObject-Basisklasse**](cbaseobject.md) und die meisten davon abgeleiteten Klassen enthalten einen Parameter für den Namen des Objekts. Geben Sie Ihren Objekten eindeutige Namen, um sie zu identifizieren. Verwenden Sie [**das NAME-Makro,**](name.md) wenn Sie den Namen deklarieren, damit der Name nur in Debugbuilds zugeordnet wird. In Einzelhandels-Builds wird der Name **ZU NULL.**

## <a name="debug-logging"></a>Debugprotokollierung

Die [**DbgLog-Funktion**](dbglog.md) zeigt Debugmeldungen an, während das Programm ausgeführt wird. Verwenden Sie diese Funktion, um die Ausführung Ihrer Anwendung oder Ihres Filters zu verfolgen. Sie können Rückgabecodes, die Werte von Variablen und alle anderen relevanten Informationen protokollieren.

Jede Debugmeldung verfügt über einen Typ, z. B. LOG TRACE oder LOG ERROR, und eine Debugebene, die die Wichtigkeit \_ \_ der Nachricht angibt. Nachrichten mit niedrigeren Debugebenen sind wichtiger als Nachrichten mit höheren Ebenen.

Im folgenden Beispiel trennt ein hypothetischer Filter eine Stecknadel von einem Array von Stecknadeln. Wenn der Verbindungsversuch erfolgreich ist, zeigt der Filter eine LOG \_ TRACE-Meldung an. Wenn der Versuch fehlschlägt, wird eine LOG \_ ERROR-Meldung angezeigt:


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



Beim Debuggen können Sie die Debugebene für jeden Nachrichtentyp festlegen. Außerdem verwaltet jedes Modul (DLL oder ausführbare Datei) seine eigenen Debugebenen. Wenn Sie einen Filter testen, erhöhen Sie die Debugebenen für die DLL, die den Filter enthält.

Weitere Informationen finden Sie unter [Debugausgabefunktionen](debug-output-functions.md).

## <a name="critical-sections"></a>Kritische Abschnitte

Um die Nachverfolgung von Deadlocks zu vereinfachen, schließen Sie Assertionen ein, die bestimmen, ob der aufrufende Code einen bestimmten kritischen Abschnitt besitzt. Die [**Funktionen CritCheckIn**](critcheckin.md) und [**CritCheckOut**](critcheckout.md) geben an, ob der aufrufende Thread einen kritischen Abschnitt besitzt. In der Regel würden Sie diese Funktionen innerhalb eines Assert-Makros aufrufen.

Sie können auch die [**DbgLockTrace-Funktion**](dbglocktrace.md) verwenden, um zu verfolgen, wann kritische Abschnitte gehalten oder freigegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



