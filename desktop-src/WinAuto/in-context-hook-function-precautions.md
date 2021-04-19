---
title: Vorsichtsmaßnahmen für In-Context Hook-Funktion
description: Aus Leistungsgründen registrieren Client Entwickler kontextbasierte Hook-Funktionen.
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e319037cb1295725548b3361bf076b4b1f760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339895"
---
# <a name="in-context-hook-function-precautions"></a>Vorsichtsmaßnahmen für In-Context Hook-Funktion

Aus Leistungsgründen registrieren Client Entwickler kontextbasierte Hook-Funktionen. Da diese Hook-Funktionen jedoch im Adressraum des Servers zugeordnet sind, müssen Client-und Server Entwickler Vorsichtsmaßnahmen treffen, um sicherzustellen, dass die Ereignisverarbeitung reibungslos verläuft.

## <a name="precautions-for-client-developers"></a>Vorsichtsmaßnahmen für Client Entwickler

Client Entwickler sollten folgende Probleme beachten:

-   In-context-Hook-Funktionen sollten nicht viel Prozessorzeit verwenden, da die Hook-Funktion zurückgegeben werden muss, bevor die Serveranwendung fortgesetzt wird.
-   Nachdem ein Ereignis ausgelöst wurde, ist es möglich, dass das Fenster, das einem Ereignis zugeordnet ist, nicht mehr zu dem Zeitpunkt vorhanden ist, zu dem die Hook-Funktion aufgerufen wird. Clients müssen überprüfen, ob das einem Ereignis zugeordnete Fenster noch vorhanden ist, bevor Sie eine andere Aktion im Zusammenhang mit dem Ereignis ausführen. Um sicherzustellen, dass noch ein Fenster vorhanden ist, verwenden Clients die Microsoft Win32 [**IsWindow**](/windows/desktop/api/winuser/nf-winuser-iswindow) -Funktion.
-   Wenn die dll, in der die Hook-Funktion definiert ist, mit einer anderen DLL verknüpft ist, müssen Client Entwickler sicherstellen, dass das System die andere dll lädt. Wenn Sie implizit (mit DEF-und DEF-Dateien) verknüpfen, muss sich die zusätzliche DLL entweder im Windows-Verzeichnis oder in einem der Systemverzeichnisse befinden, wie z \\ . b. Windows System, Windows \\ system32 oder Windows \\ syswow64. Wenn Sie explizit (mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)) verknüpfen, muss der vollständige Pfad zu dem Verzeichnis, in dem sich die zusätzliche dll befindet, im **LoadLibrary**-Befehl angegeben werden.
-   In-context-Hook-Funktionen können einen Stapelüberlauf verursachen, wenn die dll, die die Hook-Funktion enthält, in eine 16-Bit-Anwendung geladen wird. Dieses Problem tritt auf, weil 16-Bit-Anwendungen eine festgelegte Stapelgröße verwenden, die nicht groß genug ist, um die Kette von System Funktionsaufrufen zu unterstützen, die zu einem Aufruf der Hook-Funktion führen.

## <a name="precautions-for-server-developers"></a>Vorsichtsmaßnahmen für Server Entwickler

Server Entwickler müssen sich bewusst sein, dass Client Anwendungen möglicherweise kontextabhängige Hook-Funktionen registrieren. Wenn ein Server [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)aufruft, muss er darauf vorbereitet sein, [**WM \_ GetObject**](wm-getobject.md) und andere [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden zu verarbeiten.

## <a name="invalid-interface-pointers"></a>Ungültige Schnittstellen Zeiger

Wenn ein Client [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) innerhalb einer Kontext gebundenen Hook-Funktion aufruft, zeigt der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger, der zurückgegeben wird, direkt auf den Code im Adressbereich des Servers. Wenn der Client eine Schnittstellen Eigenschaft mithilfe dieses Zeigers aufruft, ist die Component Object Model (com)-Bibliothek nicht daran beteiligt, das Marshalling (Verpacken und Senden von Schnittstellenparametern über Prozess Grenzen hinweg) oder das Marshalling (entpacken von Parametern, die über Prozess Grenzen hinweg gesendet wurden) zu verwenden, und erkennt nicht, ob ein Objekt zerstört wird.

Wenn der Client eine Schnittstellen Eigenschaft für ein Objekt aufruft, das zerstört wird, verursacht der ungültige Schnittstellen Zeiger einen allgemeinen Schutz Fehler im Adressraum des Servers, es sei denn, der Server erkennt diese Situation.

Zum Schutz vor ungültigen Schnittstellen Zeigern [Erstellen Server Proxy Objekte](creating-proxy-objects.md) , die barrierefreie Objekte umschließen und die Lebensdauer von zugänglichen Objekten überwachen. Wenn ein Client beispielsweise eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaft aufruft, um Informationen zu einem Objekt zu erhalten, prüft der Proxy, ob das barrierefreie Objekt weiterhin verfügbar ist, und leitet die Anforderung des Clients an das barrierefreie Objekt weiter, wenn dies der Fall ist. Wenn das barrierefreie Objekt zerstört wird, gibt der Proxy einen Fehler an den Client zurück.

 

 