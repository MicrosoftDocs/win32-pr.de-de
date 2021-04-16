---
description: Viele der in diesem Thema beschriebenen Debuggingfunktionen sind in der DirectShow-Basisklassen Bibliothek implementiert. Weitere Informationen finden Sie unter DirectShow-Basisklassen.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Debugging von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522555"
---
# <a name="debugging-directshow-filters"></a>Debugging von DirectShow-Filtern

Viele der in diesem Thema beschriebenen Debuggingfunktionen sind in der DirectShow-Basisklassen Bibliothek implementiert. Weitere Informationen finden Sie unter [DirectShow-Basisklassen](directshow-base-classes.md).

## <a name="assertion-checking"></a>Assertionüberprüfung

Verwenden Sie die Assert-Überprüfung. Assertionen können Annahmen, die Sie in Ihrem Code vornehmen, über Vorbedingungen und nach Bedingungen überprüfen. DirectShow bietet mehrere Assert-Makros. Weitere Informationen finden Sie unter [Assert-und breakpointmakros](assert-and-breakpoint-macros.md).

## <a name="object-names"></a>Objektnamen

In Debugbuilds gibt es eine globale Liste von Objekten, die von der [**cbaseobject**](cbaseobject.md) -Klasse abgeleitet werden. Wenn Objekte erstellt werden, werden Sie der Liste hinzugefügt. Wenn Sie zerstört werden, werden Sie aus der Liste entfernt. Um eine Liste dieser Objekte anzuzeigen, müssen Sie die [**dbgdumpobjectregiester**](dbgdumpobjectregister.md) -Funktion aufrufen.

Die Konstruktormethode für die [**cbaseobject**](cbaseobject.md) -Basisklasse – und die meisten davon abgeleiteten Klassen – enthalten einen Parameter für den Namen des Objekts. Geben Sie Ihren Objekten eindeutige Namen, um Sie zu identifizieren. Verwenden Sie das [**Name**](name.md) -Makro, wenn Sie den Namen deklarieren, sodass der Name nur in Debugbuilds zugeordnet wird. In Einzelhandels Builds wird der Name **null**.

## <a name="debug-logging"></a>Debugprotokollierung

Die [**dbglog**](dbglog.md) -Funktion zeigt Debugmeldungen an, während das Programm ausgeführt wird. Verwenden Sie diese Funktion, um die Ausführung der Anwendung oder des Filters nachzuverfolgen. Sie können Rückgabecodes, die Werte von Variablen und alle anderen relevanten Informationen protokollieren.

Jede Debugmeldung weist einen Typ auf, z \_ . b. Protokoll Ablauf Verfolgung oder Protokoll \_ Fehler, und eine Debugebene, die die Wichtigkeit der Nachricht angibt. Nachrichten mit niedrigeren debugebenen sind wichtiger als solche mit höheren Ebenen.

Im folgenden Beispiel trennt ein hypothetischer Filter die Verbindung einer PIN von einem Array von Pins. Wenn der Verbindungsversuch erfolgreich ist, zeigt der Filter eine Protokoll Ablauf \_ Verfolgungs Meldung an. Wenn der Versuch fehlschlägt, wird eine Protokoll \_ Fehlermeldung angezeigt:


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



Beim Debuggen können Sie die Debugebene für jeden Nachrichtentyp festlegen. Außerdem verwaltet jedes Modul (dll oder ausführbare Datei) seine eigenen debugebenen. Wenn Sie einen Filter testen, erhöhen Sie die debugebenen für die dll, die den Filter enthält.

Weitere Informationen finden Sie unter [Debug Output Functions](debug-output-functions.md).

## <a name="critical-sections"></a>Kritische Abschnitte

Um Deadlocks leichter nachvollziehen zu können, schließen Sie Assertionen ein, die bestimmen, ob der aufrufende Code einen bestimmten kritischen Abschnitt besitzt. Die [**critcheckin**](critcheckin.md) -und [**critcheckout**](critcheckout.md) -Funktionen geben an, ob der aufrufende Thread einen kritischen Abschnitt besitzt. In der Regel würden Sie diese Funktionen innerhalb eines Assert-Makros aufzurufen.

Sie können auch die [**dbglocktrace**](dbglocktrace.md) -Funktion verwenden, um zu verfolgen, wann kritische Abschnitte gespeichert oder freigegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen in DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



